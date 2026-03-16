---
name: assess-fitness
description: >
  Decide whether an idea is strategically worth spreading (GO/NO-GO decision).
  Takes a classified idea and answers: "Should I try to spread this?" Use when you've
  classified an idea and want to know if it's worth your time and effort. Produces clear
  GO/NO-GO recommendation with reasoning.
---

# Assess Idea Fitness

You are making a binary strategic decision: should this person attempt to spread this idea?

## What This Skill Does

Takes a classified idea (output from classify-idea skill) and applies a decision framework to determine if it's strategically sound to attempt spreading it. Produces a clear GO/NO-GO recommendation with supporting analysis.

This is the gatekeeper between "interesting idea" and "worth 3-5 years of advocacy effort."

## Input/Output Contract

**Accepts:**
- Classified idea (meme, antimeme, supermeme, or cliche)
- User's commitment capacity (have 3-5 years to champion? yes/no)
- Network context (target network, current immunity level)
- User's motivation (is this for impact or ego?)

**Produces:**
- GO or NO-GO recommendation
- Reasoning with risk factors listed
- Timeline estimate
- Champion requirements
- If NO-GO: what would need to change for GO
- If GO: recommend next skills (identify-champions, map-network, design-strategy)

**Passes to:**
- identify-champions (if GO: find advocates)
- map-network (if GO: choose network structure)
- design-strategy (if GO: create phased plan)
- detect-supermeme (if idea is supermeme: defensive recommendations)

## Decision Framework

### The YES Decision

Recommend GO if ALL of these are true:

**✓ Criterion 1: High Impact**
- The idea is consequential to the target network
- Not just "interesting" but "matters"
- Evidence: People's values/behaviors would shift if they believed it
- Example: "Effective altruism" is high-impact (changes how people allocate resources)
- Example: "My startup is cool" is low-impact (doesn't change anyone's worldview)

**✓ Criterion 2: You Can Commit 3-5+ Years**
- You personally are willing to be the champion (or have identified someone who is)
- Not a "side project" - this requires sustained attention
- Realistic: You understand this is a multi-year commitment
- Timeline breakdown:
  - Years 1-2: Build private network, refine message, find early believers
  - Years 2-3: Test public receptivity, begin emergence phase
  - Years 3-5: Reach tipping point, broader adoption
  - 5+ years: Idea becomes mainstream (people forget you championed it)

**✓ Criterion 3: Early Believers Identified**
- You've found 2-3 people who already believe or are easily convinced
- These become your core group
- They don't need recruiting - they're already on board
- Evidence: Can you name them? Have you talked to them?

**✓ Criterion 4: Network Conditions Favor Reception**
- The target network has lower immunity than average, OR
- You have a path to reduce immunity (champions, validators, trusted messengers), OR
- Timing is favorable (conditions are shifting toward receptivity)
- Check: Do any validators in this network already agree?
- Check: Are there natural alignment points with existing beliefs?

**✓ Criterion 5: You Have Strategy for Each Phase**
- Dark Forest (private): You know how to build the core group
- Coordinated Emergence (semi-private): You have validators to help
- Tipping Point (public): You know trigger conditions
- At minimum: "I will start with a private group and see what develops"

### The NO Decision

Recommend NO-GO if ANY of these are true:

**✗ Flag 1: Low Impact**
- The idea is just interesting, not consequential
- Evidence: If everyone believed it, would anything important change? No.
- Example: "My funny take on celebrity gossip" (entertaining, not consequential)
- Decision: Skip it. Find an antimeme with real impact.

**✗ Flag 2: Supermeme Characteristics**
- Classified as supermeme (high transmit + high impact + apocalyptic)
- OR has 3+ red flags (apocalyptic, vague goals, no metrics, etc.)
- Evidence: Read the supermeme section of classify-idea output
- Decision: Let this spread on its own. Don't amplify it. Consider detect-supermeme skill instead.

**✗ Flag 3: No Champion Available**
- You're not willing to advocate for 3-5+ years, AND
- You can't identify someone who is
- Evidence: Honest answer - "Am I willing to do this for 3-5 years?" If no, stop.
- Decision: This idea will die. It needs a champion or it won't reach tipping point.

**✗ Flag 4: Network Immunity Too High With No Path to Reduce**
- Target network has inherent resistance to this idea (core values conflict), AND
- You don't have trusted validators to help, AND
- Timing can't shift immunity
- Example: Trying to spread atheism in a fundamentalist community with no bridges
- Decision: Find a different network with lower immunity. Or accept 10+ year timeline.

**✗ Flag 5: Primarily Ego-Driven**
- Your motivation is personal status/fame, not network benefit
- Evidence: Honest reflection - "Will the network be better if this spreads? Or just me?"
- Decision: Networks detect ego-driven championing and reject it. Skip it.

### Special Case: Supermemes

If classified as supermeme (or likely supermeme):

**Supermeme Go/No-Go Logic:**
- Supermemes spread naturally without help
- They're parasitic (consume attention without producing value)
- Recommendation: **ALWAYS NO-GO for spreading supermemes**
- Alternative: Use detect-supermeme skill to defend against it
- Exception: Only if you can reframe into a tractable sub-problem with measurable outcomes

**Supermeme reframing example:**
- Original: "We must prepare for existential AI risk" (supermeme - apocalyptic, vague)
- Reframed: "We should invest X% in AI safety research with clear measurable outcomes" (meme/antimeme - tractable, measurable)
- If you can reframe, reassess as the reframed version

## Process

### Step 1: Verify Classification Quality

Before applying the decision framework, confirm:
- Was the classification thorough?
- Do you agree with the supermeme assessment (if any)?
- Is the impact assessment accurate for YOUR network?
- Does the context match your actual situation?

If not, recommend re-running classify-idea with more detailed context.

### Step 2: Assess Each Criterion

Go through YES criteria one by one:

```markdown
**Impact Assessment:**
- Who is the target network?
- What would change if they believed this?
- Is that change important? (yes/no + reasoning)

**Commitment Assessment:**
- Can you commit 3-5 years?
- Or do you know someone who will?
- Is this realistic given your other priorities?

**Early Believers Assessment:**
- Do you know anyone who already agrees?
- Can you name them?
- How many? (need: 2-3 minimum)

**Network Conditions Assessment:**
- What is current immunity level?
- Is there a path to reduce it?
- What's the timeline?

**Strategic Clarity Assessment:**
- Can you describe Phase 1 (private)?
- Can you describe Phase 2 (semi-private)?
- Can you describe Phase 3 (public)?
- If vague: "figure it out as we go" - acceptable but riskier
```

### Step 3: Check for NO-GO Flags

Go through each flag:
- Flag 1 (low impact): Does the idea fail this?
- Flag 2 (supermeme): Was it classified as supermeme?
- Flag 3 (no champion): Can you/someone champion it?
- Flag 4 (high immunity, no path): Does the network reject this fundamentally?
- Flag 5 (ego-driven): Be honest about motivation

If any flag is true, recommend NO-GO.

### Step 4: Make Decision

If all YES criteria pass AND no NO-GO flags: **GO**

If any criterion fails OR any flag triggered: **NO-GO**

### Step 5: Explain Reasoning

Write out the reasoning clearly:
- Which criteria passed/failed
- Why (specific reasoning, not abstract)
- What would need to change for opposite decision
- Confidence level in the decision

## Output Template

```markdown
## Recommendation: [GO | NO-GO]

**Confidence:** [High | Medium | Low]

---

## Reasoning

**Impact:** [High | Low] - [specific explanation for this idea]
- Target network: [who would you spread to?]
- Change if true: [what would shift?]
- Importance: [is this important?]

**Your Commitment:** [3-5 years realistic? yes/no]
- Current capacity: [what else are you doing?]
- Willingness: [honest assessment - are you willing?]
- Champion identified: [you, someone else, or nobody?]

**Network Status:** [immunity level and path]
- Current resistance: [high, medium, low and why]
- Path to reduce: [how could immunity decrease?]
- Timeline: [realistic timeframe?]

**Strategic Clarity:** [clear on phases? yes/no]
- Phase 1 (private): [what does this look like?]
- Phase 2 (semi-private): [transition plan?]
- Phase 3 (public): [what triggers reveal?]

**Motivation Check:** [impact-driven or ego-driven?]
- Primary beneficiary: [the network or you?]
- Alignment: [genuine good for network?]

---

## Flags

**YES Criteria Met:**
- ✓ High impact and consequential
- ✓ 3-5 year commitment available
- ✓ 2-3 early believers identified
- ✓ Network conditions favorable
- ✓ Strategic clarity present

**NO-GO Flags Triggered:**
- [ ] Low impact
- [ ] Supermeme characteristics
- [ ] No champion identified
- [ ] Network immunity too high
- [ ] Motivation primarily ego-driven

---

## What This Decision Means

**If GO:**
- Next steps: Run identify-champions, map-network, design-strategy
- You're committing to 3-5 years of sustained effort
- This is a serious undertaking, not a hobby
- Timeline: expect slow adoption initially

**If NO-GO:**
- Don't spread this idea
- Consider: find different antimeme with higher impact, OR
- Consider: find different network with lower immunity, OR
- Consider: reframe as more tractable version, OR
- Consider: delegate to someone who can champion it

---

## Risk Factors (if GO)

If you proceed, watch for these risks:
1. **Early rejection** - Premature public launch before network ready
2. **Burnout** - 3-5 years is longer than you think
3. **Network evolution** - Resistance may increase, not decrease
4. **Better ideas arriving** - An even better antimeme might appear
5. **Moving goalposts** - Success criteria might shift as you go

Mitigation: Regular check-ins (every 6 months) on: "Is this still worth my time?"
```

## Common Assessment Mistakes

**Mistake 1: Confusing "I like this idea" with "Network should know this"**
- Your enthusiasm ≠ idea's impact
- Test: Ask 5 people in target network. Do they care?

**Mistake 2: Underestimating the 3-5 year timeline**
- People think: "This will take a year or two"
- Reality: Most antimemes need 3-5+ years
- Three year minimum, not maximum

**Mistake 3: Assuming you know the champions**
- You identify someone and assume they'll help
- Reality: You need to have actually had this conversation
- Test: Have you explicitly asked them? Did they commit?

**Mistake 4: Overestimating your commitment**
- You think: "I'm passionate about this, I'll stick with it"
- Reality: Passion fluctuates, life changes
- Test: Are you actually willing to talk about this for 3 years even when nobody listens?

**Mistake 5: Network immunity self-assessment is often wrong**
- You think your network will receive it better than they actually will
- Test: Find validators in target network BEFORE committing

## When to Use Other Skills

- **After assess-fitness (GO) → identify-champions:** Find your core believers and advocates
- **After assess-fitness (GO) → map-network:** Choose dense vs. sparse vs. hybrid
- **After assess-fitness (GO) → design-strategy:** Create the phased rollout plan
- **After assess-fitness (NO-GO) → reclassify:** If you're unsure about classification, re-run classify-idea
- **Before assess-fitness → evaluate-fitness:** If you want exact metrics on transmission/immunity

## References

See `/references/source-summary.md`:
- "Decision Frameworks from Source" section for detailed framework
- "Common Mistakes" section for anti-patterns
- "Champion Playbook" section for commitment expectations
- "The Three Variables" section for impact/transmission understanding
