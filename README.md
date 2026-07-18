# UI/UX 交互逻辑与状态链审查专家

**中文** | [English](README.en.md)

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

## 使用方式

将所需语言的技能目录复制到你的 Codex、Claude Code 或其他兼容 Agent 的技能目录：

```bash
# 中文版
cp -r skills/zh-cn/ui-ux-interaction-review-cn ~/.codex/skills/

# English version
cp -r skills/en/ui-ux-interaction-review ~/.codex/skills/
```

## 许可证

本项目采用 [MIT License](LICENSE)。
