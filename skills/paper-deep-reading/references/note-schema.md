# Deep Reading Note Schema

Use this schema when creating or revising a paper note. Keep headings stable so notes remain comparable across papers.

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

用 2-4 句话说明：论文解决的问题、核心方法、最重要结论、为什么对当前研究线有价值。

## 毒舌评论

用一小段话或 2-3 个 bullet 给出够狠的直接判断：这篇论文到底有多大价值、最可能被高估的地方是什么、最大短板或最脆弱假设在哪里。不能写成摘要，必须比 TL;DR 更尖锐；但每个狠话都要有论文事实支撑，不确定就明确说“不确定”。

## Research Question

- 研究对象：
- 小领域范围：
- 具体问题：
- 为什么重要：
- 论文边界：

## Motivation and Basic Idea

- Motivation：
- Basic idea：
- 这个 idea 如何回应 motivation：
- 作者给出的证据：
- 我的判断：

## Background

- 背景：
- 问题：
- Gap：

## Method

- 核心思路：
- 核心思路是怎么想到的：
- 从 motivation 到 method 的逻辑链：
- 关键设计取舍：
- 为什么不是更直接 / 更简单的方案：
- 系统流程或算法步骤：
- 关键定义 / 公式 / 不变量：
- 实现细节：

## Evaluation

- 实验思路：
- 评估指标：
- 主要结果：

## Key Artifacts

- 关键图：
- 关键表：
- 关键公式 / 定义 / 算法：
- 这些证据分别支撑哪些结论：

## Findings

- 发现 1：
- 发现 2：
- 发现 3：

## Strengths

- 论文最有说服力的地方：
- 方法、数据、实验或问题设定的优势：
- 相比已有工作的有效推进：

## Limitations

- 假设或适用范围等的限制：
- 复现性、成本等的不足：
- 在真实应用场景中可能失效的条件：

## My Takeaways

- 对后续研究的启发：
- 可复用的方法：
- 可能的后续问题：

## Open Questions

- 
```

If a section does not apply, keep the heading and write `N/A` or `TBD` with a short reason.

Use an internal critical analysis step: goal, prior practice, novelty, impact, risks, cost, and evidence. Do not add a separate critical-review section. Convert that judgment into `Strengths`, `Limitations`, and `My Takeaways`. When judging external impact or follow-up work, use sources retrieved in the current turn instead of memory.

When filling `Key Artifacts`, prefer the figures, tables, equations, algorithms, and definitions that carry the paper's core claims. Preserve notation accurately and explain what each artifact proves. If the user requests exhaustive notes, include every figure, table, and important equation.
