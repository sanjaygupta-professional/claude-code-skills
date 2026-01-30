---
name: viz-business
description: "Visualization sub-skill for business/strategy books. Provides genre-specific Mermaid diagram strategies, content structures, color palettes, and chapter analysis templates optimized for frameworks, competitive analysis, growth models, and strategic decision-making content."
---

# Visualization Sub-Skill: Business / Strategy Books

This sub-skill is loaded by parent companion skills (visual, dual, adaptive) when the book is classified as BUSINESS genre during Phase 1.

---

## A. Visualization Strategy

### Diagram Quantity
- **3-6 diagrams per chapter** (frameworks and case studies drive quantity)

### Primary Diagram Types
| Diagram Type | Best For |
|-------------|----------|
| `flowchart` | Decision trees, value chains, process models, strategy flows |
| `mindmap` | Framework decomposition, pillar breakdowns, strategy landscapes |
| `quadrantChart` | 2x2 matrices (growth-share, effort-impact, urgency-importance) |
| `xychart-beta` | Trend lines, growth curves, performance metrics over time |
| `flowchart` with subgraphs | Competitive landscapes, market comparisons, org structures |

### Secondary Diagram Types
| Diagram Type | Best For |
|-------------|----------|
| `pie` | Market share, resource allocation, portfolio distribution |
| `gantt` | Implementation timelines, roadmaps, phased rollouts |
| `sankey-beta` | Value flows, resource flows, customer journeys |
| `flowchart LR` | Linear processes, pipeline stages, funnel models |

### Visual Narrative Arc: **Framework-Apply**
Each chapter's diagrams should follow this progression:
1. **Framework mindmap** — decompose the chapter's core framework or model into its components
2. **Structured diagram** — formalize the framework as a flowchart, quadrant, or process
3. **Case study application** — show the framework applied to a specific example from the chapter
4. **Connection to thesis** — link this chapter's framework to the book's overarching argument

### Color Palette
| Role | Color | Hex | Usage |
|------|-------|-----|-------|
| Growth / Opportunity | Green | `#c8e6c9` | Revenue, scaling, positive outcomes |
| Risk / Threat | Orange | `#ffe0b2` | Risks, challenges, disruption forces |
| Analysis / Strategy | Blue | `#bbdefb` | Analytical frameworks, data-driven insights |
| Competition | Pink | `#f8bbd0` | Competitors, market forces, rivals |
| Innovation | Purple | `#e1bee7` | New ideas, disruption, blue ocean moves |
| Current State | Yellow | `#fff9c4` | Status quo, existing conditions, baseline |

### Complexity Cap
- **16 nodes maximum** without subgraphs
- Use subgraphs to group related nodes (e.g., internal vs. external factors)
- Prefer labeled edges over additional nodes for relationships

---

## B. Content Strategy

### Section Structure
Each chapter's companion content should follow this pattern:
1. **Strategic Question** — What business question does this chapter answer?
2. **The Framework** — What model, matrix, or mental model is introduced?
3. **In Practice** — How is the framework applied through case studies or examples?
4. **Your Situation** — Prompts for the reader to apply the framework to their own context

### Callout Types
Use these Starlight callout types consistently:
- `:::tip[Framework]` — Named frameworks, models, or matrices being introduced
- `:::note[Case Study]` — Real-world examples and business stories from the chapter
- `:::tip[Action Item]` — Concrete steps the reader can take
- `:::caution[Common Mistake]` — Strategic errors or misapplications of the framework

### Chapter End Section
Each chapter companion page should end with:

**Framework Cheat Sheet** + **Application Checklist**
```markdown
## Framework Cheat Sheet

| Component | Definition | Key Question |
|-----------|-----------|-------------|
| [Element 1] | [Definition] | [Question to ask] |
| [Element 2] | [Definition] | [Question to ask] |

## Application Checklist

- [ ] Can I identify which quadrant/category my situation falls into?
- [ ] Have I considered the key trade-offs this framework highlights?
- [ ] Do I have a clear next step based on this analysis?
```

---

## C. Chapter Analysis Template

When analyzing each chapter during Phase 1, answer these 8 questions to guide visualization:

```
BUSINESS CHAPTER ANALYSIS — Chapter [N]: [Title]

1. STRATEGIC QUESTION: What business problem or decision does this chapter address?
   (Growth strategy / competitive positioning / resource allocation / innovation)

2. NAMED FRAMEWORK: Does the chapter introduce a named framework, model, or matrix?
   (e.g., Porter's Five Forces, BCG Matrix, Jobs-to-be-Done, Blue Ocean)
   If yes, what are its components?

3. MATRIX OR QUADRANT: Can the chapter's key insight be expressed as a 2x2 matrix?
   (What are the two axes? What goes in each quadrant?)

4. PROCESS: Does the chapter describe a step-by-step process or sequence?
   (Implementation steps, decision tree, evaluation process)

5. CASE STUDIES: What real-world examples or companies are discussed?
   (Company name, what they did, outcome, lesson)

6. METRICS: Does the chapter reference quantitative data, KPIs, or trends?
   (Revenue numbers, market share, growth rates, time series)

7. COMPETITIVE DYNAMICS: Does the chapter contrast strategies, companies, or approaches?
   (Side-by-side comparisons, market positioning, competitive moves)

8. VISUAL DENSITY (1-5): How diagram-heavy should this chapter be?
   1 = Conceptual/narrative (1-2 diagrams)
   3 = Framework-heavy (3-4 diagrams)
   5 = Data-rich with multiple models (5-6 diagrams)
```

---

## D. Multi-Genre Handling

When a chapter is tagged with BUSINESS as its secondary genre (primary is something else):
- Use `mindmap` for any framework decomposition within the chapter
- Use `quadrantChart` if the chapter introduces a 2x2 matrix
- Apply the business color palette only to business-related diagram nodes
- Keep the primary genre's visual arc for the chapter's overall structure
- Limit business diagrams to sections that present frameworks or strategic analysis
