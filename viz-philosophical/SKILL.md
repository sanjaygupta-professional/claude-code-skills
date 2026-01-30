---
name: viz-philosophical
description: "Visualization sub-skill for philosophy/ideas books. Provides genre-specific Mermaid diagram strategies, content structures, color palettes, and chapter analysis templates optimized for argument structures, dialectical flows, concept decomposition, and intellectual lineage."
---

# Visualization Sub-Skill: Philosophy / Ideas Books

This sub-skill is loaded by parent companion skills (visual, dual, adaptive) when the book is classified as PHILOSOPHICAL genre during Phase 1.

---

## A. Visualization Strategy

### Diagram Quantity
- **2-5 diagrams per chapter** (quality over quantity; sparse diagrams are better for abstract ideas)

### Primary Diagram Types
| Diagram Type | Best For |
|-------------|----------|
| `mindmap` | Concept decomposition, term disambiguation, idea landscapes |
| `flowchart` with subgraphs | Argument structure: premises → conclusion, logical chains |
| `flowchart` | Dialectical flow: thesis → antithesis → synthesis |
| `quadrantChart` | Positioning ideas on 2 axes (e.g., individual vs. collective, empirical vs. rational) |

### Secondary Diagram Types
| Diagram Type | Best For |
|-------------|----------|
| `stateDiagram` | Conceptual state changes, transformations of understanding |
| `flowchart LR` | Intellectual lineage, influence chains between thinkers |
| `flowchart TB` with subgraphs | Schools of thought, philosophical traditions |
| `mindmap` (nested) | Key distinctions and their sub-categories |

### Visual Narrative Arc: **Dialectical**
Each chapter's diagrams should follow this progression:
1. **Concept landscape mindmap** — map the key ideas, terms, and distinctions in the chapter
2. **Argument structure** — formalize the chapter's central argument (premises → conclusion)
3. **Tensions / oppositions** — show the dialectical tension (thesis vs. antithesis, competing views)
4. **Synthesis** — the resolution, reconciliation, or new understanding the chapter reaches

### Color Palette
| Role | Color | Hex | Usage |
|------|-------|-----|-------|
| Claims / Thesis | Indigo | `#c5cae9` | Central claims, main arguments, propositions |
| Counterarguments | Pink | `#f8bbd0` | Objections, antitheses, opposing views |
| Synthesis | Green | `#c8e6c9` | Resolutions, reconciliations, new understanding |
| Evidence | Amber | `#ffe0b2` | Examples, thought experiments, empirical support |
| Meta-concepts | Purple | `#e1bee7` | Meta-level ideas, frameworks about frameworks |
| Historical context | Teal | `#b2dfdb` | Historical figures, intellectual traditions, lineage |

### Complexity Cap
- **14 nodes maximum** per diagram (sparse is better for abstract ideas)
- Argument diagrams should have 3-6 premises maximum leading to a conclusion
- Prefer depth (deeper chains) over breadth (many parallel branches)

---

## B. Content Strategy

### Section Structure
Each chapter's companion content should follow this pattern:
1. **The Question** — What philosophical question or problem does this chapter address?
2. **The Argument** — What is the chapter's central argument, step by step?
3. **The Tensions** — What counterarguments, objections, or unresolved tensions exist?
4. **The Implications** — What follows if the argument is accepted? What changes?

### Callout Types
Use these Starlight callout types consistently:
- `:::tip[Key Distinction]` — Important conceptual distinctions (e.g., "knowledge vs. belief")
- `:::note[Thought Experiment]` — Hypothetical scenarios used to test ideas
- `:::caution[Unstated Assumption]` — Hidden premises or assumptions the argument relies on
- `:::note[Intellectual Context]` — Historical or philosophical context for the ideas

### Chapter End Section
Each chapter companion page should end with:

**Takeaway in One Sentence** + **Questions This Chapter Raises**
```markdown
## Takeaway in One Sentence

> [A single sentence capturing the chapter's core insight — the one idea the reader should carry forward.]

## Questions This Chapter Raises

1. [A genuine philosophical question the chapter opens but doesn't fully resolve]
2. [A question about how this idea applies to a different domain]
3. [A question that connects this chapter to a later chapter or broader theme]
```

---

## C. Chapter Analysis Template

When analyzing each chapter during Phase 1, answer these 9 questions to guide visualization:

```
PHILOSOPHICAL CHAPTER ANALYSIS — Chapter [N]: [Title]

1. CENTRAL QUESTION: What philosophical question is the chapter trying to answer?
   (What is X? Is X possible? Should we X? How does X relate to Y?)

2. THESIS: What is the chapter's main claim or position?
   (State in one clear sentence)

3. ARGUMENT STRUCTURE: What are the premises that support the thesis?
   (P1: ... P2: ... P3: ... Therefore: ...)

4. KEY DISTINCTIONS: What conceptual distinctions does the chapter introduce?
   (X vs. Y, where the difference matters because...)

5. THOUGHT EXPERIMENTS: Does the chapter use hypothetical scenarios?
   (Describe each and what it's meant to demonstrate)

6. OBJECTIONS: What counterarguments or objections does the chapter address?
   (Or: what objections SHOULD be raised that the author doesn't address?)

7. INTELLECTUAL CONTEXT: What thinkers, traditions, or schools does this draw from?
   (Influences, predecessors, interlocutors)

8. CONCEPT INVENTORY: List all important terms/concepts introduced or redefined.
   (Term: definition or the author's specific usage)

9. VISUAL DENSITY (1-5): How diagram-heavy should this chapter be?
   1 = Abstract meditation, minimal structure (1-2 diagrams)
   3 = Clear argument with distinctions (2-3 diagrams)
   5 = Complex multi-layered argument (4-5 diagrams)
```

---

## D. Multi-Genre Handling

When a chapter is tagged with PHILOSOPHICAL as its secondary genre (primary is something else):
- Use `mindmap` for concept decomposition within the chapter
- Use `flowchart` for any argument structure (premises → conclusion)
- Apply the philosophical color palette only to philosophical diagram nodes
- Keep the primary genre's visual arc for the chapter's overall structure
- Limit philosophical diagrams to sections that present arguments or define concepts
