# 给 Designer：Design System Skill

用途：为不同项目制定自己的设计规则，输出 DESIGN.md 和可检查的视觉示例。文件格式以 Stitch 官方 DESIGN.md 规范为基础，不复制 Linear 的品牌风格。

## 先读 Stitch 官方原文（Main Source）

1. [DESIGN.md 概念与创建方法](https://stitch.withgoogle.com/docs/design-md/overview/)：了解两层结构和三种创建方式。
2. [格式规范](https://stitch.withgoogle.com/docs/design-md/specification/)：理解参数类型、引用、组件状态与标准章节。
3. [官方检查工具](https://stitch.withgoogle.com/docs/design-md/cli/) 和 [检查规则](https://stitch.withgoogle.com/docs/design-md/linting-rules/)：知道如何验证，以及检查的局限。
4. [Stitch CLI 入门](https://stitch.withgoogle.com/docs/cli/overview/)：需要操作 Stitch 时再读；写 DESIGN.md 不要求先登录或上传资料。

以上是主要技术来源。references/official-format.md 是有日期的阅读摘要，不能替代原文。视觉提案、审批及交付要求是本 skill 的团队流程；awesome-design-md 只是第三方案例参考。

## AI Designer

把整个 design-system 文件夹交给你的 AI 工具。支持 skills 的工具可安装到其技能目录；不支持的工具，要求它先读取 SKILL.md 及其中链接的两个文件。

可以直接发送：

请使用 design-system skill，为我们的项目制定设计系统。先阅读上述 Stitch 官方原文，再检查已有品牌和项目资料，整理约束及待决问题。没有确认视觉方向时，先给最多两个方向，并制作代表性区域及关键组件的桌面和手机样张。将规则整理进 DESIGN.md，区分草案、已批准和未验证内容。不要直接改造整个产品。项目背景与资料见随附内容。

## 真人 Designer

1. 阅读 SKILL.md，了解流程与交付要求。
2. 复制 assets/DESIGN.template.md 到项目指定位置，命名 DESIGN.md。
3. 按 references/decision-guide.md 制定规则，并用实际设计稿验证。
4. 删除不适用项，填写适用参数，记录尚未决定的问题。
5. 交付 DESIGN.md、桌面与手机样张、组件状态及验证记录。

模板中的数值是可检查格式的中性示例，必须按项目重新决定；待决定事项记录在 Open Questions。样张批准后再将对应范围标记 approved。Markdown 里的语义引用不会自行改变产品代码，开发需要按映射实施。

来源：Stitch 官方规范与检查规则见 references/official-format.md；工作流程与指南为本地编写，VoltAgent/awesome-design-md 仅作为第三方案例参考。上游许可随 THIRD-PARTY-NOTICE.txt 保留。没有附带 Linear 字体或品牌资产。
