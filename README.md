# Design System Skill

给 UI designer 使用的设计系统工作流程与 DESIGN.md 模板。以 **Google Stitch 官方 DESIGN.md 规范为主要技术来源**，帮助团队把品牌方向、视觉样张和可复用规则整理成项目自己的设计系统。

适用于真人设计师和 AI designer。它没有固定品牌风格，模板内的中性数值只是格式示例；不是 Google 官方发布的 skill，也不附带 Linear 的字体或品牌素材。

## 先读这里

- **第一次使用**：阅读 [Designer 使用说明](HANDOFF.md)。
- **AI 执行入口**：读取 [SKILL.md](SKILL.md)，按其中指引读取模板与参考文件。
- **制作项目文件**：复制 [DESIGN.template.md](assets/DESIGN.template.md)，在项目内命名 DESIGN.md。
- **怎样决定设计值**：阅读 [制定与检查指南](references/decision-guide.md)。

## Main Source：Stitch 官方原文

建议按顺序阅读，而不是只看本仓库的摘要。

| 官方文档 | 读完应理解什么 |
| --- | --- |
| [What is DESIGN.md?](https://stitch.withgoogle.com/docs/design-md/overview/) | 为什么要用设计系统文档，以及根据描述、品牌资料或手工创建的方法 |
| [The specification](https://stitch.withgoogle.com/docs/design-md/specification/) | 参数字段、类型、引用、组件变体和章节顺序 |
| [Validate with the CLI](https://stitch.withgoogle.com/docs/design-md/cli/) | 如何检查格式、比较版本和导出参数 |
| [Linting rules](https://stitch.withgoogle.com/docs/design-md/linting-rules/) | 错误、警告和信息提示分别代表什么 |
| [Stitch CLI Quickstart](https://stitch.withgoogle.com/docs/cli/overview/) | 需要通过命令操作 Stitch 时的安装、登录与生成页面流程；不是本 skill 的必装依赖 |

[本地阅读摘要](references/official-format.md) 标注了核对日期。后续以官方原文及实际工具版本为准；原文无法访问时明确标记尚未重新核对。

官方规范定义 DESIGN.md 的文件格式。本 skill 添加的视觉方向选择、样张审核、项目批准、代码映射及交付检查，是团队流程，不声称为 Google 官方标准。

[VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md) 仅作为第三方品牌案例参考，不是主要规范来源，也不代表各品牌官方发布的完整设计系统。

## 开始前准备什么

把以下已有资料交给 designer；缺少关键项时由 designer 集中询问：

- 项目目标、主要用户与最重要的操作。
- 平台、语言、页面或流程范围。
- 品牌 Logo、既有颜色或字体规范、已批准设计。
- 喜欢的参考与具体原因，以及要避免的方向。
- 已有项目文件或设计稿位置、最终批准人。

不要为了填模板虚构品牌事实或审批记录。

## AI Designer 如何使用

1. 下载或 clone **整个仓库**，保留 assets 与 references。
2. 在支持 skills 的工具中按该工具的安装方式加载本 skill；也可以不安装，直接要求 AI 读取仓库根目录 SKILL.md。
3. 提供项目资料，发送下面的指令。

```text
请使用这个仓库的 design-system skill，为当前项目制定专属设计系统。

先读取 SKILL.md，以及其中要求阅读的 Stitch 官方原文。
检查已有品牌和项目资料，区分已批准规则、建议和未知。
已有批准方向就沿用；否则给最多两个方向，并制作代表性区域和关键组件的桌面、手机样张让我确认。
按官方格式整理项目自己的 DESIGN.md，使用官方工具检查，并记录实际版本、结果和未解决问题。
模板参数只是示例。先交付设计系统和验证样张，不直接开发整个产品。
```

用户只要求文档时，允许交付明确标注的草案；没有实际打开或渲染检查的画面，不能声称视觉已验证。

## 真人 Designer 如何使用

1. 阅读上面的官方概念和格式原文，再阅读 HANDOFF.md。
2. 根据品牌与业务需求提出视觉方向，用真实内容制作桌面、手机样张。
3. 样张确认后填写模板：保留适用部分，删除不用的组件与规则。
4. 检查实际组件状态、长文字、图片裁切与手机表现。
5. 将 DESIGN.md、样张、检查记录和待决问题一起交付开发。

无需在任何真人设计工作之前安装 AI 工具。实际画面可使用团队现有设计工具制作。

## Skill 带领你完成的流程

了解项目 → 确定视觉方向 → 样张验证 → 记录设计规则 → 格式和实际效果检查 → 交付。

已有批准方向或规则时直接复用，不要求重新做选择。每个项目独立制定参数，不能把参考品牌或本模板的默认值自动当成批准规则。

## 应交付什么

- **项目 DESIGN.md**：参数与使用理由，包含状态和来源。
- **桌面、手机样张**：代表性区域与关键组件的实际效果。
- **验证记录**：工具版本、检查结果、样张位置及未验证项目。
- **待决与批准记录**：谁批准哪个版本和范围。
- **实施映射**：文档规则对应哪些设计变量或代码组件；未实现部分标记 planned。

Skill 的终点是设计系统与验证样张；完整产品实现、上传资料和正式发布按项目另行授权。

## 检查 DESIGN.md

需要可用的 Node/npm 环境。按照官方工具文档操作。下面版本已用于检查本仓库模板：

```sh
npx --yes @google/design.md@0.4.0 lint assets/DESIGN.template.md
```

项目填写完成后，应检查实际项目文件：

```sh
npx --yes @google/design.md@0.4.0 lint DESIGN.md
```

后续升级工具时重新核对官方规范并记录版本。修复错误，处理或解释警告。不要把格式检查通过等同于视觉优秀、交互可用或全面可访问性合规。

本次模板的检查结果见 [VALIDATION.md](VALIDATION.md)，尚未在客户项目中验证整个视觉工作流程。

## 文件说明

| 文件 | 作用 |
| --- | --- |
| SKILL.md | AI 执行入口，保留最初安装版本的注释快照 |
| HANDOFF.md | Designer 的阅读与操作说明 |
| assets/DESIGN.template.md | 按 Stitch 格式组织的可修改模板 |
| references/official-format.md | 官方链接、格式摘要及工具限制 |
| references/decision-guide.md | 设计取舍与实际样张检查 |
| VALIDATION.md | 已执行检查与局限 |
| THIRD-PARTY-NOTICE.txt | 保留的上游 MIT 许可声明 |

## 维护与来源

主要技术来源为本页列出的 Stitch 官方文档，核对日期 2026-11-04。工作流程与通用指南为本地编写；第三方案例参考的许可见 [THIRD-PARTY-NOTICE.txt](THIRD-PARTY-NOTICE.txt)。官方文档仅链接供原文阅读，没有作为本仓库内容重新分发。

更新顺序：重读官方规范与工具规则 → 修订模板与 skill → 检查实际模板 → 更新验证记录与使用说明。保留原有已批准项目规则，任何冲突应说明影响后处理。
