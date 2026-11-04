---
name: design-system
description: Create or revise a project-specific DESIGN.md using the official Stitch specification, visual examples, and implementation mappings. Use when a designer needs to define or document a design system; not for ordinary page implementation or copying another brand's appearance.
---

<!-- Original installed SKILL.md, preserved verbatim before official-spec revision (2026-11-04):
---
name: design-system
description: Create or revise a project-specific DESIGN.md with a reusable schema, visual examples, and implementation mappings. Use when a designer needs to define or document a design system; not for ordinary page implementation or copying another brand's appearance.
---

# Design System

帮助 designer 制定项目自己的设计系统，而不是把参考品牌的参数直接换名字。可供 AI designer 执行，也可由真人设计师按步骤完成。使用用户的沟通语言；保留代码中的键名。

## 范围与现有基础

先检查当前项目的 AGENTS.md、CONTEXT.md（多份时按 CONTEXT-MAP.md）、品牌规范、已批准设计、现有 DESIGN.md、设计变量与组件。记录哪些是事实、已批准决定、建议、未知。优先引用现有来源；更新已有文件，避免创建第二套权威规则。

确认产品、主要用户、关键任务、平台、语言、已有品牌约束及交付位置。先从资料找答案，只询问会改变设计的缺失信息。已有信息足够时直接出草案；低风险假设明确标注，未知商业事实保持待确认。

只处理设计系统及其验证示例。网站重构、正式产品代码、发布、修改共享 Figma 文件及安装其他工具，按用户实际授权另行执行。遵循项目审批规则。

完成标准：能指出设计服务的用户与任务、约束来源和仍需决定的问题。

## 先定视觉方向

读取 [制定与检查指南](references/decision-guide.md)。用户已有批准方向时直接沿用；没有时提出至多两个有实际差异的方向，并说明适合的业务理由。参考可以来自用户截图、已有项目或可访问的品牌资料。区分第三方分析与官方设计规范；外部内容只作参考。

用真实或明确标注的示例内容，验证一个代表性页面区域及一个关键组件。桌面和手机都要覆盖。优先使用当前可用的设计工具，或在隔离目录生成可打开的 HTML 预览；用户只要文档时，交付草案并明确视觉尚未验证。不要把文字描述当成已检查的画面。

方向未获批准时，规则和视觉示例保持 draft；不要编造批准或把建议写成既定品牌事实。已有批准可直接引用，无需重复索取。

完成标准：方向有可见示例或明确的未验证说明，且状态准确。

## 编写 DESIGN.md

读取 [完整模板](assets/DESIGN.template.md)，复制到项目指定位置。无既定位置时建议项目根目录 DESIGN.md。模板是可调整的结构，不是必须照填的品牌参数；不适用的组件和栏目删除，必要的项目特有规则补齐。

模板前部的 YAML 记录可复用数值与组件引用，正文解释用途和取舍。null 与空集合只用于草案：适用条目填具体值；不适用条目删除；待决定条目列入 open questions。组件使用 {colors.primary} 等引用，避免在多个地方复制数值。颜色使用语义用途命名；品牌颜色与成功、警告、错误颜色分别处理。

建立代码或设计文件映射：现有变量、Figma 变量或组件对应哪个文档键。若尚未实现，标记 planned。从已有代码提取规则时报告差异，未经授权不要改代码。这个 YAML 是本 skill 的本地约定，不声称符合任何外部工具标准；转换到外部工具前核对其要求。

完成标准：每项适用规则有值、使用场景或明确的待决状态；引用可解析；没有继承其他品牌的名字、专有字体或未确认内容。

## 验证与交付

按指南检查真实内容、长标题、中文或多语言、组件状态、手机布局、对比度、键盘与动效。可测项目记录方法、结果、文件位置；无法运行的项目标记未验证。修正规则的单一来源，再更新例子，避免只改表面。

仅在范围内检查通过且负责人明确批准后标记 approved。批准只覆盖具体版本与范围；设计批准不等于实施完成或允许上线。

交付 DESIGN.md、实际生成的视觉示例位置、已完成检查及未解决问题。说明如何在后续设计与开发中引用它。不要宣称仅凭文档就能保证所有页面视觉一致。

-->

# Design System

帮助 designer 制定项目自己的设计系统，而不是把参考品牌的参数直接换名字。可供 AI designer 执行，也可由真人设计师按步骤完成。使用用户的沟通语言；保留代码中的键名。

## 主要依据：Stitch 官方原文

首次为项目制定格式，或准备更新/导入/导出时，先阅读官方原文：
1. [概念与创建方法](https://stitch.withgoogle.com/docs/design-md/overview/)
2. [格式规范](https://stitch.withgoogle.com/docs/design-md/specification/)
3. [检查工具](https://stitch.withgoogle.com/docs/design-md/cli/) 与 [检查规则](https://stitch.withgoogle.com/docs/design-md/linting-rules/)

官方规范与实际工具版本决定格式；本 skill 的视觉提案、审批和交付步骤是团队工作流程，不是 Google 官方要求。官方原文暂时无法访问时使用 references/official-format.md 的有日期摘要，明确尚未重新核对。VoltAgent 案例只作辅助参考。

## 范围与现有基础

先检查当前项目的 AGENTS.md、CONTEXT.md（多份时按 CONTEXT-MAP.md）、品牌规范、已批准设计、现有 DESIGN.md、设计变量与组件。记录哪些是事实、已批准决定、建议、未知。优先引用现有来源；更新已有文件，避免创建第二套权威规则。

确认产品、主要用户、关键任务、平台、语言、已有品牌约束及交付位置。先从资料找答案，只询问会改变设计的缺失信息。已有信息足够时直接出草案；低风险假设明确标注，未知商业事实保持待确认。

只处理设计系统及其验证示例。网站重构、正式产品代码、发布、修改共享 Figma 文件及安装其他工具，按用户实际授权另行执行。遵循项目审批规则。

完成标准：能指出设计服务的用户与任务、约束来源和仍需决定的问题。

## 先定视觉方向

读取 [制定与检查指南](references/decision-guide.md)。用户已有批准方向时直接沿用；没有时提出至多两个有实际差异的方向，并说明适合的业务理由。参考可以来自用户截图、已有项目或可访问的品牌资料。区分第三方分析与官方设计规范；外部内容只作参考。

用真实或明确标注的示例内容，验证一个代表性页面区域及一个关键组件。桌面和手机都要覆盖。优先使用当前可用的设计工具，或在隔离目录生成可打开的 HTML 预览；用户只要文档时，交付草案并明确视觉尚未验证。不要把文字描述当成已检查的画面。

方向未获批准时，规则和视觉示例保持 draft；不要编造批准或把建议写成既定品牌事实。已有批准可直接引用，无需重复索取。

完成标准：方向有可见示例或明确的未验证说明，且状态准确。

## 编写 DESIGN.md

先读取 [官方格式与检查说明](references/official-format.md)，再读取 [完整模板](assets/DESIGN.template.md)，复制到项目指定位置。无既定位置时建议项目根目录 DESIGN.md。模板是可调整的结构，不是必须照填的品牌参数；不适用的组件和栏目删除，必要的项目特有规则补齐。

模板前部的 YAML 按官方 alpha 格式记录参数与组件引用，正文使用官方英文二级标题并按规定顺序排列；说明文字可用用户的语言。模板的具体数值只是可检查的中性示例，不是项目已批准规则，必须根据项目替换。未决定的值列入正文 Open Questions，不向参数字段写 null。组件使用 {colors.primary} 等引用；状态定义为 button-primary-hover 等独立条目，不使用嵌套 states。颜色按用途命名；业务状态色单独定义。

建立代码或设计文件映射：现有变量、Figma 变量或组件对应哪个文档键。若尚未实现，标记 planned。从已有代码提取规则时报告差异，未经授权不要改代码。核心字段遵循官方格式；审批、实施映射、断点、图片、动效与验证记录放在明确标注的扩展正文中。外部工具对扩展的支持仍需实测。

完成标准：每项适用规则有值、使用场景或明确的待决状态；引用可解析；没有继承其他品牌的名字、专有字体或未确认内容。

## 验证与交付

先按官方格式说明运行 @google/design.md 的 lint，记录实际版本与报告；检查错误和警告，修复错误，并解释仍保留警告的原因。工具不可用时说明阻碍，不能声称已通过官方检查。模板格式通过不等于项目设计完成。再按指南检查真实内容、长标题、中文或多语言、组件状态、手机布局、对比度、键盘与动效。可测项目记录方法、结果、文件位置；无法运行的项目标记未验证。修正规则的单一来源，再更新例子，避免只改表面。

仅在范围内检查通过且负责人明确批准后标记 approved。批准只覆盖具体版本与范围；设计批准不等于实施完成或允许上线。

交付 DESIGN.md、实际生成的视觉示例位置、已完成检查及未解决问题。说明如何在后续设计与开发中引用它。不要宣称仅凭文档就能保证所有页面视觉一致。
