---
name: reframe-idea
description: >
  Transform a dead-end idea into a viable memetic form. Converts clichés into fresh angles,
  supermemes into tractable sub-problems, and NO-GO ideas into spreadable versions. Use when
  classify-idea returns cliché, assess-fitness returns NO-GO, or detect-supermeme confirms
  parasitic properties. Trigger on: "How do I make this spreadable?", "This idea isn't working",
  "Reframe this", "Make this less apocalyptic", "Find a fresh angle".
---

# Reframe Memetic Idea

Core concept: Ideas that fail memetic assessment can often be salvaged by changing their packaging, scope, or framing — without losing the core insight.

## What This Skill Does

Takes a failed/stuck idea and applies one of three transformation paths:

1. **Cliché → Fresh Angle**: Recover novelty from a worn-out idea by finding the unsaid or contrarian take
2. **Supermeme → Tractable Sub-Problem**: Narrow apocalyptic, vague ideas into measurable, actionable scope
3. **NO-GO → Viable**: Address the specific failure criterion (low impact, no champion, high immunity) by restructuring

## Input/Output Contract

**Accepts:**
- The idea in its current form
- Classification output (from classify-idea) or assessment output (from assess-fitness/detect-supermeme)
- The specific failure reason (cliché, supermeme, NO-GO flag)
- Optional: target network context

**Produces:**
- 2-3 reframed versions of the idea
- For each: which transformation path was used, why it works, and predicted classification of the reframed version
- Recommendation on which reframe to pursue
- Recommended next skill(s) for the chosen reframe

**Passes to:**
- classify-idea (re-classify the reframed version)
- assess-fitness (re-assess with the new framing)
- craft-content (if reframe produces something ready to spread)
- design-strategy (if reframe produces viable antimeme)

## Process

### Step 1: Diagnose the Failure Mode

Identify exactly WHY the idea failed:

**If CLICHÉ:**
- What made it novel originally? When did novelty wear out?
- Is the CORE INSIGHT still valid, just overexposed?
- What has the audience NOT heard about this topic?
- Source: "A cliché occurs when a meme 'wears out'. When an audience is tired of a joke or an idea, it starts to receive negative feedback, which kills the meme's ability to propagate further."

**If SUPERMEME:**
- Which red flags triggered? (apocalyptic, vague goals, no metrics, total prioritization, no success criteria)
- Is there a legitimate concern buried under the parasitic framing?
- Can the scope be narrowed to something measurable?
- Source: Nadia writes that supermemes "suck up everyone's attention and time and result in very little constructive action; they are parasites."
- Example from source: "We must prepare for existential AI risk" (supermeme) → "Invest X% in AI safety research with clear measurable outcomes" (antimeme/meme — tractable, measurable)

**If NO-GO (from assess-fitness):**
- Which specific criterion failed?
  - Low impact → needs scope change or different network
  - No champion → needs different messenger or coalition
  - High immunity → needs different network or slower inoculation
  - Ego-driven → needs reorientation toward network benefit
  - Supermeme properties → apply supermeme reframe path

### Step 2: Apply Transformation

**PATH A: Cliché Recovery**

Techniques:

1. **Contrarian Inversion**: Take the opposite position. "Follow your passion" (cliché) → "Ignore your passion, follow your curiosity" (fresh)
2. **Specificity Injection**: Replace vague with concrete. "Be authentic" (cliché) → "Post one thing this week that would embarrass your professional self" (specific, actionable)
3. **New Evidence Attachment**: Tie the worn-out idea to recent data, events, or examples that make it feel timely again
4. **Audience Shift**: Same core insight, different network where it hasn't been heard yet
5. **Format Shift**: Same idea, radically different packaging. Essay → data visualization. Tweet → long-form case study. Advice → story.

Source support: The examples file notes that a cliché "retains form but lost meaning" — so the goal is to restore meaning through one of these transformations.

**PATH B: Supermeme Narrowing**

Techniques:

1. **Scope Reduction**: "Save the planet" → "Reduce plastic waste in your city by 30% this year"
2. **Metric Attachment**: Force measurable success criteria onto the vague threat
3. **Timeboxing**: "Existential forever-crisis" → "What can we accomplish in 12 months?"
4. **Sub-problem Extraction**: Identify one tractable piece of the supermeme and champion THAT
5. **Villain Specificity**: Replace vague existential threat with a specific, attackable target (source: Jason Levin — "pick a villain to fight against. It doesn't have to be a person. It can be a big faceless company.")

Source support: The book notes supermemes have "a surprising lack of consensus as to what the 'climate crisis' actually means, nor how to measure its progress." The reframe forces that missing specificity.

**PATH C: NO-GO Restructuring**

For each failure mode:
- **Low impact**: Change the SCOPE or the NETWORK. Same idea in a network where it's more consequential. Or expand the idea's implications.
- **No champion**: Reduce the idea to a form that doesn't NEED a 3-5 year champion. Can it be a meme (short burst) instead of an antimeme (long advocacy)?
- **High immunity**: Use the sediment filter approach — introduce through a proxy idea that lowers resistance first. Inoculate gradually rather than attempting direct transmission. Source: "Networks need to be inoculated to avoid triggering an immune response."
- **Ego-driven**: Strip the idea of personal branding. Reframe as network benefit. Remove yourself as the visible champion and empower others.

### Step 3: Generate 2-3 Reframed Versions

For each reframe, provide:
- The reframed idea (concrete, not abstract)
- Which technique was used
- Predicted classification of the reframed version (meme/antimeme/supermeme/cliché)
- Why this version avoids the original failure mode
- Strength: what's better about this version
- Risk: what could still fail

### Step 4: Recommend Best Reframe

Choose the strongest reframe based on:
- Highest predicted impact
- Lowest predicted immunity in target network
- Most sustainable (can you champion this version for 3-5 years?)
- Best fit with user's actual capabilities and network

## Output Template

```markdown
## Reframe Analysis

**Original Idea:** [the idea as submitted]
**Failure Mode:** [CLICHÉ | SUPERMEME | NO-GO: specific flag]
**Diagnosis:** [why exactly it failed]

---

### Reframe 1: [Name]
**Technique:** [which transformation technique]
**Reframed Idea:** [the new version]
**Predicted Classification:** [meme | antimeme]
**Why This Works:** [how it avoids the original failure]
**Strength:** [best property]
**Risk:** [remaining vulnerability]

### Reframe 2: [Name]
[same structure]

### Reframe 3: [Name] (optional)
[same structure]

---

## Recommendation

**Best Reframe:** [which one and why]
**Next Steps:** Run [classify-idea | assess-fitness | craft-content | design-strategy] on the reframed version
**Timeline Impact:** [how this reframe affects the spread timeline]
```

## Examples from Source Material

**Example 1: Supermeme → Tractable**
- Original: "AI will make humanity extinct" (supermeme — apocalyptic, no metrics, total prioritization demanded)
- Reframe: "Federal AI safety labs should publish quarterly risk assessments with specific capability thresholds" (antimeme — specific, measurable, championed by policy experts)

**Example 2: Cliché → Fresh**
- Original: "Follow your passion" (cliché — everyone's heard it, triggers boredom)
- Reframe: "Your passion is probably wrong — track what makes you lose time instead" (contrarian inversion — challenges the premise, creates novelty)

**Example 3: NO-GO (high immunity) → Viable**
- Original: Trying to spread Yarvin's political theory in progressive academic network (NO-GO: immunity too high)
- Reframe: Abstract the non-political structural insights and present them through a different lens to a different network — tech/startup communities where structural analysis resonates (audience shift + specificity injection)
- Source: The book documents exactly this pattern — Yarvin's ideas spread through tech networks first, where immunity was lower, before eventually reaching broader discourse.

## Common Reframing Mistakes

**Mistake 1: Cosmetic reframe** — Changing the words but not the structure. "Save the world" → "Change the world" is not a reframe. The scope, metrics, and framing must actually change.

**Mistake 2: Losing the core insight** — Reframing so aggressively that the original truth disappears. The goal is to preserve what's valuable while changing what blocks transmission.

**Mistake 3: Reframing into another supermeme** — Narrowing one apocalyptic framing into another. Test the reframed version against supermeme red flags.

**Mistake 4: Assuming one reframe is enough** — Sometimes you need multiple rounds of reframing. Run the reframed version through classify-idea again to verify it actually escaped the failure mode.

## When to Use Other Skills

- **After reframe-idea → classify-idea:** Verify the reframed version's classification
- **After reframe-idea → assess-fitness:** Check if the reframe makes it GO
- **After reframe-idea → craft-content:** If the reframe is ready for content creation
- **After reframe-idea → design-strategy:** If the reframe produces a viable antimeme strategy

## References

See `/references/source-summary.md`:
- Supermeme characteristics and reframing examples
- Cliché definition and novelty recovery
- Network immunity and inoculation strategy
- Villain narrative strategy from Jason Levin
