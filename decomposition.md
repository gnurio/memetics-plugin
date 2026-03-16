# Memetics Plugin: Skill Decomposition

**Extracted from:**
- Memetics 101 - Practical Guide
- Difference between meme and cliche
- Examples of memes, antimemes and cliches

**Date:** 2026-03-16

---

## Skill Inventory

### Confirmed Skills (10)

| # | Skill Name | What It Does | Status |
|---|---|---|---|
| 1 | classify-idea | Determine if raw idea is meme/antimeme/supermeme/cliche | Confirmed |
| 2 | assess-fitness | Decide if idea is strategically worth spreading (GO/NO-GO) | Confirmed |
| 3 | map-network | Recommend network structure (dense/sparse/hybrid) for spreading | Confirmed |
| 4 | design-strategy | Create phased spread strategy (dark forest → tipping point OR viral) | Confirmed |
| 5 | craft-content | Write optimized viral content for transmissibility | Confirmed |
| 6 | identify-champions | Find and develop persistent idea advocates | Confirmed |
| 7 | detect-supermeme | Flag and defend against parasitic supermemes | Confirmed |
| 8 | evaluate-fitness | Measure transmission rate, network immunity, symptomatic period | Confirmed |
| 9 | transform-taboo | Gradual acceptance process for taboo/controversial ideas | Confirmed |
| 10 | monitor-receptivity | Track network readiness signals for idea launch | Confirmed |

### Speculative Skills (4)

| # | Skill Name | What It Does | Status | Missing Information |
|---|---|---|---|---|
| 11 | build-immunity | Strengthen network resistance to unwanted memes and supermemes | Speculative | Source describes defensive goal but not implementation procedure |
| 12 | execute-calendar | Schedule viral content with optimal timing and frequency strategy | Speculative | Source recommends 3-5 posts/day but doesn't detail scheduling methodology |
| 13 | apply-domain | Adapt general playbooks to specific domains (personal/product/movement) | Speculative | Source lists domain applications but doesn't fully detail playbooks |
| 14 | orchestrate-memetics | Intelligent router for all memetics skills (special - orchestrator) | Confirmed | Entry point and routing logic |

---

## Coverage Matrix: Source Sections to Skills

| Source Section | Source Lines | Maps to Skills |
|---|---|---|
| Core Definitions (meme, antimeme, supermeme, cliche) | 7-28 | classify-idea |
| Three Variables (transmission, immunity, symptomatic) | 32-61 | evaluate-fitness, design-strategy |
| Dark Forest Playbook (Phase 1) | 68-73 | design-strategy |
| Coordinated Emergence (Phase 2) | 75-80 | design-strategy, monitor-receptivity |
| Tipping Point (Phase 3) | 82-87 | design-strategy, monitor-receptivity |
| Viral Content Tactics | 91-103 | craft-content, execute-calendar |
| Network Topology (dense/sparse/hybrid) | 122-156 | map-network |
| Champion Playbook | 160-175 | identify-champions |
| Defensive Memetics | 179-201 | detect-supermeme, build-immunity |
| Domain Applications | 205-226 | apply-domain |
| Decision Framework (YES/NO) | 261-296 | assess-fitness |
| Cliche vs Meme Distinction | difference-file:1-28 | classify-idea |
| Examples of meme/antimeme/cliche | examples-file | classify-idea (reference examples) |
| Taboo Transformation | 107-118 | transform-taboo |
| Common Mistakes | 249-257 | Embedded as warnings across skills |
| Mental Models | 230-245 | Context/orchestrator reasoning |

---

## I/O Chain Map

```
User Request (any memetics question)
    ↓
ORCHESTRATE-MEMETICS (router)
    ├─ Detect entry point and path
    └─ Accumulate context
    ↓
CLASSIFY-IDEA (raw idea → classified idea)
    Outputs: idea_type (meme|antimeme|supermeme|cliche), reasoning, risk_flags
    ↓
    ├─→ [If supermeme detected]
    │   ↓
    │   DETECT-SUPERMEME (classified → red flags + defense strategy)
    │   ├─→ Return to user with warning, OR
    │   └─→ BUILD-IMMUNITY (preventive network tactics)
    │
    ├─→ [If cliche detected]
    │   ↓
    │   Return to user: idea has lost transmissibility, suggest reframe
    │
    └─→ [If meme or antimeme]
        ↓
        EVALUATE-FITNESS (classified idea → transmission_rate, immunity, symptomatic_period)
        ↓
        ASSESS-FITNESS (classified + evaluated → GO/NO-GO + reasoning)
        ├─→ [If NO-GO] Return to user with explanation
        └─→ [If GO]
            ↓
            IDENTIFY-CHAMPIONS (classified + GO → champion_profiles, recruitment_tactics)
            ↓
            MAP-NETWORK (idea_type + goal → network_recommendation)
            ↓
            DESIGN-STRATEGY (all above → phased_strategy_with_tactics)
            ├─→ [If meme strategy]
            │   ↓
            │   CRAFT-CONTENT (core_message → content_variants)
            │   ↓
            │   EXECUTE-CALENDAR (approved_content → posting_schedule)
            │
            └─→ [If antimeme strategy]
                ├─→ [If taboo idea]
                │   ↓
                │   TRANSFORM-TABOO (classified + strategy → gradual_acceptance_plan)
                │   ↓
                │   MONITOR-RECEPTIVITY (ongoing → readiness_signals)
                │
                └─→ [If domain-specific]
                    ↓
                    APPLY-DOMAIN (strategy + domain_context → domain_playbook)
```

---

## Dependency Graph

**Entry Points (no dependencies):**
- classify-idea (takes raw user input)
- build-immunity (standalone defensive skill)

**Requires Classify:**
- assess-fitness
- map-network
- detect-supermeme
- evaluate-fitness
- identify-champions
- transform-taboo
- apply-domain

**Requires Assess-Fitness (GO recommendation):**
- identify-champions
- map-network
- design-strategy

**Requires Map-Network:**
- design-strategy
- monitor-receptivity

**Requires Design-Strategy:**
- monitor-receptivity (for antimeme path)
- execute-calendar (for meme path)
- apply-domain (domain adaptation)

**Requires Craft-Content:**
- execute-calendar

**Requires Evaluate-Fitness:**
- assess-fitness (feeds into decision)

**Terminal Skills (produce final output to user):**
- assess-fitness (if NO-GO)
- detect-supermeme (warning output)
- design-strategy (phased plan)
- craft-content (publishable content)
- execute-calendar (posting schedule)
- transform-taboo (acceptance timeline)
- apply-domain (domain playbook)

---

## MECE Validation

### Mutual Exclusivity: All Boundaries Are Clear

✓ **Classification vs. Fitness Assessment:**
- Classify answers "What type of idea is this?" (property detection)
- Assess answers "Should I spread this?" (strategic decision)
- No overlap: classification is descriptive, assessment is prescriptive

✓ **Viral Content vs. Dark Forest Strategy:**
- Craft-content produces shareable artifacts for memes
- Design-strategy (antimeme path) is multi-phase incubation and launch
- No overlap: different idea types and workflows

✓ **Network Topology vs. Strategy Design:**
- Map-network analyzes network structure (input/precondition)
- Design-strategy uses that analysis to create action plan
- Not alternatives: topology is input to strategy, not competing with it

✓ **Supermeme Detection vs. Main Classification:**
- Classify categorizes all idea types
- Detect-supermeme adds specialized red-flag analysis + defense
- No overlap: detection is enhancement to classification, not replacement

✓ **Champion Identification vs. Strategy Design:**
- Identify-champions focuses on people (who will advocate)
- Design-strategy focuses on process (how ideas spread)
- No overlap: complementary concerns

✓ **Taboo Transformation vs. General Strategy:**
- Design-strategy provides generic dark forest → tipping point playbook
- Transform-taboo specializes that playbook for taboo dynamics
- No overlap: transformation is specialization, not alternative

✓ **Monitoring vs. Strategy:**
- Design-strategy is planning
- Monitor-receptivity is execution surveillance
- No overlap: different phases of work

✓ **Build Immunity vs. Detect Supermeme:**
- Detect-supermeme identifies individual supermemes and defends against them
- Build-immunity strengthens entire network's resistance
- No overlap: individual defense vs. systemic prevention

### Collective Exhaustiveness: All Actionable Content Is Covered

✓ **Core Definitions** → classify-idea (meme, antimeme, supermeme, cliche definitions)
✓ **Three Variables** → evaluate-fitness (transmission, immunity, symptomatic measurement)
✓ **Transmission Increase Tactics** → design-strategy (embedded in playbooks)
✓ **Immunity Decrease Tactics** → design-strategy (find receptive networks, use validators)
✓ **Symptomatic Period Extension** → design-strategy (make consequential, tie to identity)
✓ **Dark Forest Playbook** → design-strategy (Phase 1 tactics)
✓ **Coordinated Emergence** → design-strategy (Phase 2 tactics)
✓ **Tipping Point** → design-strategy (Phase 3 tactics)
✓ **Viral Content Tactics** → craft-content (villain, narrative, weight, niche targeting)
✓ **Secondary Accounts** → execute-calendar (risk assessment, scheduling)
✓ **Volume Strategy** → execute-calendar (3-5 posts/day, timing)
✓ **Network Topology Dense** → map-network (identify and recommend when)
✓ **Network Topology Sparse** → map-network (identify and recommend when)
✓ **Hybrid Strategy** → map-network (recommend and explain switching)
✓ **Champion Role: Patient Zero** → identify-champions (own idea publicly)
✓ **Champion Role: Persistent Advocate** → identify-champions (advocate 3-5+ years)
✓ **Champion Role: Language Creator** → identify-champions (develop terms/frameworks)
✓ **Champion Role: Network Connector** → identify-champions (bridge siloed groups)
✓ **Supermeme Red Flags** → detect-supermeme (apocalyptic, vague, etc.)
✓ **Supermeme Defense** → detect-supermeme (time-boxing, sub-problem focus)
✓ **Network Immunity Building** → build-immunity (gradual exposure, frameworks, diversity)
✓ **Personal Branding Applications** → apply-domain (domain-specific playbook)
✓ **Product Launch Applications** → apply-domain (domain-specific playbook)
✓ **Social Movement Applications** → apply-domain (domain-specific playbook)
✓ **YES/NO Decision Framework** → assess-fitness (decisioning logic)
✓ **Cliche Recognition** → classify-idea (worn-out memes)
✓ **Taboo Transformation Process** → transform-taboo (gradual inoculation)
✓ **Monitoring and Readiness** → monitor-receptivity (when to advance phases)
✓ **Common Mistakes** → Embedded as warnings in relevant skills
✓ **Mental Models** → Context in orchestrator reasoning

---

## Speculative Skills: What's Needed

### Build Network Immunity
**Status:** Speculative
**Missing:** Source describes defensive goal (lines 197-201) but doesn't detail implementation procedure.
**Needs to complete:**
- Specific tactics for gradually exposing network to diverse ideas
- Explicit decision frameworks to teach
- Critical evaluation protocols
- Optimal diversity ratios and exposure frequency
- Timeline for immunity building

### Evaluate Memetic Fitness
**Status:** Speculative (though well-founded)
**Missing:** Source names three variables but doesn't provide measurement methodology.
**Needs to complete:**
- How to assess transmission rate (quantitative? qualitative? input from who?)
- How to assess network immunity percentage (surveys? historical data? archetypes?)
- How to estimate symptomatic period (half-life? factors affecting duration?)
- How to composite scores into decision-useful metric
- Confidence levels and error margins

### Execute Content Calendar
**Status:** Speculative
**Missing:** Source recommends 3-5 posts/day but doesn't detail scheduling methodology.
**Needs to complete:**
- Optimal posting times per platform (Twitter prime hours, etc.)
- Content rotation patterns (avoid repetition burnout)
- Primary vs. secondary account decision rules
- How to sequence content (cliff notes, deep dives, engagement bait)
- Analytics tracking and virality monitoring
- When to pause or accelerate posting

### Monitor Network Receptivity
**Status:** Speculative
**Missing:** Source mentions monitoring as necessary but doesn't specify signals or decision rules.
**Needs to complete:**
- Specific indicators of reduced immunity (linguistic patterns? behavior change? network growth?)
- How to distinguish between phases (are we still in Phase 1 or ready for Phase 2?)
- Measurement methods (surveys? archival? informant networks?)
- Decision rules for phase advancement (threshold metrics?)
- False positive filtering (distinguish genuine receptivity from noise)

### Transform Taboo to Mainstream
**Status:** Confirmed but light on procedure
**Missing:** Source gives principles but not step-by-step procedure.
**Needs to complete:**
- Detailed gradual inoculation schedule (how many networks? how frequently introduced?)
- "Sediment filter" mechanics (how long should ideas sit before advancing?)
- Specific immune response triggers to avoid
- Exact timing and decision rules for coordinated reveal
- Success metrics for taboo transformation
- Handling rejection and immunity spikes

### Apply Domain-Specific Strategy
**Status:** Speculative
**Missing:** Source lists domain applications but doesn't fully detail playbooks.
**Needs to complete:**
- Full personal branding memetics playbook
- Full product launch memetics playbook
- Full social movement memetics playbook
- Domain-specific metrics and checkpoints
- Domain-specific risk factors
- Examples and case studies for each domain

---

## Orchestrator Routing Logic

The orchestrator (orchestrate-memetics skill) uses this logic:

### Entry Point Detection
- **If user has raw idea/content and no classification** → START with classify-idea
- **If user explicitly asks "should I spread this?"** → START with classify-idea → assess-fitness
- **If user has classified idea and wants to act** → START with design-strategy (or identify-champions if first question is "who should help?")
- **If user asks "how do I defend against bad ideas?"** → START with detect-supermeme or build-immunity
- **If user is evaluating a specific supermeme** → START with detect-supermeme
- **If user asks domain-specific question** → START with apply-domain

### Chaining Rules
After each skill completes, inspect outputs:

**Terminal outputs (return to user):**
- assess-fitness outputs NO-GO → return with explanation
- detect-supermeme outputs high-risk warning → return with defense strategy
- design-strategy outputs phased plan → return (user may request Craft-Content next)
- craft-content outputs content variants → return (user may request Execute-Calendar next)
- execute-calendar outputs schedule → return (terminal delivery)
- transform-taboo outputs timeline → return
- apply-domain outputs domain playbook → return

**Routing rules:**
- classify-idea output (classified idea) can go to: assess-fitness, map-network, detect-supermeme, evaluate-fitness, identify-champions, transform-taboo
- assess-fitness output (GO) → automatically route to identify-champions AND map-network (run in parallel)
- map-network output + identify-champions output → automatically route to design-strategy
- design-strategy output (meme path) → route to craft-content
- design-strategy output (antimeme path, non-taboo) → return to user
- design-strategy output (antimeme + taboo) → route to transform-taboo
- craft-content output → route to execute-calendar
- evaluate-fitness output → feeds into assess-fitness (not standalone return)

### Skip Logic
Skip skills when:
- User already classified idea → skip classify-idea, start with assess-fitness
- User already has fitness assessment → skip classify + assess, start with design-strategy
- User only wants to craft one-off content → skip classify through design, go directly to craft-content
- User explicitly asks for specific skill → route directly there, don't force full chain
- Skill's preconditions aren't met (e.g., user hasn't committed to timeline needed for assess-fitness) → skip and explain why

### Error Handling
- If skill returns no clear output → return to user with partial results and explain what downstream steps are available
- If speculative skill is needed but incomplete → tell user what source material would complete it, offer to proceed with available info
- If output doesn't match any downstream skill's input → return to user with result and suggest logical next steps (even if no skill exists)

---

## MECE Judgment Calls

### Why Apply-Domain Is Separate
Could have integrated domain applications as routing within orchestrator rather than separate skill. Made it separate because:
- Domain expertise is distinct from general memetics (different mental models)
- Source material treats domains as complete playbooks, not just routing options
- Separation allows domain specialists to fill in domain-specific details later
- Clearer for users: "which domain are you in?" is explicit routing question

### Why Detect-Supermeme Is Separate
Could have made supermeme detection just an output of classify-idea. Made it separate because:
- Requires different reasoning (red-flag pattern matching vs. property classification)
- Produces defensive recommendations not relevant to all classifications
- Defensive memetics is distinct from offensive/neutral classification
- Users might ask "help me defend against this" without pre-classification

### Why Evaluate-Fitness Is Separate
Could have merged into assess-fitness. Separated because:
- Measurement is distinct from decision-making
- Allows users to get metrics without committing to strategy
- Provides data that feeds into assess-fitness decision
- Separates "what are the transmission stats?" from "should I act on them?"

### Why Craft-Content and Execute-Calendar Are Separate
Could have merged. Separated because:
- Content creation is distinct from scheduling/timing
- Users might want to draft content without committing to calendar
- Execution calendar is about systematic posting strategy, not creation
- Craft-content can serve marketing teams; calendar serves ops teams

### Why Transform-Taboo Is Not Merged Into Design-Strategy
Could have made taboo transformation just output of design-strategy with conditional logic. Separated because:
- Taboo transformation has specialized principles (lines 107-118) distinct from standard antimeme strategy
- Long timeline (5-10 years) and monitoring needs are specific
- Users need explicit guidance on taboo-specific mistakes
- Teaches different mental models (network sediment filter, immune response management)

---

## Source Provenance

Every skill in this decomposition traces back to specific sections of source material:

**Primary Source:** Memetics 101 - Practical Guide
- Core definitions and properties
- Three variables framework
- All strategic playbooks
- Network topology analysis
- Champion playbook
- Defensive memetics
- Practical applications
- Decision frameworks
- Common mistakes

**Secondary Sources:**
- "Difference between meme and cliche" - cliche dynamics, worn-out memes
- "Examples of memes, antimemes, and cliches" - concrete examples, vaccimes/contra-memes definition

This decomposition extracts and organizes the actionable knowledge from these sources into atomic, reusable skills with clear inputs, outputs, and triggering conditions.

---

## Next Steps for Completion

1. **Review skill files** - Each SKILL.md file contains complete instructions, I/O contracts, and markers for where speculative skills need additional source material

2. **Fill gaps in speculative skills** - Where source material is referenced but procedure is incomplete, [NEEDS SOURCE MATERIAL] markers show exactly what information is needed

3. **Test with users** - Run memetics questions through the orchestrator, observe which skills are invoked, validate that routing logic produces expected results

4. **Refine domain playbooks** - Once Apply-Domain skill is used by domain experts, domain-specific playbooks can be developed and specialized

5. **Add monitoring tools** - As Monitor-Receptivity skill is used, develop concrete tooling for measuring network readiness (surveys, linguistic analysis, etc.)

6. **Develop measurement frameworks** - As Evaluate-Fitness is used, systematize the assessment of transmission rate, network immunity, symptomatic period
