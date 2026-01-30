# Skill: Explain Simply (ELI10)

> *"Everything should be made as simple as possible, but not simpler."* — Albert Einstein

Transform complex content into clear, intuitive explanations that a smart 10-year-old can understand—without losing the essential meaning.

## Invocation

Use this skill when:
- User asks to "explain simply", "simplify", "ELI10", or "explain like I'm 10"
- User wants content transformed for broader accessibility
- Creating summaries that prioritize clarity over completeness
- Adding "simple explanation" sections to documentation

## The Smart 10-Year-Old Persona

**Who they are:**
- Curious and eager to understand
- Intelligent but without specialized knowledge
- Familiar with: school, family, friends, games, sports, basic technology
- Can follow logical reasoning when explained step-by-step
- Appreciates "why" something matters, not just "what" it is

**What they know:**
- Basic math and logic
- How teams and groups work (classroom, sports teams)
- Fair vs unfair, helpful vs unhelpful
- Goals and how to achieve them
- Technology basics (apps, games, websites)

**What they DON'T know:**
- Business jargon (stakeholders, KPIs, leverage, synergy)
- Corporate structures and politics
- Industry-specific terminology
- Abstract management concepts

---

## Transformation Principles

### 1. Replace Jargon with Everyday Words

| Instead of... | Say... |
|---------------|--------|
| Stakeholders | People who care about the project |
| Leverage | Use |
| Optimize | Make better |
| Iterate | Try again with improvements |
| Synergy | Working well together |
| Deliverables | Things you create and share |
| Bandwidth | Time and energy |
| ROI | Whether it's worth the effort |
| Pivot | Change direction |
| Scale | Grow bigger |

### 2. Use Relatable Metaphors

Draw from a 10-year-old's world:

| Complex Concept | Simple Metaphor |
|-----------------|-----------------|
| Product vision | A treasure map showing where you want to go |
| Strategy | Your game plan for winning |
| Empowered teams | Players who get to decide how to play, not just follow orders |
| Feature teams | Players who only do exactly what the coach says |
| OKRs | Goals + scoreboard to track progress |
| Technical debt | Messy room that gets harder to clean the longer you wait |
| MVP | A skateboard, not a car missing wheels |
| A/B testing | Trying two different things to see which works better |
| Roadmap | A plan for what you'll build and when |
| Sprint | A short race to finish something small |

### 3. Structure for Clarity

**The Simple Explanation Formula:**

```
1. HOOK: Start with something familiar
   "You know how...?" or "Imagine if..."

2. CORE IDEA: One sentence that captures the essence
   "The main idea is..."

3. WHY IT MATTERS: Connect to their world
   "This is important because..."

4. EXAMPLE: Make it concrete
   "It's like when..."

5. SO WHAT: The takeaway
   "So remember..."
```

### 4. Sentence Rules

- **Short sentences.** One idea per sentence.
- **Active voice.** "The team decides" not "Decisions are made by the team"
- **Concrete nouns.** "The designer" not "The relevant personnel"
- **Present tense.** "Teams work better when..." not "Teams would work better if..."
- **Questions engage.** "Have you ever tried to build something with friends?"

### 5. Avoid These Patterns

❌ "In order to facilitate the optimization of..."
✅ "To make things work better..."

❌ "It's important to note that stakeholders should be aligned..."
✅ "Everyone involved should agree on the plan..."

❌ "The paradigm shift necessitates a fundamental restructuring..."
✅ "This big change means we need to do things differently..."

---

## Output Format

When simplifying content, produce:

```markdown
## [Topic] — Simply Explained

**In one sentence:** [Core idea in ≤15 words]

**Imagine this:** [Relatable scenario or metaphor]

[2-4 paragraphs of simple explanation]

**The key thing to remember:** [One takeaway]
```

---

## Examples

### Example 1: Empowered Teams vs Feature Teams

**Original (complex):**
> "Empowered product teams are cross-functional groups given problems to solve rather than features to build. They have the autonomy to determine the best solution and are accountable for outcomes, not outputs. Feature teams, conversely, exist to serve stakeholders by implementing predetermined solutions with limited agency."

**Simplified (ELI10):**

> ## Empowered Teams vs Feature Teams — Simply Explained
>
> **In one sentence:** Empowered teams get to figure out HOW to solve problems; feature teams just follow instructions.
>
> **Imagine this:** You're building a treehouse with friends.
>
> In an **empowered team**, a grown-up says: "We need a place to hang out in the backyard. Figure out what would be awesome!" You and your friends brainstorm, maybe decide a treehouse is best, design it together, and build it. If something doesn't work, you fix it your way.
>
> In a **feature team**, a grown-up hands you exact blueprints and says: "Build this. Use these boards. Put the window here." You just follow the instructions—even if you think a different design would be better.
>
> Which sounds more fun? Which team do you think builds something they're proud of?
>
> **The key thing to remember:** Give people a problem to solve, not a list of instructions to follow.

### Example 2: OKRs (Objectives and Key Results)

**Original (complex):**
> "OKRs are a goal-setting framework where Objectives define qualitative goals and Key Results provide quantitative measures of progress. They create alignment across organizational levels while maintaining team autonomy in execution methodology."

**Simplified (ELI10):**

> ## OKRs — Simply Explained
>
> **In one sentence:** OKRs are goals plus a scoreboard to track if you're winning.
>
> **Imagine this:** You want to get better at basketball.
>
> Your **Objective** (the goal) is: "Become a great free-throw shooter."
>
> Your **Key Results** (the scoreboard) might be:
> - Make 7 out of 10 free throws by March
> - Practice free throws 20 minutes every day
> - Watch 3 videos about free-throw technique
>
> The Objective tells you WHERE you want to go. The Key Results tell you HOW you'll know you're getting there.
>
> **The key thing to remember:** A goal without a way to measure it is just a wish.

---

## Integration with Visual Companions

When adding ELI10 sections to book companions:

1. **Placement:** Add "Simply Explained" callout at the START of each chapter
2. **Length:** 100-200 words max
3. **Visuals:** Pair with simple diagrams when possible
4. **Tone:** Friendly, not condescending

### MDX Component Pattern

```mdx
import { Aside } from '@astrojs/starlight/components';

<Aside type="tip" title="Simply Explained">
**In one sentence:** [Core idea]

**Imagine this:** [Metaphor from a 10-year-old's world]

[1-2 short paragraphs]

**Remember:** [Key takeaway]
</Aside>
```

---

## Quality Checklist

Before finalizing a simple explanation:

- [ ] Could a 10-year-old read this aloud without stumbling?
- [ ] Are there any words that need a dictionary?
- [ ] Is there at least one concrete example or metaphor?
- [ ] Does it capture the ESSENTIAL idea (not every detail)?
- [ ] Would the original author say "Yes, that's what I meant"?
- [ ] Is it SHORT? (Aim for 50% fewer words than original)

---

## The Feynman Test

After writing, ask yourself:

> "If I had to teach this to a curious 10-year-old for 2 minutes, would they get it?"

If not, simplify further. True understanding reveals itself through simple explanation.

---

## Anti-Patterns to Avoid

1. **Dumbing down:** Removing meaning, not just jargon
2. **Condescension:** "This is super easy, even YOU can understand it!"
3. **Over-simplification:** Losing the core insight
4. **Kiddie language:** Using baby talk instead of clear language
5. **Too many metaphors:** One strong metaphor beats three weak ones

---

## When NOT to Simplify

Some content requires precision:
- Legal or compliance text
- Technical specifications
- Safety-critical instructions
- Direct quotes (attribute, then explain separately)

In these cases, provide the simple explanation AS WELL AS the precise original.
