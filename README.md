# Memetics Plugin for Claude and Cursor

A complete skill extraction and orchestration system for memetics — the science of idea spread, cultural transmission, and strategic communication.

## Installation

### Cursor

Clone the repo into your local Cursor plugins directory and restart Cursor:

```bash
git clone https://github.com/gnurio/memetics-plugin ~/.cursor/plugins/local/memetics-plugin
```

Cursor will automatically discover all 14 skills from the `skills/` directory.

### Claude Code

Clone the repo locally and add it as a plugin:

```bash
git clone https://github.com/gnurio/memetics-plugin
```

Then in your terminal, reference it for a session:

```bash
claude --plugin-dir ./memetics-plugin
```

Or add it permanently via the Claude Code TUI — open Claude Code and run:

```
/plugin add ./memetics-plugin
```

Claude Code will automatically discover all 14 skills from the `skills/` directory. Once this plugin is listed in a marketplace, you will also be able to install it with:

```bash
claude plugin install memetics-plugin
```

## What's Inside

This plugin extracts all actionable knowledge from "Memetics 101: Practical Guide" and related materials into atomic, reusable skills organized for intelligent orchestration.

### Directory Structure

```
memetics-plugin/
├── README.md (this file)
├── decomposition.md
│   └── Complete MECE skill decomposition with coverage matrix, dependency graph, I/O chains
├── references/
│   └── source-summary.md
│       └── Condensed source material organized by skill, with examples and definitions
└── skills/
    ├── orchestrate-memetics/
    │   └── SKILL.md (intelligent router for entire system)
    ├── classify-idea/
    │   └── SKILL.md (determine if idea is meme/antimeme/supermeme/cliche)
    ├── assess-fitness/
    │   └── SKILL.md (GO/NO-GO decision on spreading)
    ├── map-network/
    │   └── SKILL.md (recommend network topology)
    ├── design-strategy/
    │   └── SKILL.md (create phased spread strategy)
    ├── craft-content/
    │   └── SKILL.md (create viral content variants)
    ├── execute-calendar/
    │   └── SKILL.md (schedule content posting)
    ├── identify-champions/
    │   └── SKILL.md (find persistent advocates)
    ├── detect-supermeme/
    │   └── SKILL.md (identify parasitic supermemes)
    ├── evaluate-fitness/
    │   └── SKILL.md (measure transmission/immunity/symptomatic metrics)
    ├── transform-taboo/
    │   └── SKILL.md (gradual acceptance strategy for controversial ideas)
    ├── monitor-receptivity/
    │   └── SKILL.md (track readiness for phase advancement)
    ├── build-immunity/
    │   └── SKILL.md (strengthen network resistance)
    └── apply-domain/
        └── SKILL.md (adapt strategies to domains)
```

## Skills at a Glance

### Entry Points (Can Start Here)
- **orchestrate-memetics** - Router for any memetics question (recommended entry)
- **classify-idea** - Analyze what kind of idea you have
- **detect-supermeme** - Check if idea is parasitic
- **build-immunity** - Defensive memetics for networks

### Strategic Decision Skills
- **assess-fitness** - Should I try to spread this?
- **evaluate-fitness** - What are the exact metrics?
- **map-network** - How should I structure my network?

### Execution Skills
- **design-strategy** - Create complete action plan
- **identify-champions** - Find persistent advocates
- **transform-taboo** - Special handling for controversial ideas
- **craft-content** - Create shareable content
- **execute-calendar** - Schedule posting
- **monitor-receptivity** - Track when network is ready

### Adaptation Skills
- **apply-domain** - Tailor to personal branding, product launch, social movement

## How to Use

### Quick Start
1. **Start with orchestrate-memetics** if you're unsure what to do
2. **Or pick a specific skill** if you know what you need

### Full Workflow Example
```
User has idea
↓
orchestrate-memetics → routes to classify-idea
↓
classify-idea → outputs classification (meme/antimeme/supermeme/cliche)
↓
orchestrate-memetics → routes to assess-fitness
↓
assess-fitness → outputs GO or NO-GO decision
↓
[If GO] orchestrate-memetics → routes to identify-champions, map-network
↓
design-strategy → creates phased strategy
↓
craft-content + execute-calendar → creates and schedules content
```

### What You Get From Each Skill

Each skill SKILL.md file includes:

- **What it does** - Core purpose
- **Input/Output Contract** - What it accepts, produces, and passes to
- **Detailed Process** - Step-by-step how to use it
- **Examples** - Concrete examples from source material
- **Decision trees** - When to use which option
- **Common mistakes** - What not to do
- **Output templates** - Ready-to-use formats
- **References** - Links to relevant source material

## Key Features

### 1. Complete MECE Decomposition
- 10 confirmed skills fully supported by source material
- 4 speculative skills marked with [NEEDS SOURCE MATERIAL] gaps
- Every piece of source material mapped to exactly one skill
- No overlapping responsibilities

### 2. Explicit I/O Contracts
Each skill defines exactly what it accepts and produces, enabling intelligent orchestration and chaining.

### 3. Intelligent Orchestration
The orchestrate-memetics skill:
- Analyzes user requests to find entry points
- Routes to appropriate skills
- Chains outputs from skill to skill
- Accumulates context so later skills have full information
- Explains reasoning to user

### 4. Embedded Routing Logic
Skills know when to route to other skills and what conditions enable advancement:
- When to skip steps
- When to run skills in parallel
- When to accept NO-GO and explain why
- When to flag speculative skill gaps

### 5. Practical Examples
All skills use examples from the source material:
- Real memetic examples (viral tweets, political movements, etc.)
- Actual case studies (Ukraine meme warfare, 1up sales SaaS, etc.)
- Specific frameworks and decision trees

## What's Confirmed vs. Speculative

### Confirmed Skills (Complete Implementation)
1. **classify-idea** - Full classification procedure with matrix
2. **assess-fitness** - Complete GO/NO-GO framework
3. **map-network** - Detailed topology analysis
4. **design-strategy** - Full multi-phase strategies for both paths
5. **craft-content** - Complete content creation methodology
6. **identify-champions** - Full recruitment strategy
7. **detect-supermeme** - Complete red flag assessment and defense
8. **transform-taboo** - Full transformation timeline and tactics
9. **evaluate-fitness** - Assessment approach (though measurement methodology needs work)
10. **monitor-receptivity** - Framework (though specific indicators need detail)

### Speculative Skills (Scaffolding Provided)
These are marked with [NEEDS SOURCE MATERIAL] and include what's known plus explicit gaps:

1. **build-immunity** - Goal is clear, tactics need detailed methodology
2. **execute-calendar** - Recommendations clear, platform-specific optimization needs detail
3. **apply-domain** - Three domain overviews provided, each needs full detail
4. **monitor-receptivity** - Framework clear, measurement methods need specification

Each speculative skill shows:
- What IS known from the source
- Exactly what gaps exist
- How to complete it
- What it could accomplish with that information

## Gaps and Next Steps

To complete the speculative skills, the following source material is needed:

**Build Network Immunity:**
- Specific immunity-building curricula/exercises
- Frequency and duration of immunity training
- Measurement frameworks for immunity levels
- Integration with ongoing network operations

**Execute Content Calendar:**
- Platform-specific optimal posting times
- Content rotation patterns and formulas
- Secondary account decision criteria (detailed)
- Analytics tracking and adjustment algorithms

**Monitor Network Receptivity:**
- Specific behavioral indicators of receptivity change
- Quantitative measurement methods
- Decision rules for phase advancement
- False positive filtering methods

**Apply Domain:**
- Complete detailed playbooks for each domain
- Domain-specific metrics frameworks
- Domain-specific risk factors
- Domain-specific case studies

## Using This Plugin

### Installation
1. Copy the memetics-plugin directory to your skills folder
2. Each subdirectory under `/skills/` is a separate skill
3. The orchestrator routes between them automatically

### Starting a Memetics Project
1. **Use orchestrate-memetics** - Describe your situation
2. **Or go directly to a skill** - If you know what you need
3. **Review decomposition.md** - Understand skill relationships
4. **Reference source-summary.md** - For examples and context

### Key Decision Points
- **"Is this worth spreading?"** → assess-fitness
- **"What kind of idea is this?"** → classify-idea
- **"How do I structure my network?"** → map-network
- **"How do I create content?"** → craft-content
- **"Is this a supermeme trap?"** → detect-supermeme
- **"How do I build a movement?"** → design-strategy + monitor-receptivity
- **"My team is obsessed with something, help"** → build-immunity

## Philosophy

This plugin extracts skills, not opinions. Every skill:
- Traces back to specific source material
- Contains actionable, repeatable procedures
- Has clear inputs and outputs
- Knows when to route to other skills
- Identifies its own limitations

The system respects both:
- **MECE decomposition** - No overlaps, nothing missed
- **Speculative honesty** - Marks what's missing with [NEEDS SOURCE MATERIAL]

## Questions?

Refer to:
- **decomposition.md** - For understanding skill relationships
- **references/source-summary.md** - For definitions and examples
- **Individual skill SKILL.md files** - For detailed procedures
- **orchestrate-memetics SKILL.md** - For routing logic

---

*Generated from: Memetics 101 - Practical Guide, Difference between meme and cliche, Examples of memes antimemes and cliches*

*Using: skill-extractor process with full MECE decomposition, explicit I/O contracts, intelligent orchestration, and complete skill files*

*Status: 10/14 skills fully confirmed. 4 speculative skills with explicit gap markers.*
