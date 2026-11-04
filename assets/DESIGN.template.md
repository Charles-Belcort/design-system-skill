---
version: alpha
name: Project Design Draft
description: Neutral example values for replacement after project-specific design review.
colors:
  primary: "#1f2937"
  on-primary: "#ffffff"
  primary-hover: "#374151"
  primary-active: "#111827"
  surface: "#ffffff"
  on-surface: "#1f2937"
typography:
  headline-lg:
    fontFamily: system-ui
    fontSize: 40px
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: -0.02em
  body-md:
    fontFamily: system-ui
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0em
  label-md:
    fontFamily: system-ui
    fontSize: 16px
    fontWeight: 600
    lineHeight: 1.25
    letterSpacing: 0em
rounded:
  sm: 4px
  md: 8px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 48px
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.sm}"
    padding: "{spacing.md}"
    height: 48px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.sm}"
    padding: "{spacing.md}"
    height: 48px
  button-primary-active:
    backgroundColor: "{colors.primary-active}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.sm}"
    padding: "{spacing.md}"
    height: 48px
  card:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: "{spacing.lg}"
---

# Project Design System

## Overview
**草案模板，尚未获得项目批准。** YAML 中是便于检查格式的中性示例值，不代表品牌推荐或已完成设计；请按项目替换名称、描述、参数和正文。

填写目标用户、关键任务、平台、语言、品牌气质、适用页面与非目标。每条设计原则配一个实际使用场景。

## Colors
说明每个颜色的用途与限制。数值以 YAML 为准；需要更多背景、文字或状态色时添加相应参数和实际组件配对。记录实际组合的对比度结果，不能把模板通过当作项目通过。

## Typography
说明标题、正文、标签的职责，以及字体来源、使用权限、语言覆盖、替代字体和加载策略。用长标题、中文、数字与手机正文验证后调整示例层级。

## Layout
说明 spacing 的使用规则、页面最大宽度、页边距、排列方式和断点。手机变化按内容需求制定，填写具体条件与行为，避免只写“自适应”。

## Elevation & Depth
说明通过背景差异、边框或阴影表达层次的方法。具体阴影和边框规则在此记录，不伪装成核心组件属性。保持与实际示例一致。

## Shapes
说明 rounded 各级的使用位置、图片边缘处理与允许例外。

## Components
逐项填写实际组件的用途、结构、参数引用与示例位置。模板展示扁平的 button-primary、button-primary-hover、button-primary-active 条目；其他适用状态照此添加。说明状态共用哪些基础规则，不假定工具自动继承。

焦点轮廓、禁用原因、加载反馈、错误提示、键盘顺序、触屏目标及长内容行为在本节说明。输入框与数据组件按实际需要增加。

## Do's and Don'ts
填写项目可执行的使用规则及反例；用真实组件说明什么情况应使用哪种样式。不要把参考品牌的限制直接当成本项目要求。

## Project Extensions
以下章节是团队交付约定，不是 Stitch 必填字段。仅保留适用内容。

## Sources and Decisions
记录品牌文件、官方规范、参考画面及具体借鉴点。区分现有事实、已批准决定、提案和未知；注明参考内容的署名与许可。

## Responsive Behavior
记录断点、实际测试尺寸、导航收起、卡片排列、表格溢出、固定按钮避让、字体调整与缩放表现。补足 Layout 的项目细节。

## Imagery and Iconography
填写图片风格、比例、裁切焦点、背景、缺图、替代文字、图标来源与尺寸。区分真实产品图与概念示意。

## Motion and Accessibility
按实际组件填写动效目的、触发条件、时长、缓动和减少动态效果的替代方案。记录对比度、键盘焦点、触屏与阅读顺序检查；结构检查不等于全面可访问性认证。

## Implementation Mapping
| 文档键 | 设计变量或组件 | 代码变量或组件 | 状态与来源 |
| --- | --- | --- | --- |

每项选择权威数值来源，其他位置引用或生成。planned 不等于已实现；记录手动同步方式。

## Validation
| 检查范围 | 工具版本／方法与尺寸 | 结果 | 文件或链接 |
| --- | --- | --- | --- |

记录官方 lint 的错误、警告及处置，另行记录桌面、手机、组件状态、长文案和多语言样张。未运行的检查标明未验证。

## Open Questions
| 待决问题 | 影响范围 | 负责人／决定 | 状态 |
| --- | --- | --- | --- |

未决定的设计值在此登记，避免把 null 写入核心参数。未解决值不作为获批实施依据。

## Approval and History
设计版本与状态：待填写，初始为 draft。记录批准人、日期、范围、具体版本及可检查的批准记录。此处设计版本与 YAML 的格式版本 alpha 分开维护。设计批准不等于上线授权。
