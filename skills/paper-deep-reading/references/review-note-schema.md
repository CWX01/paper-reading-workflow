# Review Article Deep Reading Note Schema

Use this schema when creating or revising a review article note. Keep headings stable so notes remain comparable across papers.

## Template

```markdown
# Paper Title

## Metadata

- Title:
- Authors:
- Institution:
- Publication:
- Year:
- Scope / Subfield:
- Tags:
- Status: DONE

## TL;DR

用 2-4 句话说明：综述覆盖的领域、核心分类框架或主线、最重要的结论或趋势、为什么对当前研究线有价值。

## 毒舌评论

用一小段话或 2-3 个 bullet 给出够狠的直接判断：这篇综述到底有多大价值、最可能被高估的地方是什么、最大短板或最脆弱假设在哪里。不能写成摘要，必须比 TL;DR 更尖锐；但每个狠话都要有论文事实支撑，不确定就明确说"不确定"。

## Research Question

- 研究对象：
- 小领域范围：
- 综述问题：
- 为什么重要：
- 综述边界：

## Motivation and Basic Idea

- Motivation：
- 综述的组织逻辑（分类框架 / 时间线 / 问题分解）：
- 这个组织方式如何回应 motivation：
- 我的判断：

## Background

- 背景：
- 问题：
- Gap：

## [综述正文各章节]

> 按原文章节结构展开，每节一个子标题，使用原文章节编号。
> 详略程度由章节重要性决定：原理和方法类章节详细论述，应用和案例类章节简要总结。

## Key Artifacts

只保留关键表格内容，图片只记录编号与标题，用户需要时自行查阅原文。

- 关键表：
- 关键图标题：
- 这些证据分别支撑哪些结论：

## Findings

只记录跨章节的重要结论，标注具体章节号。

- 发现 1（§X.X）：
- 发现 2（§X.X）：
- 发现 3（§X.X）：

## Strengths

- 综述最有说服力的地方：
- 覆盖范围、分类框架或分析深度的优势：
- 对该领域的有效推进或整合：

## Limitations

- 覆盖范围或时效性的限制：
- 分类框架或组织方式的不足：
- 可能遗漏的重要方向或偏见：

## My Takeaways

- 对后续研究的启发：
- 可复用的方法或框架：
- 可能的后续问题：

## Open Questions

- 
```

## Body Section Checklist

Each body section（对应综述正文的一个章节或子章节）应按以下 checklist 记录，根据章节重要性决定详略：

- **核心论点**：本节在论证什么观点或回答什么问题
- **关键概念 / 定义 / 原理**：本节引入或讨论的核心术语、概念，需要详细描述
- **分类体系**：如果本节涉及分类，记录分类维度和各类别
- **主要方法类别**：每类方法的核心原理、适用场景、优缺点
- **重要对比**：不同方法/观点之间的关键差异
- **开放问题**：作者指出的未解决问题或未来方向
- **重要表格**：记录表格内容（分类对比表、方法总结表等）
- **重要图表标题**：仅记录标题，不展开内容

**详略原则**：
- 原理和方法类章节：详细论述核心机制、设计取舍、关键公式
- 应用和案例类章节：简要总结应用场景、代表性工作、效果
- 对比和评价类章节：重点记录对比维度和结论

## Notes

- If a section does not apply, keep the heading and write `N/A` or `TBD` with a short reason.
- Use an internal critical analysis step: scope, coverage, organization quality, timeliness, bias, and evidence. Do not add a separate critical-review section. Convert that judgment into `Strengths`, `Limitations`, and `My Takeaways`.
- 不记录引用的具体论文，用户需要时自行查阅原文。
- 综述中的关键表格（分类对比表、方法总结表等）应完整记录，因为这些是综述的核心价值。
- Findings 只记录跨章节的重要结论，并标注具体章节号（如 §3.2），方便回溯。
