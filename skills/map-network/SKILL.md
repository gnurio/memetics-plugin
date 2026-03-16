---
name: map-network
description: >
  Analyze your network structure and recommend optimal topology (dense, sparse, or hybrid)
  for spreading your idea. Use when you need to decide: should I develop this privately or
  go public? Dense networks for development and trust-building, sparse for viral scale.
---

# Map Network Topology

You are analyzing network structure and recommending optimal topology for spreading an idea.

## What This Skill Does

Takes a description of your network and the idea type, then recommends the best network structure:
- **Dense networks** (group chats, private communities) - for development and antimeme incubation
- **Sparse networks** (public platforms) - for viral scale of memes
- **Hybrid approach** - develop privately, then scale publicly

Outputs explain tradeoffs and switching strategy.

## Input/Output Contract

**Accepts:**
- Network description (current state, size, connectivity, homogeneity)
- Idea type (meme | antimeme | supermeme)
- Strategic goal (development/incubation vs. scale vs. validation)
- Timeline (how many years?)

**Produces:**
- Recommended topology: dense | sparse | hybrid
- Explanation of why this topology fits the idea
- Strengths and weaknesses of recommendation
- Concrete tactics for implementing recommendation
- Switching strategy (if hybrid: when/how to transition)

**Passes to:**
- design-strategy (uses network recommendation to create playbook)
- monitor-receptivity (tracks readiness to switch from dense to sparse)

## Process

### Step 1: Understand the Network Structure

Analyze your current network on these dimensions:

**Dimension 1: Density (how connected)**
- Dense: Everyone knows everyone, high trust, low threshold for sharing controversial ideas
- Sparse: Loosely connected, low trust, high threshold for controversy
- Current state: Where is your network today?

**Dimension 2: Homogeneity (how similar)**
- Homogeneous: Similar beliefs, backgrounds, values (echo chamber risk)
- Heterogeneous: Diverse perspectives (resistant to new ideas but more balanced)
- Current state: Are people in your network like each other?

**Dimension 3: Context (how much shared history)**
- High-context: Long relationships, shared language, implicit understanding
- Low-context: Transactional, need explicit explanation, little shared history
- Current state: How much do people know each other?

**Dimension 4: Formality (structure level)**
- Formal: Official roles, hierarchy, rules
- Informal: Loose, peer-level, self-organizing
- Current state: Is there authority structure or peer governance?

### Step 2: Assess Idea-Network Fit

Match the idea type to network properties:

**If MEME (high transmit, low impact):**
- Fits: Sparse networks (low-context, loose connections okay)
- Why: Spreads easily, doesn't require deep understanding
- Network structure: Can use social platforms, broad audiences
- Risk: Context collapse, meaning distortion

**If ANTIMEME (low transmit, high impact):**
- Fits: Dense networks (high-context, high trust essential)
- Why: Needs deep understanding, high cognitive load
- Network structure: Group chats, private communities, tight circles
- Risk: Echo chambers, slow spread

**If SUPERMEME (high transmit, high impact):**
- AVOID spreading
- If must address: Use sparse networks + containment strategy
- Risk: Will spread uncontrollably

### Step 3: Understand Dense Network Properties

Use dense networks for developing antimemes (high-impact, hard-to-spread ideas).

**Strengths of Dense Networks:**
- Reinforce ideas strongly (repetition and validation from trusted group)
- Safe for half-formed thoughts (room for mistakes, evolution)
- Build trust (people open up more)
- Incubate antimemes (can discuss taboo/controversial ideas)
- Preserve nuance (context shared, less distortion)
- Develop language (create shared terminology)

**Weaknesses of Dense Networks:**
- Weak immune systems (vulnerable to wrong ideas spreading unchecked)
- Can't jump gaps (ideas trapped in the group)
- Echo chamber risk (groupthink, lack of external pressure)
- Small reach (limited to group size)
- Hard to scale (adding people destabilizes trust)

**Best for:**
- Developing controversial ideas (taboos, challenging orthodoxy)
- Building core believers (3-5 deeply committed people)
- Creating shared language/framework
- Private refinement phase (dark forest)

**Tactics:**
- Small group (4-10 people max to start)
- Regular meetings (weekly or bi-weekly)
- Explicit confidentiality agreements
- Structured discussion format (read + discuss + synthesize)
- Clear roles (facilitator, note-taker, synthesizer)

### Step 4: Understand Sparse Network Properties

Use sparse networks for spreading memes (high-transmit, lightweight ideas).

**Strengths of Sparse Networks:**
- Diffuse ideas quickly (low friction to share)
- Reach diverse audiences (no gatekeeping)
- Test market receptivity (see what resonates)
- Scale rapidly (network effects)
- Low barrier to entry (don't need to "join" anything)

**Weaknesses of Sparse Networks:**
- Context collapse (detailed meaning becomes distorted)
- High immunity baseline (people skeptical by default)
- Short attention spans (ideas forgotten quickly)
- Difficult to maintain nuance (reduced to soundbites)
- No relationship substrate (harder to build trust)
- Algorithmic randomness (spread depends on platform mechanics)

**Best for:**
- Launching validated ideas (proven in dense networks first)
- Viral content (lightweight, memorable)
- Broad awareness (getting the word out)
- Reaching beyond existing circles

**Tactics:**
- Platform selection (Twitter, TikTok, Reddit, LinkedIn, etc.)
- Content optimization (short, shareable, memorable)
- Hashtags and discoverability (algorithm amplification)
- Volume strategy (3-5 posts per day)
- Community building (threads, replies, engagement)

### Step 5: Recommend Hybrid Strategy

For most serious antimemes, recommend hybrid:

**Dense Phase (Years 1-2):**
- Build private network (4-10 core believers)
- Refine message and language
- Develop examples and frameworks
- Create "patient zero" stories
- Identify champions
- Build trust and alignment

**Transition Phase (6 months):**
- Soft testing (small reveals to broader network)
- Gauge receptivity (what resonates?)
- Identify validators (respected people who agree)
- Test message variants (what lands?)
- Find natural amplifiers (people naturally sharing it)

**Sparse Phase (Years 2-3+):**
- Public emergence (champions go public)
- Coordinated reveals (multiple networks simultaneously)
- Leverage validators (trusted messengers boost credibility)
- Rapid scale (networks connect)
- Mainstream adoption (idea becomes obvious)

**Key principle:**
"Memetic and antimemetic cities depend on each other"
- Dense develops ideas, creates depth
- Sparse scales ideas, reaches breadth
- Both needed for successful spread

### Step 6: Explain Tradeoffs

For each recommendation, explain:

**Density Tradeoff:**
- More dense = safer development, more echo chamber risk
- More sparse = broader reach, more distortion risk

**Timeline Tradeoff:**
- Dense first (slower, safer) vs. sparse immediately (faster, riskier)
- Hybrid requires patience through Phase 1

**Group Size Tradeoff:**
- Smaller dense groups = higher trust, deeper work, slower development
- Larger groups = more perspectives, faster development, harder coordination

**Authority Tradeoff:**
- Hierarchical leadership = faster decisions, possible dogmatism
- Peer governance = slower decisions, more resilience

## Output Template

```markdown
## Recommended Topology: [DENSE | SPARSE | HYBRID]

**Idea Type:** [meme | antimeme | supermeme]
**Strategic Goal:** [development | scale | validation]

---

## Why This Topology

**Fit Analysis:**
- Idea transmissibility: [high | low] → favors [sparse | dense]
- Idea impact: [high | low] → favors [dense | sparse]
- Your goal: [you need] [privacy/validation/reach]
- Timeline: [X years] → recommends [this topology]

---

## This Topology's Strengths

For your situation:
- [Specific strength 1 relevant to your goal]
- [Specific strength 2 relevant to your idea]
- [Specific strength 3 relevant to your timeline]

---

## Weaknesses to Watch

- [Specific weakness 1 and how to mitigate]
- [Specific weakness 2 and how to mitigate]
- [Specific weakness 3 and how to mitigate]

---

## Implementation Tactics

**Immediate (next 30 days):**
- [Action 1]
- [Action 2]
- [Action 3]

**Medium-term (3-6 months):**
- [Action 1]
- [Action 2]
- [Action 3]

**Long-term (6+ months):**
- [Action 1]
- [Action 2]
- [Action 3]

---

## If Hybrid: Switching Strategy

**Dense Phase Objectives:**
- [Develop X]
- [Build Y]
- [Refine Z]

**Transition Triggers:**
- When: [specific conditions indicate readiness]
- Who decides: [champion, core group, measurement?]
- How quick: [gradual or rapid shift?]

**Sparse Phase Launch:**
- Start with: [which platform(s)?]
- Lead with: [which champions?]
- Amplify with: [validators, content types, timing]

---

## Risks Specific to This Topology

- [Risk 1 and mitigation]
- [Risk 2 and mitigation]
- [Risk 3 and mitigation]
```

## Common Topology Mistakes

**Mistake 1: Using wrong topology for idea type**
- Example: Trying to spread complex antimeme via social media only (sparse network)
- Result: Idea gets distorted, rejected, or trivialize
- Fix: Use dense for development, sparse for proven ideas

**Mistake 2: Staying too long in dense phase**
- Example: Perfecting message for 3 years in private group
- Result: Idea never reaches tipping point, stays niche
- Fix: Set explicit transition date, get uncomfortable with imperfection

**Mistake 3: Going public too early**
- Example: Revealing antimeme to broad audience before core believers ready
- Result: Idea triggers immune response, gets shut down
- Fix: Spend adequate time in Phase 1 (minimum 1 year, typically 2)

**Mistake 4: Confusing "private" with "secret"**
- Example: Making group existence hidden
- Result: Looks like conspiracy, triggers opposition
- Fix: Private group is okay; secret group is not. Be transparent about gathering.

**Mistake 5: Ignoring context collapse**
- Example: Assuming message that works in dense group will work on Twitter
- Result: Gets misunderstood, attacked, or ridiculed
- Fix: Explicitly reframe for sparse network audience (simpler, shorter, vice examples)

## When to Use Other Skills

- **Before map-network → identify-champions:** Know who should be in your dense network
- **After map-network → design-strategy:** Network choice informs playbook selection
- **After map-network → monitor-receptivity:** Tracks when dense→sparse transition happens

## References

See `/references/source-summary.md`:
- "Network Topology Strategy" section for detailed topology analysis
- "Strategic Playbooks" section for context on phases
- "Practical Applications by Domain" for domain-specific network structures
