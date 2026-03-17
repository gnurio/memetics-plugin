---
name: execute-calendar
description: >
  Create and manage a content posting calendar for viral meme spread. Takes approved
  content variants and produces a schedule with timing, platform, volume, and secondary
  account strategy. Implements the 3-5 posts/day consistent posting strategy.

  [NEEDS SOURCE MATERIAL] Source recommends 3-5 posts/day but doesn't detail calendar
  mechanics, optimal timing per platform, or analytics tracking methodology.
---

# Execute Content Calendar

You are scheduling and managing viral content distribution.

## What This Skill Does

Takes approved viral content variants and produces:
- Posting schedule (dates, times, platforms)
- Platform-specific optimization (Twitter vs. LinkedIn, etc.)
- Primary vs. secondary account assignments (risk-based)
- Volume strategy (3-5 posts/day sustained)
- Performance tracking setup
- Adjustment rules (what signals accelerate/decelerate?)

Outputs a ready-to-execute calendar with tracking.

## Input/Output Contract

**Accepts:**
- Approved content variants (from craft-content skill)
- Primary platform(s) (Twitter, LinkedIn, etc.)
- Risk levels per variant (high/medium/low)
- Campaign duration (weeks or months)
- Performance goals (reach, engagement, followers)

**Produces:**
- Posting calendar (dates, times, content assignments)
- Platform-specific tactics
- Account assignments (primary or secondary)
- Performance tracking sheet
- Weekly adjustment rules
- Go/no-go metrics

**Passes to:** Terminal (execution phase)

## [NEEDS SOURCE MATERIAL]

Source material recommends:
- "3-5 posts/day" for sustained campaigns (line 98)
- "Algorithms reward consistency" (line 98)
- Secondary accounts for "unhinged content" (line 96)

But doesn't specify:
1. **Optimal posting times** - When do different audiences engage?
2. **Content rotation patterns** - How to sequence to avoid repetition?
3. **Secondary vs. primary rules** - Exact criteria for which account?
4. **Analytics tracking** - What metrics, how tracked, decision rules?
5. **Adjustment framework** - What triggers increase/decrease posting?

## Based on Available Context

Here's what we can infer from memetics principles:

### Posting Frequency and Volume

**Base Strategy: 3-5 Posts Per Day**

**Why this frequency:**
- Algorithms reward consistency (more chances to be seen)
- Multiple time zones (some people sleep when you post)
- Different content types have different decay rates
- Volume compounds reach over time

**Pattern Options:**

Option 1: Consistent Spacing
- 5 posts evenly spread (5:00am, 9:00am, 1:00pm, 5:00pm, 9:00pm)
- Regular interval (every 4 hours)
- Easy to automate

Option 2: Peak Clustering
- 3 posts at morning peak (7am, 8am, 9am)
- 1-2 posts at lunch peak
- 1-2 posts at evening peak
- Follows engagement patterns

Option 3: Content-Based
- Thread post (morning, highest-effort)
- Quote tweet (early afternoon)
- Original observation (evening)
- Retweet/engagement (throughout day)
- Mix formats for algorithm variety

### Platform-Specific Optimization

**Twitter-Specific:**
- Peak times: 8-10am and 5-7pm weekdays
- Post frequency: 3-5/day sustainable
- Format: Mix threads, tweets, quote-tweets, media
- Engagement: Reply to comments within 1 hour (early)

**LinkedIn-Specific:**
- Peak times: 7-9am and 12-2pm weekdays
- Post frequency: 1-2/day (LinkedIn lower volume)
- Format: Professional, insights, thought leadership
- Engagement: Mix personal and professional

**Mix Approach (Most Effective):**
- Heavy on Twitter (more posts tolerated)
- Supporting on LinkedIn (professional credibility)
- Rare on Facebook/Instagram (different audiences, different content)

### Content Rotation Strategy: Vary by Objective

The two-way nature of social media implies that authors have to persuade their own audience to help spread their message in order to reach wider audiences. Different objectives may require spreading different types of content.

**Weekly Pattern (Example):**

Day 1:
- Tweet 1: Hot take / Villain narrative
- Tweet 2: Data / Evidence
- Tweet 3: Example / Story
- Tweet 4: Question (engagement bait)
- Tweet 5: Meta-observation (funny/relatable)

Day 2-3: Rotate variants of core themes

Day 4-5: New angles on same core messages

Day 6-7: Strongest performers repeated (audiences change)

**Why rotation matters:**
- Avoids repetition fatigue
- Reaches different audience segments
- Tests which angles resonate
- Maximizes algorithmic distribution
- Serves different objectives (awareness vs. conversion vs. community building)

**For Antimeme/Slow Content:**
In the Dark Forest era, virality is no longer automatically considered desirable. If an idea spreads too quickly, it might escape its original context; its meaning could become distorted. Calendar for antimemes should deliberately SLOW the posting rate vs. memes — quality over frequency, selected audiences over maximum reach.

### Secondary Account Strategy: The Jason Levin Model

Create a 2nd meme account to be goofy and make fun of people. If you're afraid to say something on the main account, do it on a 2nd account. Then if it blows up, blame the "social media intern."

**Real-World Example (Ukraine):**
Official account (hero narrative) + @uamemesforces (villain narrative) — two accounts serve different strategic purposes.

**Primary Account Standards:**
- ✓ Professional enough for your brand
- ✓ Defensible if directly asked
- ✓ Aligned with public persona
- ✓ No regrets if attributed to you

**Secondary Account Characteristics:**
- ⚠ More experimental/unhinged
- ⚠ Edgier humor or takes
- ⚠ Testing riskier angles
- ⚠ Plausible deniability ("intern" blame)

**Decision Rule:**
- Risk level LOW → Primary account
- Risk level MEDIUM → Depends on brand, probably primary
- Risk level HIGH → Secondary account

**Revenue Proof:**
1up built an IG page dedicated to sales memes and drove 1/3 of their revenue thanks to memes — secondary accounts can be business drivers, not just risk hedges.

### Measurement and Tracking

**Core Metrics to Track:**

1. **Reach Metrics:**
   - Impressions (how many saw it)
   - Retweets/shares (extended reach)
   - New followers (audience growth)

2. **Engagement Metrics:**
   - Likes/reactions
   - Replies/comments
   - Quote tweets
   - Engagement rate (engagement / impressions)

3. **Virality Signals:**
   - Which posts get 5-10x normal engagement?
   - Which get shared by influencers?
   - Which drive traffic/conversions?

4. **Trend Indicators:**
   - Week-over-week follower growth
   - Month-over-month reach increase
   - Content type performance (which types perform best)

**Tracking Method:**
- Spreadsheet with date, content, metrics
- Weekly review of what worked
- Monthly analysis of trends
- Quarterly performance vs. goals

### Adjustment Rules

**If Low Engagement (Underperforming):**
- Revisit content angle (is it missing?)
- Check timing (posting at wrong time?)
- Test new variant
- Increase frequency (maybe more volume helps)

**If High Engagement (Working):**
- Double down on successful angles
- Create more of that variant
- Same timing, same platform
- Build on momentum

**If No Change (Plateau):**
- Rotate content type
- Try new platforms
- Change timing
- Introduce new angle
- Test secondary account version

## Output Template

```markdown
## Content Calendar

**Campaign:** [What is being promoted?]
**Duration:** [Start date to end date]
**Accounts:**
- Primary: [@account]
- Secondary: [@account]

---

## Daily Posting Schedule

### Example Week:

**Monday:**
- 7:00am - [Tweet 1 - Villain narrative] (Primary)
- 11:00am - [Tweet 2 - Data/evidence] (Primary)
- 2:00pm - [Tweet 3 - Example story] (Primary)
- 6:00pm - [Tweet 4 - Question] (Primary)
- 9:00pm - [Tweet 5 - Meta] (Secondary)

**Tuesday:**
[Similar pattern, different content]

---

## Content Assignment

| Date | Time | Content | Platform | Account | Expected Reach |
|---|---|---|---|---|---|
| 3/16 | 7am | [Variant 1] | Twitter | Primary | [High] |
| 3/16 | 11am | [Variant 2] | Twitter | Primary | [Medium] |
| 3/16 | 2pm | [Variant 3] | LinkedIn | Primary | [Medium] |
| 3/16 | 6pm | [Variant 4] | Twitter | Primary | [High] |

---

## Account Assignments

**Variant 1 (villain narrative):** Primary (low risk)
**Variant 2 (data):** Primary (no risk)
**Variant 3 (unhinged humor):** Secondary (medium risk)
**Variant 4 (edgy take):** Secondary (high risk if backfires)

---

## Performance Tracking

**Weekly Metrics:**
- Total reach: [Track cumulative]
- Average engagement rate: [Engagement/impressions]
- Follower growth: [New followers per day]
- Viral posts (5x+ engagement): [Count and analyze]

**Monthly Review:**
- Best performing content type: [Data]
- Best performing time: [Data]
- Platform comparison: [Which platform performs best?]
- Adjustment: [Change for next month]

---

## Weekly Adjustment Rules

**If engagement < [baseline]:**
- Change to more proven angles
- Test new platform
- Increase frequency
- Revisit content quality

**If engagement > [target]:**
- Keep doing this
- Create more of this type
- Find variants of what works

**If plateau:**
- Rotate content
- Change timing
- Try new platform
- Introduce new angle
```

## Posting Calendar Example

```
Week of March 16, 2026

MONDAY 3/16
7:00am: "The problem with X is Y" [Villain angle] @Primary
11:00am: "Here's the data proving..." [Evidence angle] @Primary
2:00pm: "In my experience..." [Story angle] @LinkedIn
6:00pm: "What if we..." [Question for engagement] @Primary
9:00pm: "Only people in tech understand..." [Niche humor] @Secondary

TUESDAY 3/17
[Repeat with different content variants]

... [continues for full month]
```

## Common Execution Mistakes

**Mistake 1: Inconsistent Posting**
- You post 3 days on, 4 days off
- Algorithms penalize inconsistency
- Reach suffers
- Fix: Pre-schedule, automate if possible

**Mistake 2: Too Much Same Angle**
- All posts are same variant
- People get tired
- Reach declines
- Fix: Rotate through 3-5 variants

**Mistake 3: Ignoring Peak Times**
- You post whenever
- Missing peak engagement windows
- Lower reach than potential
- Fix: Research platform-specific peak times

**Mistake 4: Not Tracking Metrics**
- You post content but don't measure
- Don't know what works
- Can't optimize
- Fix: Track 3-5 key metrics

**Mistake 5: Forgetting Secondary Account Risk**
- You post risky content on primary
- Backfires
- Damages brand
- Fix: Use secondary account for high-risk variants

## When to Use This Skill

- **After craft-content → execute-calendar:** Schedule the approved content
- **Ongoing:** Weekly adjustment based on performance data

## References

See `/references/source-summary.md`:
- "Viral Content Tactics" for content strategy context
- "Practical Examples" for real campaign examples
- "Decision Frameworks" for when to scale posting
