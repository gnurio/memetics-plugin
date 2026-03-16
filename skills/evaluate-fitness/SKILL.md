---
name: evaluate-fitness
description: >
  Measure specific memetic properties of an idea: transmission rate, network immunity,
  and symptomatic period. Use when you want exact metrics on spreadability before
  committing to strategy. Outputs scored assessment feeding into fitness decision.
---

# Evaluate Memetic Fitness

You are measuring specific properties that determine how well an idea can spread.

## What This Skill Does

Takes a classified idea and measures three key variables:
- **Transmission Rate:** How likely infected people spread to others
- **Network Immunity:** Percentage of target population categorically resistant
- **Symptomatic Period:** How long people actively think/express the idea

Outputs scored assessment that feeds into strategy design.

## Input/Output Contract

**Accepts:**
- Classified idea (meme, antimeme, supermeme)
- Target network description (who will we be spreading to)
- Historical context if available (has this been attempted before?)

**Produces:**
- Transmission rate score (high/medium/low + factors)
- Network immunity assessment (high/medium/low + reasons)
- Symptomatic period estimate (short/medium/long + drivers)
- Composite fitness score
- Recommendations for strategy based on scores

**Passes to:**
- assess-fitness (uses these metrics to inform GO/NO-GO decision)

## Transmission Rate Assessment

How likely is an "infected" person to spread the idea to others?

### High Transmission Indicators

**Emotional Activation:**
- ✓ Anger (fastest spread emotion)
- ✓ Joy (highly shareable)
- ✓ Curiosity (drives engagement)
- ✓ Validation (makes people feel smart)

Example: "Here's how X company is exploiting creators" → high anger activation

**Lightweight Format:**
- ✓ Fits in social media format
- ✓ Can be shared in seconds
- ✓ Doesn't require deep explanation
- ✓ Quotable (people remember it)

Example: A 5-word phrase beats a 500-word essay

**Alignment with Existing Beliefs:**
- ✓ Doesn't contradict core values
- ✓ Feels intuitive to target audience
- ✓ Builds on existing knowledge
- ✓ Requires little cognitive adjustment

Example: "Effective altruism" (builds on existing "do good" value) vs. "Extreme hedonism is actually ethical" (contradicts)

**Perceived Impact:**
- ✓ Seems important to people who might spread it
- ✓ Consequences are imaginable
- ✓ Spreader looks smart for sharing it
- ✓ Others will want to know about it

Example: "How to double your productivity" vs. "The color of my office"

**Social Proof Elements:**
- ✓ Others are talking about it
- ✓ Seems like a trend
- ✓ "Everyone's thinking about this"
- ✓ Low social cost to share

Example: Idea shared by trusted people in your network

### Low Transmission Indicators

**Requires Deep Understanding:**
- ✗ Complex explanation needed
- ✗ Counterintuitive
- ✗ Challenges core beliefs
- ✗ Technical or specialized

Example: "The Hayekian case for capitalism" (hard to explain, counterintuitive)

**Contradicts Existing Beliefs:**
- ✗ Goes against group values
- ✗ Feels wrong intuitively
- ✗ Sharer looks foolish
- ✗ High social cost to share

Example: Arguing against universally held values in your audience

**High Friction to Share:**
- ✗ Too long to explain
- ✗ Requires credentials to understand
- ✗ Needs visual aids or context
- ✗ Easily misunderstood

Example: Dense academic papers vs. viral tweets

**No Emotional Hook:**
- ✗ Intellectually interesting but emotionally neutral
- ✗ Doesn't make people feel anything
- ✗ Boring
- ✗ Low share motivation

Example: "Here are statistics about something" with no narrative

### Scoring Transmission Rate

Count your idea against factors:

**High transmission (3+ factors present):** Transmission Rate = HIGH
**Medium transmission (1-2 factors):** Transmission Rate = MEDIUM
**Low transmission (0 factors, or negative factors present):** Transmission Rate = LOW

## Network Immunity Assessment

What percentage of your target population is categorically resistant?

### High Immunity Signals

**Value Conflicts:**
- Core value disagreement with the idea
- Idea threatens existing beliefs
- Example: Arguing against someone's religion to a religious person (very high immunity)

**Identity Threat:**
- Idea threatens group identity
- Suggests identity was wrong
- Example: "You've been doing your job wrong your whole career" (high identity threat)

**Cognitive Dissonance:**
- Accepting idea requires changing too much
- Too much psychological work
- Example: "Everything you think about society is backwards"

**Institutional Resistance:**
- Existing institutions threatened
- Example: "We should eliminate the legal system" to lawyers (institutional threat)

**In-Group Norms:**
- Idea violates "how we do things here"
- Saying it makes you an outsider
- Example: Challenging company culture in front of employees

### Low Immunity Signals

**Value Alignment:**
- Idea aligns with existing values
- Feels like natural extension
- Example: "More freedom" to a freedom-valuing group

**No Identity Threat:**
- Doesn't challenge who people are
- Is orthogonal to identity
- Example: "Here's a new productivity technique" (not threatening)

**Low Cognitive Load:**
- Easy to understand
- Intuitive
- Example: "Simple trick saves time" (easy to accept)

**Network Champions:**
- Respected people already believe it
- Makes it safe to consider
- Example: Multiple trusted figures endorsing

**Flexibility in Group:**
- Group is open to new ideas
- Values learning/evolution
- Example: Scientific communities vs. dogmatic communities

### Scoring Network Immunity

**High immunity (3+ signals present, value conflicts, identity threats):**
- Network Immunity = HIGH (80%+ resistant)
- Strategy: Only proceed if you have champions and long timeline

**Medium immunity (1-2 signals, some friction):**
- Network Immunity = MEDIUM (40-60% resistant)
- Strategy: Manageable with right approach

**Low immunity (no signals, value aligned, champions visible):**
- Network Immunity = LOW (20-40% resistant)
- Strategy: Idea spreads more naturally

## Symptomatic Period Assessment

How long do people actively express/think about the idea?

### Short Symptomatic Period

**Characteristics:**
- ✓ Entertainment-focused
- ✓ Novelty wears off quickly
- ✓ People forget after days/weeks
- ✓ One-time engagement

**Examples:**
- Viral meme (forgotten in a week)
- Trending phrase (in rotation for a month)
- Cat video (watched, enjoyed, forgotten)

**Extending short period is hard** - entertainment is inherently fleeting

### Medium Symptomatic Period

**Characteristics:**
- ✓ Practical/useful
- ✓ People return to it
- ✓ Active engagement for months
- ✓ Useful tool becomes normal

**Examples:**
- New productivity technique (use it for months, becomes normal)
- Dietary approach (people experiment for 3-6 months)
- Business practice (implemented, becomes standard)

**Extending medium period:**
- Build community (people who care about it)
- Create rituals (repeated touchpoints)
- Make it identity-connected ("I'm a X person")

### Long Symptomatic Period

**Characteristics:**
- ✓ Identity-connected
- ✓ Consequential to life
- ✓ People think about it years later
- ✓ Belief-system level

**Examples:**
- Religious belief (people think about for decades)
- Political ideology (shapes all decisions)
- Core value (influences life direction)
- Personality trait (part of identity)

**Natural drivers of long symptomatic:**
- Ties to identity
- Consequential to daily decisions
- Community/ritual around it
- Challenged repeatedly (thinking about it to defend it)

### Extending Symptomatic Period

**Tactic 1: Make It Consequential**
- Connect to real outcomes
- Show impact on person's life
- Example: "This saves you money daily" vs. "This is efficient"

**Tactic 2: Tie to Identity**
- Make it identity-based
- "People who understand X..."
- Community membership signal

**Tactic 3: Create Rituals**
- Weekly/daily touchpoints
- Group discussions
- Public expressions
- Example: Weekly meetings, rituals, public commitments

**Tactic 4: Build Community**
- People who care about this
- Shared language
- Mutual reinforcement
- Example: Subcultures, movements, religions

**Tactic 5: Make It Challenged**
- Ideas get tested and defended
- Controversial (so thinking about it)
- Active opposition (engages believers)

### Scoring Symptomatic Period

**Short (days to weeks):** Symptomatic Period = SHORT
- Example: Viral memes, entertainment

**Medium (weeks to months):** Symptomatic Period = MEDIUM
- Example: Practical techniques, trends

**Long (months to years):** Symptomatic Period = LONG
- Example: Belief systems, identity elements, values

## Composite Fitness Assessment

Map the three dimensions:

```
Transmission: HIGH / MEDIUM / LOW
Immunity: HIGH / MEDIUM / LOW
Symptomatic: SHORT / MEDIUM / LONG
```

### Fitness Profiles

**Profile A: Natural Meme**
- Transmission: HIGH
- Immunity: LOW
- Symptomatic: SHORT
- Assessment: Spreads easily, fast, doesn't stick
- Strategy: Viral content approach, high volume

**Profile B: Challenging Antimeme**
- Transmission: LOW
- Immunity: HIGH
- Symptomatic: LONG
- Assessment: Hard to spread, requires champions, worth doing
- Strategy: Dark forest → tipping point, 3-5 year timeline

**Profile C: Niche Meme**
- Transmission: HIGH (within niche)
- Immunity: MEDIUM (in target, HIGH in broader population)
- Symptomatic: MEDIUM
- Assessment: Spreads within community, doesn't go mainstream
- Strategy: Niche-targeted content, community building

**Profile D: Low-Impact Idea**
- Transmission: MEDIUM
- Immunity: LOW
- Symptomatic: SHORT
- Assessment: Spreads somewhat, doesn't matter much
- Strategy: Might not be worth championing effort

**Profile E: Supermeme-Risk**
- Transmission: HIGH
- Immunity: MEDIUM
- Symptomatic: LONG
- Assessment: Spreads rapidly, dominating, might be parasitic
- Strategy: Don't amplify, use detect-supermeme skill

## Output Template

```markdown
## Memetic Fitness Assessment

**Idea:** [What are we evaluating?]
**Target Network:** [Who will this spread in?]

---

## Transmission Rate

**Score:** [HIGH | MEDIUM | LOW]

**High Transmission Factors Present:**
- [ ] Emotional activation (which emotion?)
- [ ] Lightweight format
- [ ] Aligns with existing beliefs
- [ ] Perceived impact
- [ ] Social proof visible

**Count:** [X/5 factors]

**Explanation:** [Why this transmission rate?]

---

## Network Immunity

**Score:** [HIGH | MEDIUM | LOW]

**Immunity Factors:**
- [ ] Value conflicts
- [ ] Identity threats
- [ ] High cognitive load
- [ ] Institutional resistance
- [ ] In-group norm violation

**Count:** [X/5 factors]

**Explanation:** [Why this immunity level?]

---

## Symptomatic Period

**Score:** [SHORT | MEDIUM | LONG]

**Natural Drivers:**
- [ ] Identity connection
- [ ] Consequential to life
- [ ] Community around it
- [ ] Ritual/repeated touchpoints
- [ ] Challenged/defended

**Count:** [X/5 drivers]

**Explanation:** [Why this period length?]

---

## Fitness Profile

**Pattern:** [Which profile does this match?]

**Strategic Implication:** [What does this profile suggest?]

---

## Recommendations

Based on fitness assessment:
- [Specific advice for this idea]
- [What to enhance or change]
- [Which strategy approach best fits]
```

## When to Use Other Skills

- **After evaluate-fitness → assess-fitness:** Use metrics to inform GO/NO-GO decision
- **After evaluate-fitness → design-strategy:** Fitness profile informs strategy type
- **Before strategy → evaluate-fitness:** Get exact metrics before committing

## References

See `/references/source-summary.md`:
- "The Three Variables of Idea Spread" for detailed transmission/immunity/symptomatic explanation
- "Strategic Playbooks" for how different fitness profiles map to strategies
