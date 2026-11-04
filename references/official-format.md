# Stitch DESIGN.md 官方格式依据

核对日期：2026-11-04。当前文档使用 alpha 格式；以后更新时重新读取官方规范和安装版本的检查规则，不将本文当作永久缓存。

## 官方来源

- 概念与创建方式：https://stitch.withgoogle.com/docs/design-md/overview/
- 字段、类型和章节规范：https://stitch.withgoogle.com/docs/design-md/specification/
- 检查、比较与导出：https://stitch.withgoogle.com/docs/design-md/cli/
- 检查规则：https://stitch.withgoogle.com/docs/design-md/linting-rules/
- 操作 Stitch 的入门：https://stitch.withgoogle.com/docs/cli/overview/

前四项定义文件及其检查。最后一项介绍 Stitch 操作工具，不是设计取舍教程。生成自己的 DESIGN.md 不要求登录 Stitch 或上传项目资料。

## 本模板采用的核心格式

文件开头用两行独立的 --- 包住 YAML。核心字段：version（格式版本，当前 alpha）、name、description（可选）、colors、typography、rounded、spacing、components。设计版本、批准状态与日期放在正文，不与 version 的格式版本混用。

- colors：带 # 的 sRGB 十六进制字符串，包含 primary。组件的文字/背景配对要检查对比度。
- typography：命名对象；fontFamily 为字符串，fontSize 与 letterSpacing 为 px/em/rem 尺寸，fontWeight 为数值或可解析的数值字符串，lineHeight 为尺寸或无单位倍数。fontFeature 与 fontVariation 按需使用。
- rounded：命名尺寸；spacing：命名尺寸或数值。参数只保留项目实际使用的级别。
- components：每个组件是扁平的属性映射；核心属性为 backgroundColor、textColor、typography、rounded、padding、size、height、width。使用字符串值或 {path.to.token} 引用。
- 组件内允许引用整个字体对象，例如 {typography.body-md}；通常其他引用需指向单值。所有目标须存在，避免循环。
- hover、active、focus、disabled、loading 等适用状态用独立组件条目命名，必要的完整行为规则写在正文。独立条目显式引用基础参数，不假定消费者自动继承。

## 正文章节

保留适用章节，并按以下顺序使用原样的英文 ## 标题，避免加编号或改成中文导致检查器无法识别：
Overview → Colors → Typography → Layout → Elevation & Depth → Shapes → Components → Do's and Don'ts。

规范允许省略不适用章节，并支持扩展章节。品牌来源、图片、响应式细则、交互行为、映射、验证、待决事项和批准记录放在上述章节之后，清楚标注为项目扩展。重复二级标题属于错误。

## 检查与工具边界

在可用的 Node/npm 环境执行：

```sh
npx --yes @google/design.md lint DESIGN.md
```

正式项目优先使用项目固定的工具版本；记录实际执行版本。可用 spec 查看安装版本规范，用 diff 比较前后变化，用 export 导出参数。选择导出目标前核对项目框架，不直接覆盖已有配置。

处理 broken-ref、missing-primary、contrast-ratio、orphaned-tokens、missing-typography、section-order、missing-sections、token-summary 的结果。信息提示不等于失败；警告应修复或说明原因。

官方规范对未知组件属性写“警告”，但官方 lint 规则页将未知组件属性列入 broken-ref 错误；为兼容检查器，模板仅用核心属性。边框、阴影、焦点轮廓和动效行为放正文。额外自定义字段不等于官方支持的标准字段。

官方检查器主要覆盖结构、引用及组件颜色配对，不证明图片合适、中文排版正确、交互可用或整体符合可访问性要求；这些仍用真实样张检查。

## 与示例库的关系

VoltAgent/awesome-design-md 是第三方品牌分析案例库，可作灵感来源。格式与兼容性以官方规范及实际检查结果为准；案例参数不是设计默认值。沿用的上游许可保留于 THIRD-PARTY-NOTICE.txt。
