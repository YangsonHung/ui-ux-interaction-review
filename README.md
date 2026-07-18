# UI/UX 交互逻辑与状态链审查专家

**中文** | [English](README.en.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) [![Skill](https://img.shields.io/badge/Agent%20Skill-UI%2FUX%20Review-1f6feb)](skills/zh-cn/ui-ux-interaction-review-cn/SKILL.md)

面向 AI 编程助手的 UI/UX 交互审查技能。它将界面交互视为状态机，系统识别控制权不清、状态冲突、反馈缺失与认知负荷问题，并输出最佳体验与低成本稳健两套优化方案。

## 能力

- 解构 UI 区域的核心任务与组件控制关系
- 穷举状态组合，定位信息断层与操作断层
- 审查文案、视觉隐喻与交互层级带来的认知摩擦
- 按固定结构给出渐进式呈现方案和低成本改造方案

## 适用场景

- 开关联动 Tab 或列表
- 自动/手动模式切换
- 单选、多选与嵌套选择
- 条件显隐、表单联动和状态设计评审
- UI 截图、原型图或交互流程走查

## 快速开始

安装中文技能后，直接把 UI 截图、原型图或交互描述交给兼容的 Agent；也可以明确调用：

```text
$ui-ux-interaction-review-cn 审查这个自动/手动模式与模型列表的联动逻辑。
```

审查结果固定包含：现状诊断、最佳体验方案、低成本稳健方案，以及可选的微交互建议。

## 项目结构

```
skills/
├── en/
│   └── ui-ux-interaction-review/
│       └── SKILL.md
└── zh-cn/
    └── ui-ux-interaction-review-cn/
        └── SKILL.md
```

- [`skills/zh-cn/ui-ux-interaction-review-cn/SKILL.md`](skills/zh-cn/ui-ux-interaction-review-cn/SKILL.md)：中文技能定义，默认入口
- [`skills/en/ui-ux-interaction-review/SKILL.md`](skills/en/ui-ux-interaction-review/SKILL.md)：英文技能定义

## 安装

推荐使用 `skills` 安装器：

```bash
# 安装中文技能
npx skills add YangsonHung/ui-ux-interaction-review --skill ui-ux-interaction-review-cn

# 使用 pnpm
pnpm dlx skills add YangsonHung/ui-ux-interaction-review --skill ui-ux-interaction-review-cn
```

安装英文技能：

```bash
npx skills add YangsonHung/ui-ux-interaction-review --skill ui-ux-interaction-review
```

查看仓库内可安装的技能：

```bash
npx skills add YangsonHung/ui-ux-interaction-review --list
```

也可以手动安装：

```bash
# Codex：安装到用户级技能目录
cp -r skills/zh-cn/ui-ux-interaction-review-cn ~/.agents/skills/

# Claude Code：安装到用户级技能目录
cp -r skills/zh-cn/ui-ux-interaction-review-cn ~/.claude/skills/
```

将命令中的 `ui-ux-interaction-review-cn` 替换为 `ui-ux-interaction-review` 即可安装英文版本。

## 使用边界

- 本技能聚焦交互逻辑、状态反馈与认知负荷，不替代视觉品牌设计或可用性测试。
- 最佳体验方案与低成本方案均需明确说明状态变化、控制权和反馈方式。
- 设计结论应基于提供的界面、原型或业务规则；缺失关键信息时先列出待确认项。

## 参与贡献

欢迎修正触发条件、补充交互案例、完善中英文表述或改进输出结构。提交前请阅读：

- [贡献指南](CONTRIBUTING.md)
- [更新日志](CHANGELOG.md)
- [安全策略](SECURITY.md)
- [维护规范](AGENTS.md)

请通过 GitHub 的 [问题模板](.github/ISSUE_TEMPLATE) 报告缺陷或提出功能建议；提交代码时使用 [PR 模板](.github/PULL_REQUEST_TEMPLATE.md)。

## 路线图

- [ ] 补充常见 UI 模式的状态机示例
- [ ] 增加可复用的审查清单
- [ ] 建立真实界面案例库

## 许可证

本项目采用 [MIT License](LICENSE)。
