---
name: analyze-memeplex
description: >
  Map the ecosystem of reinforcing ideas around a concept. Identifies which memeplex an idea
  belongs to, what ideas support or compete with it, and what mimetic desire dynamics drive
  its carriers. Use when you need to understand the ideological landscape before spreading an
  idea, or when you want to understand why an idea is thriving or dying. Trigger on: "What's
  the memeplex around this?", "What ideas compete with mine?", "Why does this idea keep coming
  back?", "Map the idea ecosystem", "What's reinforcing this narrative?"
---

# Analyze Memeplex

You are mapping the ecosystem of ideas surrounding a concept to understand its competitive landscape and reinforcement dynamics.

## What This Skill Does

Takes an idea (classified or raw) and maps:
1. **The memeplex it belongs to** — what cluster of reinforcing ideas does it live within?
2. **Competing memeplexes** — what rival idea-clusters oppose it?
3. **Mimetic desire dynamics** — who are the "models" (in Girard's sense) driving carriers to spread this?
4. **Reinforcement structure** — what other ideas, rituals, symbols, or institutions support this idea's survival?
5. **Vulnerability points** — where is the memeplex weak? What could disrupt it?

## Input/Output Contract

**Accepts:**
- An idea or concept (classified or raw)
- Optional: the network context (where is this idea circulating?)
- Optional: known competitors or opposing narratives

**Produces:**
- Memeplex map: the idea's position within its reinforcing cluster
- Competing memeplex map: rival idea-ecosystems
- Mimetic desire analysis: who are the models, what object is being competed for
- Reinforcement inventory: supporting ideas, rituals, institutions, symbols
- Vulnerability assessment: weak points in the memeplex structure
- Strategic implications: how this landscape affects your spread strategy

**Passes to:**
- design-strategy (informed by competitive landscape)
- craft-content (know what narratives to counter or leverage)
- identify-champions (find models who drive mimetic desire)
- build-immunity (understand what memeplexes threaten your network)
- reframe-idea (if your idea sits in a dying or hostile memeplex)

## Core Concepts

### Memeplexes (from source)

"A 'memeplex' is the institutionalized version of a meme, referring to a group of memes — such as a religion or political party — that reinforce each other via replication." — Nadia Asparouhova, citing Dawkins

Memeplexes are self-reinforcing clusters. Each idea in the cluster makes the others more believable, more spreadable, more resistant to attack. Religions are the canonical example: creation story + moral code + rituals + community + afterlife promise all reinforce each other. Remove one and the others weaken.

### Mimetic Desire (from source — Girard framework)

"Girard believes that humans are governed not by intrinsic personal preferences, but aspirational 'models,' towards which we unconsciously orient our behavior."

Three positions:
- **Subject**: the person who wants something
- **Object**: the thing they want
- **Model**: the person the subject imitates by wanting the object

"We crave certain objects not because we actually want them, but because other people — the models — do."

When objects are scarce → mimetic rivalry → scapegoating to restore order.

This explains WHY ideas spread beyond pure information value: people spread ideas to imitate their models, to signal belonging to aspirational groups, to compete for status within networks.

### Memetic Tribes (from source — Limberg)

"A group of agents with a meme complex that directly or indirectly seeks to impose its distinct map of reality — along with its moral imperatives — on others."

Tribes squabble over scarce resource: public mindshare. Rivalry leads to scapegoating (cancel culture). But context collapse prevents any single scapegoat from resolving the conflict.

## Process

### Step 1: Identify the Core Memeplex

Ask:
- What cluster of ideas does this concept belong to?
- What OTHER ideas do people who believe this ALSO tend to believe?
- What rituals, symbols, or institutions support this cluster?
- What "model" figures champion this memeplex?

Map it:
```
MEMEPLEX: [Name]
├── Core idea: [the idea being analyzed]
├── Supporting idea 1: [reinforcing concept]
├── Supporting idea 2: [reinforcing concept]
├── Ritual/practice: [what behaviors reinforce belief]
├── Symbol/language: [tribal markers, jargon, aesthetics]
├── Institution: [organizations that formalize the cluster]
└── Model figures: [who do carriers imitate?]
```

### Step 2: Map Competing Memeplexes

Every memeplex exists in opposition to others. Identify:
- What memeplex directly competes for the same audience?
- What narratives are positioned as alternatives?
- Where do the memeplexes overlap (shared assumptions) vs. diverge (points of conflict)?

Source insight: "Mimetic desire might not fully explain why every type of meme is propagated. Some memes are passed along because we find them entertaining, or we want to strengthen relationships with the person we pass them onto — though this, too, could be recast in the light of modeling ourselves after those we look up to."

### Step 3: Analyze Mimetic Desire Dynamics

For each memeplex, identify:
- **Models**: Who are the aspirational figures? Whose behavior do carriers imitate?
- **Objects**: What scarce resource are carriers competing for? (Status, mindshare, moral authority, institutional access)
- **Rivalry**: Where does competition between models/carriers create conflict?
- **Scapegoating**: Who gets blamed when tension builds? (Source: Girard — "communities resort to scapegoating where an individual or group is singled out, blamed for the conflict, and expelled to restore harmony")

### Step 4: Assess Reinforcement Strength

Rate the memeplex on:
- **Internal coherence**: How well do the ideas reinforce each other? (1-5)
- **Institutional backing**: How many formal institutions support it? (1-5)
- **Model strength**: How aspirational/visible are the model figures? (1-5)
- **Ritual density**: How many repeated practices reinforce belief? (1-5)
- **Narrative completeness**: Does the memeplex explain the world comprehensively? (1-5)

Higher scores = harder to disrupt. Lower scores = vulnerable to competing ideas.

### Step 5: Identify Vulnerability Points

Where can the memeplex be disrupted?
- **Model failure**: If a key model figure is discredited, does the memeplex weaken?
- **Internal contradiction**: Do any supporting ideas conflict with each other?
- **Institutional erosion**: Are the supporting institutions losing credibility?
- **Better model emerging**: Is there a more aspirational figure championing a competing memeplex?
- **Ritual decay**: Are the reinforcing practices losing participation?

Source: "Social media made it easier to discover new niche subcultures, but also reduced our desire to challenge culture in surprising ways, because it's more prestigious — by mimetic standards — to use proven formulas for grabbing people's attention than to do something potentially risky and original."

### Step 6: Strategic Implications

Based on the analysis:
- If your idea fits within a STRONG memeplex: leverage the existing reinforcement structure
- If your idea COMPETES with a strong memeplex: identify vulnerability points, avoid direct confrontation, use dark forest strategy
- If your idea creates a NEW memeplex: you need to build supporting ideas, rituals, and model figures — not just the core concept
- If your idea is ORPHANED (belongs to no memeplex): highest risk of failure — needs either memeplex adoption or memeplex creation

## Output Template

```markdown
## Memeplex Analysis: [Idea]

### Your Idea's Memeplex
**Name:** [memeplex name]
**Core cluster:**
- [idea 1]
- [idea 2]
- [idea 3]
**Supporting structures:** [rituals, institutions, symbols]
**Model figures:** [who carries this memeplex]
**Reinforcement score:** [X/25]

### Competing Memeplexes
**Competitor 1:** [name]
- Core ideas: [what they believe]
- Models: [who carries it]
- Overlap: [shared assumptions]
- Conflict point: [where they diverge]

**Competitor 2:** [name]
[same structure]

### Mimetic Desire Dynamics
**Models:** [aspirational figures driving spread]
**Scarce object:** [what carriers compete for]
**Rivalry pattern:** [how competition manifests]
**Scapegoat risk:** [who gets blamed when tension builds]

### Vulnerability Assessment
- [vulnerability 1]
- [vulnerability 2]
- [vulnerability 3]

### Strategic Implications
**For spreading your idea:** [how to leverage or navigate this landscape]
**Key risk:** [biggest threat from competitive memeplex]
**Recommended approach:** [direct competition / dark forest / memeplex adoption / memeplex creation]

### Next Steps
- [which skill to run next and why]
```

## [NEEDS SOURCE MATERIAL]

This skill is speculative. The source material provides the conceptual foundations (Dawkins memeplex, Girard mimetic desire, Limberg memetic tribes) but doesn't detail a step-by-step procedure for mapping memeplexes. The process above is inferred from the theoretical framework. To strengthen this skill, provide:
- Case studies of memeplex analysis applied to real ideas/movements
- Detailed methodology for competitive memeplex mapping
- Empirical examples of mimetic desire dynamics in idea spread
- Procedures for measuring reinforcement strength

## Common Analysis Mistakes

**Mistake 1: Treating ideas as isolated** — Every idea exists within a memeplex. Analyzing an idea without its reinforcing cluster misses why it persists or fails.

**Mistake 2: Ignoring mimetic desire** — People don't spread ideas because the ideas are "good." They spread them because their models do, because spreading signals belonging, because competition demands it.

**Mistake 3: Underestimating institutional reinforcement** — Ideas backed by institutions (universities, media, companies) have structural advantages that raw quality can't overcome.

**Mistake 4: Assuming your memeplex is obvious to you** — You are embedded in your own memeplex. It's hard to see the water you swim in. Actively map it rather than assuming you already understand it.

## When to Use Other Skills

- **After analyze-memeplex → design-strategy:** Use landscape awareness to inform strategy phases
- **After analyze-memeplex → craft-content:** Know which narratives to counter or leverage
- **After analyze-memeplex → identify-champions:** Find the models driving mimetic desire
- **After analyze-memeplex → build-immunity:** Understand what hostile memeplexes threaten your network
- **After analyze-memeplex → reframe-idea:** If your idea sits in a dying memeplex, reframe to fit a stronger one

## References

See `/references/source-summary.md`:
- Memeplex definition (Dawkins via Nadia)
- Mimetic desire framework (Girard via Nadia)
- Memetic tribes concept (Limberg)
- Cultural production and status (W. David Marx)
- Scapegoating dynamics (Girard)
