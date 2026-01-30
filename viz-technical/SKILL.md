---
name: viz-technical
description: "Visualization sub-skill for technical/engineering books. Provides genre-specific Mermaid diagram strategies, content structures, color palettes, and chapter analysis templates optimized for software architecture, data pipelines, API interactions, and system design content."
---

# Visualization Sub-Skill: Technical / Engineering Books

This sub-skill is loaded by parent companion skills (visual, dual, adaptive) when the book is classified as TECHNICAL genre during Phase 1.

---

## A. Visualization Strategy

### Diagram Quantity
- **3-7 diagrams per chapter** (scales with complexity of the chapter's technical content)

### Primary Diagram Types
| Diagram Type | Best For |
|-------------|----------|
| `flowchart` | Data pipelines, decision logic, algorithms, control flow |
| `sequenceDiagram` | API interactions, request/response flows, protocol handshakes |
| `classDiagram` | Type hierarchies, interface relationships, module structure |
| `erDiagram` | Data models, schema relationships, entity mappings |
| `architecture` | Infrastructure topology, cloud services, deployment diagrams |
| `block-beta` | Layered architectures, stack diagrams, protocol layers |

### Secondary Diagram Types
| Diagram Type | Best For |
|-------------|----------|
| `flowchart TB` with subgraphs | Component decomposition, package structure |
| `stateDiagram` | State machines, lifecycle transitions, connection states |
| `mindmap` | Technology landscape overview, chapter concept summary |
| `gitgraph` | Branching strategies, version evolution |

### Visual Narrative Arc: **Layer-Down**
Each chapter's diagrams should follow this progression:
1. **High-level architecture** — system-level or module-level view (architecture, block-beta, or flowchart with subgraphs)
2. **Component-level** — individual components and their responsibilities (classDiagram, erDiagram)
3. **Interaction/sequence** — how components communicate at runtime (sequenceDiagram, flowchart)
4. **Synthesis** — consolidated view or decision framework (mindmap or flowchart)

### Color Palette
| Role | Color | Hex | Usage |
|------|-------|-----|-------|
| Data / Input | Blue | `#bbdefb` | Data sources, inputs, read operations |
| Success / Output | Green | `#c8e6c9` | Successful paths, outputs, write results |
| Processing | Orange | `#ffe0b2` | Transformations, middleware, compute steps |
| External APIs | Purple | `#e1bee7` | Third-party services, external dependencies |
| Error paths | Red | `#ffcdd2` | Error handling, failure modes, exceptions |
| Infrastructure | Gray | `#e0e0e0` | Servers, queues, databases, network |

### Complexity Cap
- **20 nodes maximum** per diagram
- If a system has more than 20 components, split into multiple diagrams at different abstraction levels
- Prefer subgraphs to group related nodes rather than adding more top-level nodes

---

## B. Content Strategy

### Section Structure
Each chapter's companion content should follow this pattern:
1. **The Problem** — What technical challenge does this chapter address?
2. **The Solution** — What architecture, pattern, or approach does it propose?
3. **Trade-offs** — What are the costs, limitations, and alternatives?
4. **When to Use** — Decision criteria for applying this in practice

### Callout Types
Use these Starlight callout types consistently:
- `:::tip[Design Decision]` — Key architectural choices and their rationale
- `:::caution[Trade-off]` — Performance vs. simplicity, consistency vs. availability, etc.
- `:::danger[Anti-pattern]` — Common mistakes and why they fail
- `:::note[Implementation Note]` — Practical tips for applying the concept

### Chapter End Section
Each chapter companion page should end with:

**Decision Checklist**
A bulleted checklist of questions the reader should be able to answer after understanding the chapter:
```markdown
## Decision Checklist

- [ ] Can I identify which components are stateful vs. stateless?
- [ ] Do I know when to use synchronous vs. asynchronous communication?
- [ ] Can I articulate the trade-off being made and why?
```

---

## C. Chapter Analysis Template

When analyzing each chapter during Phase 1, answer these 9 questions to guide visualization:

```
TECHNICAL CHAPTER ANALYSIS — Chapter [N]: [Title]

1. SYSTEM SCOPE: What is the boundary of the system or subsystem discussed?
   (Single service / distributed system / full stack / algorithm)

2. ARCHITECTURE DECISIONS: What key design choices are presented?
   (List each decision and alternatives considered)

3. DATA FLOW: What data enters, transforms, and exits the system?
   (Input sources → processing stages → output destinations)

4. COMPONENT RELATIONSHIPS: What are the major components and how do they relate?
   (Dependencies, interfaces, inheritance, composition)

5. STATE TRANSITIONS: Does the chapter describe state changes?
   (Connection states, order lifecycle, deployment stages)

6. INTERACTION PATTERNS: Are there multi-step interactions between actors?
   (Client-server, pub-sub, request-response, event-driven)

7. INFRASTRUCTURE TOPOLOGY: Does the chapter describe deployment or infrastructure?
   (Servers, databases, caches, queues, load balancers)

8. ANTI-PATTERNS: Does the chapter warn against specific approaches?
   (Common mistakes, performance pitfalls, security risks)

9. VISUAL DENSITY (1-5): How diagram-heavy should this chapter be?
   1 = Conceptual/lightweight (1-2 diagrams)
   3 = Moderate architecture (3-4 diagrams)
   5 = Complex system design (5-7 diagrams)
```

---

## D. Multi-Genre Handling

When a chapter is tagged with TECHNICAL as its secondary genre (primary is something else):
- Use `flowchart` and `sequenceDiagram` for any technical content within the chapter
- Apply the technical color palette only to technical diagram nodes
- Keep the primary genre's visual arc for the chapter's overall structure
- Limit technical diagrams to the specific sections that warrant them
