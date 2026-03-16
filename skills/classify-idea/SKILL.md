---
name: classify-idea
description: >
  Classify a raw idea or concept into its memetic type (meme, antimeme, supermeme, or cliche).
  Use this skill when you have an idea and need to understand its spreading properties,
  or when you're evaluating whether an idea will naturally transmit or face resistance.
  Trigger on: "What type of meme is this?", "Will this spread?", "Is this a good idea to promote?",
  "Classify this idea", "What kind of meme is X?"
---

# Classify Memetic Idea

You are evaluating a raw idea or concept and determining its memetic classification. This is the entry point for most memetics work.

## What This Skill Does

Takes a raw idea, content, or concept and determines which memetic type it is:
- **Meme**: High transmissibility, low impact
- **Antimeme**: Low transmissibility, high impact
- **Supermeme**: High transmissibility, high impact (parasitic)
- **Cliche**: Worn-out meme that has lost infective power

Your output classifies the idea and explains the reasoning, so downstream skills can route appropriately.

## Input/Output Contract

**Accepts:**
- Raw idea or concept description (text, 1-1000 words)
- Optional: context about target network or intended audience
- Optional: history (has this idea been circulating? how long?)

**Produces:**
- Classification: meme | antimeme | supermeme | cliche
- Confidence level (high, medium, low)
- Supporting reasoning with key property assessment
- Risk flags (if supermeme: red flags identified)
- Recommended next skill(s)

**Passes to:**
- assess-fitness (for meme/antimeme classified as GO/NO-GO decision)
- map-network (to understand what network structure to use)
- detect-supermeme (if supermeme detected: defensive strategy)
- evaluate-fitness (to measure exact transmission/immunity properties)
- identify-champions (to find advocates)
- transform-taboo (if antimeme + taboo identified)
- craft-content (to create shareable versions)

## Process

### Step 1: Extract Core Properties

Analyze the idea across three dimensions:

**Property A: Transmissibility (How easily does it spread?)**
- High: Lightweight, entertaining, matches existing beliefs, emotionally activating
- Low: Complex, counterintuitive, threatens existing beliefs, requires deep understanding

**Property B: Impact (How much does it matter if true?)**
- High: Consequential to people's lives, changes values/behaviors, long-term implications
- Low: Entertaining but ultimately inconsequential, short-term entertainment

**Property C: Symptomatic Period (How long does it stay in mind?)**
- Short: People engage briefly then forget (entertainment, trends)
- Long: People think about it repeatedly, affects decisions over time

### Step 2: Map Properties to Classification

Use this matrix:

```
                High Impact          Low Impact
High Transmit   SUPERMEME          MEME
Low Transmit    ANTIMEME           (rare - neither transmits nor impacts)
```

**Meme (High Transmit, Low Impact):**
- Examples: viral tweets, trending phrases, catchy songs, funny videos
- Properties: lightweight, shareable, easy to understand, emotionally engaging
- Spread naturally without champions
- People forget quickly after engagement

**Antimeme (Low Transmit, High Impact):**
- Examples: original insights, complex truths, uncomfortable ideas, important secrets
- Properties: requires understanding, challenges existing beliefs, high cognitive load
- Need champions to spread
- People who get it care deeply

**Supermeme (High Transmit, High Impact):**
- Examples: existential threats (AI danger, climate catastrophe), apocalyptic narratives, war stories
- Properties: emotionally activating, easy to understand, seemingly consequential
- Spread rapidly and dominate attention
- Creates rumination loops ("can't stop thinking about it")
- USUALLY PARASITIC

**Cliche (formerly Meme, now worn-out):**
- Examples: jokes everyone's heard, punchlines that don't land, tired expressions
- Properties: was once transmissible, now triggers boredom/rejection, no novelty
- Negative feedback from repetition kills spread
- "Empty" - retains form but lost meaning

### Step 3: Check for Supermeme Red Flags

If you classified as supermeme, assess these red flags:

**RED FLAG 1: Apocalyptic framing**
- Language: "if we don't act, X will destroy us", "existential threat", "now or never"
- Example: "AI will make humanity extinct by 2030"
- Problem: Creates urgency without actionability

**RED FLAG 2: Vague/unmeasurable goals**
- Language: "change the world", "save humanity", "transform culture"
- Example: "We need to prevent catastrophe" (without defining what success looks like)
- Problem: You can never declare victory, so attention never stops

**RED FLAG 3: Appeals to "save the world"**
- Grandiose framing
- Martyr/hero language
- "Your efforts are the only thing standing between order and chaos"
- Problem: Creates false urgency

**RED FLAG 4: Demands total prioritization**
- Language: "this must be your only focus", "everything else is distraction"
- Example: "Climate change is so important that other problems don't matter"
- Problem: Prevents balanced thinking and tradeoff analysis

**RED FLAG 5: No clear success metrics**
- Can't point to: "if we achieve X by date Y, we've succeeded"
- Progress is always insufficient
- Problem: Operates in eternal crisis mode

**Scoring:**
- 0-1 flags: Likely meme or antimeme (not supermeme)
- 2-3 flags: Probable supermeme (caution advised)
- 4-5 flags: Strong supermeme (recommend defensive approach)

### Step 4: Check for Cliche Indicators

Has this idea been repeated so many times it's lost impact?

**Indicators:**
- Audience fatigued with the idea (negative feedback to repetition)
- Novelty wore out (was surprising, now obvious)
- Lost infective power (people no longer share it)
- Feels hollow/empty when articulated
- Triggers boredom rather than enthusiasm

**Example:** "You should follow your passion" was a powerful meme in 1990s. By 2020, it's a cliche - everyone's heard it, nobody feels compelled to share it.

### Step 5: Assess Confidence Level

How confident are you in this classification?

**High confidence:**
- Clear-cut category with obvious properties
- Unambiguous transmissibility and impact
- Minimal contradictory signals

**Medium confidence:**
- Some properties point different directions
- Transmissibility might vary by audience
- Impact depends on context

**Low confidence:**
- Ambiguous on key properties
- Insufficient information (ask user for clarification)
- Idea is new and precedent-lacking

## Examples from Source Material

### Clear Meme Examples
- "Happy Birthday to You" (song) - transmits easily, low consequential impact
- Wearing baseball caps backward - lightweight fashion trend, spreads socially
- "Winston tastes good like a cigarette should" - catchy jingle, easy to remember
- Cat videos - entertaining, shareable, forgettable

### Clear Antimeme Examples
- Complex mathematical insight - hard to understand, consequential if true, low natural spread
- "The Hayekian case for capitalism" - source notes: counterintuitive, hard to explain, true but unpopular
- Original scientific theories - revolutionary ideas that face initial rejection
- Uncomfortable truths about systems/society - consequential but challenging to discuss

### Clear Supermeme Examples
- "AI will destroy humanity by 2030" - spreads rapidly, emotionally activating, apocalyptic
- Climate catastrophe narratives - high spread, high impact framing, rumination loops
- War narratives - spread rapidly during conflict, dominate attention
- Existential threats (pandemics, nuclear war) - natural panic spread

### Cliche Examples
- "Think outside the box" - was novel insight, now worn-out business jargon
- "Work smarter, not harder" - was useful principle, now empty phrase nobody cares about
- "Be yourself" - was empowering message, now tired platitude
- "Love conquers all" - was poetic truth, now hollow romantic cliche

## Decision Tree

```
START: User provides raw idea

  1. Is this idea currently spreading (even slowly)?
     NO → [May be antimeme] Go to Q2
     YES → [Likely meme or supermeme] Go to Q3

  2. Is this idea trivial/low-impact?
     YES → Transmit is LOW, Impact is LOW → [rare, ignore this case]
     NO → Transmit is LOW, Impact is HIGH → **ANTIMEME**
          Rule: Check for red flags as precaution
          Recommend: assess-fitness, identify-champions, design-strategy

  3. Does idea have 4-5 supermeme red flags?
     YES → **SUPERMEME (probable)**
          Rule: High transmit + high impact + apocalyptic properties
          Recommend: detect-supermeme, build-immunity
          Warning: Are you sure you want to spread this?

     NO → Does idea have 2-3 supermeme red flags?
          YES → **SUPERMEME (possible)**
               Rule: High transmit + high impact + some parasitic properties
               Recommend: detect-supermeme (for confirmation)

          NO → Does idea feel worn-out/tiresome?
               YES → **CLICHE**
                    Rule: Was transmissible, lost infective power
                    Recommend: assess-fitness (NO-GO), suggest reframe

               NO → **MEME**
                    Rule: High transmit, low impact, spreads naturally
                    Recommend: craft-content, execute-calendar (if you want to amplify)
```

## Output Template

Use this structure for your response:

```markdown
## Classification: [MEME | ANTIMEME | SUPERMEME | CLICHE]

**Confidence:** [High | Medium | Low]

**Reasoning:**

**Transmissibility:** [High | Low] - [explanation of why spread is easy or hard]
**Impact:** [High | Low] - [explanation of why it matters or doesn't]
**Symptomatic Period:** [Short | Long] - [explanation of how long idea stays in mind]

**Key Properties:**
- [property 1]
- [property 2]
- [property 3]

[If supermeme] **Red Flags Detected:**
- [ ] Apocalyptic framing
- [ ] Vague/unmeasurable goals
- [ ] "Save the world" appeals
- [ ] Total prioritization demands
- [ ] No success metrics

**Score:** [X/5 supermeme red flags]

**Next Steps:**
User should consider: [recommend next skill(s) based on classification]
```

## Common Classification Mistakes

**Mistake 1: Confusing "popular" with "meme"**
- Just because something's popular doesn't make it a meme
- Supermemes can be even more popular
- Check the three properties, not just spread rate

**Mistake 2: Assuming high-impact = supermeme**
- Antimemes also have high impact
- The difference: antimemes are HARD to spread; supermemes spread EASILY
- Use transmissibility as key discriminator

**Mistake 3: Dismissing something as "just a cliche"**
- Check: did it actually lose infective power, or are you just tired of hearing about it?
- Your fatigue ≠ audience fatigue
- Look for negative feedback from target audience

**Mistake 4: Missing red flags in plausible-sounding ideas**
- Supermemes are often disguised as legitimate concerns
- Don't skip the red flag check just because the idea seems important
- Example: "We need to prepare for AI catastrophe" might be meme (if measured/tractable) or supermeme (if apocalyptic/vague)

## When to Use Other Skills

- **After classify-idea → assess-fitness:** You want a GO/NO-GO decision on spreading
- **After classify-idea → evaluate-fitness:** You want exact metrics on transmission/immunity/symptomatic period
- **After classify-idea → detect-supermeme:** You want confirmation if supermeme risk (or defense strategy)
- **After classify-idea → map-network:** You want to know what network structure to use
- **After classify-idea → identify-champions:** You want to find advocates for an antimeme
- **After classify-idea → craft-content:** You want to create viral versions (especially for memes)

## References

See `/references/source-summary.md`:
- "Core Definitions" section for detailed category descriptions
- "Examples of Each Memetic Type" section for more examples
- "Decision Frameworks from Source" section for evaluation guidelines
