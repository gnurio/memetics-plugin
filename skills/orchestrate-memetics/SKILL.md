---
name: orchestrate-memetics
description: >
  Intelligent router for the memetics skill network. Analyzes user requests, determines
  which skills to invoke and in what order, chains their outputs together, and accumulates
  context across the session. Use whenever you have a memetics question and aren't sure
  which specific skill to start with.
---

# Orchestrate Memetics

You are the intelligent router for memetics work, analyzing requests and routing to the right skills in the right sequence.

## What This Skill Does

Takes any memetics question or task and:
1. Understands what the user is asking
2. Detects the entry point (where to start)
3. Routes to appropriate starting skill
4. Chains outputs from skill to skill
5. Accumulates context so later skills have full information
6. Returns final answer to user with reasoning chain

This skill sits above the 16 specialized skills and orchestrates them intelligently.

## When to Use This Skill

Use orchestrate-memetics whenever:
- "I have an idea I want to spread but don't know what to do"
- "What should I do with this memetic concept?"
- "My team is being consumed by a supermeme, help"
- "I want to build a movement around this idea"
- "Help me understand the memetics of what I'm seeing"
- Any memetics question where you're not sure which specific skill fits

Don't use this skill if:
- You already know exactly which skill you need (go directly to that skill)
- You're just looking for memetics definitions (read source-summary.md)
- You need quick tactical advice (go to specific skill)

## The Skill Registry

| Skill | Accepts | Produces | Use When |
|-------|---------|----------|----------|
| classify-idea | Raw idea/content | Classification (meme\|antimeme\|supermeme\|cliche) | User has idea, needs to understand type |
| assess-fitness | Classified idea + commitment capacity | GO\|NO-GO recommendation | User wants strategic decision on spreading |
| map-network | Network description + idea type | Topology recommendation (dense\|sparse\|hybrid) | User needs to structure network for spreading |
| design-strategy | All above + champions list | Phased strategy with tactics | User wants concrete action plan |
| craft-content | Core message + audience | Content variants (3-5 ready to post) | User wants shareable content |
| execute-calendar | Approved content | Posting schedule with timing | User wants to execute viral posting |
| identify-champions | Classified idea + network | Champion profiles + recruitment strategy | User needs to find advocates |
| detect-supermeme | Classified supermeme | Red flag assessment + defense strategy | User suspects supermeme trap |
| evaluate-fitness | Classified idea + network | Transmission\|Immunity\|Symptomatic scores | User wants exact memetic metrics |
| transform-taboo | Antimeme + taboo classification | Transformation timeline + inoculation strategy | User has controversial idea needing acceptance |
| monitor-receptivity | Idea in development | Readiness assessment + phase advancement recommendation | User needs to know when network is ready |
| build-immunity | Network description | Immunity strategy + tactics | User wants to defend network against bad memes |
| apply-domain | General strategy + domain | Domain-specific playbook | User wants to adapt strategy to their domain |
| reframe-idea | Failed/stuck idea + failure reason | 2-3 reframed versions + recommendation | Idea classified as cliché, NO-GO from assess, or confirmed supermeme |
| analyze-memeplex | Idea + optional network context | Memeplex map + competitive landscape + mimetic desire analysis | User wants to understand the idea ecosystem before spreading |

## Routing Logic

### Entry Point Detection

Analyze the user's request to find the entry point:

**Pattern 1: Raw Idea, Uncertain**
```
User: "I have this idea, and I think it could spread, but I don't know if I should try"
→ START: classify-idea
→ ROUTE TO: assess-fitness
→ ROUTE TO: (design-strategy if GO, or explain why NO-GO)
```

**Pattern 2: Classified Idea, Wants Decision**
```
User: "This is a really important but hard-to-spread idea. Should I try to champion it?"
→ START: assess-fitness (skip classify since already known)
→ ROUTE TO: identify-champions (if GO)
→ ROUTE TO: design-strategy (full plan)
```

**Pattern 3: Has Classified Idea, Wants Execution**
```
User: "I've classified it as antimeme, I'm ready to spread it. What's my strategy?"
→ START: design-strategy (skip classify and assess, go straight to execution)
→ ROUTE TO: craft-content or map-network first
```

**Pattern 4: Suspicious of Supermeme**
```
User: "I keep obsessing about this idea and can't stop. Is it a supermeme trap?"
→ START: detect-supermeme
→ ROUTE TO: build-immunity (if confirmed supermeme)
```

**Pattern 5: Wants Exact Metrics**
```
User: "What's the transmission rate and immunity of this idea?"
→ START: evaluate-fitness
→ (Can then route to assess-fitness)
```

**Pattern 6: Has Strategy, Wants Domain Adaptation**
```
User: "I have a product I'm launching. How do I use memetics for marketing?"
→ START: apply-domain
→ (References general memetics but applies to product domain)
```

**Pattern 7: Wants Network Defense**
```
User: "How do I make my team more resistant to bad ideas?"
→ START: build-immunity
→ (Standalone defensive skill)
```

**Pattern 8: Dead End Recovery**
```
User: "This idea isn't working" or "How do I make this spreadable?"
→ START: reframe-idea
→ ROUTE TO: classify-idea (re-classify reframed version)
→ ROUTE TO: assess-fitness (re-assess)
```

**Pattern 9: Ecosystem Understanding**
```
User: "What's the landscape around this idea?" or "Why does this keep failing?"
→ START: analyze-memeplex
→ ROUTE TO: design-strategy (informed by landscape)
```

### Chaining Rules

After each skill produces output, follow these rules for next step:

**From classify-idea:**
- If supermeme (4-5 red flags) → ROUTE TO: detect-supermeme
- If cliche → ROUTE TO: reframe-idea (recover novelty)
- If meme or antimeme → ROUTE TO: assess-fitness

**From assess-fitness:**
- If NO-GO but idea has potential → ROUTE TO: reframe-idea (restructure for viability)
- If NO-GO → RETURN TO USER with explanation, end chain
- If GO → ROUTE TO: identify-champions AND map-network (parallel)

**From identify-champions + map-network (parallel):**
- Both outputs ready → ROUTE TO: design-strategy

**From design-strategy (meme path):**
- ROUTE TO: craft-content → execute-calendar

**From design-strategy (antimeme path):**
- If taboo → ROUTE TO: transform-taboo → monitor-receptivity
- If non-taboo → ROUTE TO: monitor-receptivity

**From detect-supermeme:**
- If confirmed supermeme and user wants to spread anyway → ROUTE TO: reframe-idea (narrow to tractable sub-problem)

**From craft-content:**
- ROUTE TO: execute-calendar (for scheduling)

**From reframe-idea:**
- ROUTE TO: classify-idea (verify reframed version escaped failure mode)
- If reframe produces viable antimeme → ROUTE TO: design-strategy
- If reframe produces meme → ROUTE TO: craft-content

**From analyze-memeplex:**
- ROUTE TO: design-strategy (with landscape awareness)
- ROUTE TO: identify-champions (find models driving mimetic desire)
- ROUTE TO: reframe-idea (if idea sits in hostile memeplex)

**From any skill:**
- User asks for domain adaptation → ROUTE TO: apply-domain

### Skip Logic

Not every request needs the full chain. Skip when:

**Skip classify-idea if:**
- User already says "this is a meme/antimeme/supermeme/cliche"
- They've already done classification themselves

**Skip assess-fitness if:**
- User already committed to spreading ("I'm going for it")
- They've already made GO decision internally

**Skip identity-champions if:**
- User is working solo, no network to recruit
- Champions already identified

**Skip map-network if:**
- Network structure already chosen ("we're going private")

**Skip design-strategy if:**
- User only wants tactical execution (content/calendar)
- They say "just tell me what to post"

**Go directly to specific skill if:**
- User says "I just need X skill"
- Clear tactical request vs. strategic

### Error and Dead-End Handling

**If skill produces output that doesn't match downstream input:**
- RETURN TO USER with partial results
- EXPLAIN what was produced
- SUGGEST next logical steps (even if no skill exists)
- OFFER ALTERNATIVES

Example:
```
classify-idea → "This is a cliche (worn-out idea)"
Dead-end: No downstream skill for cliches
Response: "This idea has lost transmission power.
Options: (1) Reframe into new angle, (2) Find different idea with impact"
```

**If speculative skill is needed but incomplete:**
- TELL USER what source material is missing
- OFFER to proceed with available information
- MARK outputs as incomplete

## Context Accumulation

The orchestrator maintains a session context object:

```
context = {
  "original_request": "User's initial question",

  "classification": {
    "type": "meme|antimeme|supermeme|cliche",
    "confidence": "high|medium|low",
    "reasoning": "..."
  },

  "fitness": {
    "go_no_go": "GO|NO-GO",
    "reasoning": "..."
  },

  "network": {
    "topology": "dense|sparse|hybrid",
    "reasoning": "..."
  },

  "champions": {
    "identified": ["Name 1", "Name 2"],
    "roles": ["Patient zero", "Language creator"],
    "commitment": "3-5 years"
  },

  "strategy": {
    "path": "antimeme dark forest|meme viral|taboo transformation",
    "phases": ["Phase 1: ..."]
  },

  "content": {
    "variants": ["Variant 1", "Variant 2", "Variant 3"],
    "recommended": "Variant 1 (high transmissibility)"
  },

  "calendar": {
    "schedule": "..."
    "frequency": "3-5/day"
  },

  "reframe": {
    "original_failure": "cliche|supermeme|no-go",
    "reframed_versions": [],
    "chosen_reframe": null
  },

  "memeplex": {
    "own_memeplex": null,
    "competitors": [],
    "mimetic_desire": null,
    "vulnerabilities": []
  },

  "risks": ["Burnout", "Immunity increase"],
  "contingencies": ["Plan if X happens", "Plan if Y happens"]
}
```

Each skill reads the full context and adds its output. Later skills can reference earlier outputs without re-deriving them.

## Output Format

Final response to user includes:

```markdown
# Memetics Analysis: [User's Topic]

## Summary
[One paragraph summary of recommendation]

---

## Your Specific Question
[Direct answer to what user asked]

---

## The Analysis Chain
- Step 1: classify-idea → [Result]
- Step 2: assess-fitness → [Result]
- Step 3: [Continue chain...]

---

## Recommendation
[Specific next steps for user]

---

## Risks to Watch
- [Risk 1]
- [Risk 2]

---

## References
- [Relevant source materials]
```

## Common Orchestration Mistakes

**Mistake 1: Over-routing**
- User says "just create content"
- You route through classify → assess → design → craft
- User gets overwhelmed with information
- Fix: Skip to craft-content directly

**Mistake 2: Under-routing**
- User says "should I spread this?"
- You only route to assess-fitness
- Misses strategic understanding from other skills
- Fix: Also route to design-strategy for full picture

**Mistake 3: Wrong entry point**
- User says "I want to make a strategy"
- You start at classify-idea
- They already classified it
- Fix: Ask what they know already

**Mistake 4: Ignoring context**
- Earlier skill outputs matter for later decisions
- You make decisions in isolation
- Results are disconnected
- Fix: Reference prior context in each step

**Mistake 5: Not explaining chain**
- User gets final answer without seeing reasoning
- They don't understand how you got there
- Fix: Show the chain, explain each step

## When to Pause and Ask User

**Pause for clarification if:**
- User's goal is ambiguous
- Multiple entry points possible
- Your classification conflicts with their description
- You need information to route effectively

**Ask before routing to:**
- Assess-fitness: "Are you willing to commit 3-5 years?"
- Design-strategy: "Have you identified any believers yet?"
- Apply-domain: "What's your domain? (personal brand, product, movement?)"

## Success Indicators

The orchestrator is working well if:
- User gets clear, actionable answer
- They understand why that's the recommendation
- They know which specific skill to use next
- They can explain the chain of reasoning
- The context accumulation prevents re-explaining

## References

See:
- `/references/source-summary.md` for decision frameworks
- Individual skill SKILL.md files for I/O contracts and detailed processes
