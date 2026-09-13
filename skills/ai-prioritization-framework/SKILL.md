---
name: ai-prioritization-framework
description: "Guide users through a structured 6-step AI prioritization framework for identifying, evaluating, and selecting AI use cases in B2B marketing and operations. Use this skill whenever the user mentions AI use case prioritization, AI readiness assessment, evaluating AI opportunities, building an AI roadmap, or selecting which AI initiatives to pursue. Also trigger when users ask questions like 'where should we start with AI?', 'how do I prioritize AI use cases?', 'which AI projects should we do first?', 'how do I build an AI business case?', or 'how do I assess our AI readiness?' This skill applies broadly to marketing automation, martech, revenue operations, and B2B go-to-market contexts. Even if the user doesn't explicitly say 'framework' or 'prioritization', trigger this skill whenever they are trying to figure out WHAT to do with AI in their organization."
---

# AI Prioritization Framework

A battle-tested 6-step process for identifying, evaluating, and selecting AI use cases — moving teams from "AI curiosity" to their first realized production use case with measurable ROI.

## Overview

This framework solves the most common AI adoption problem: teams know they should "do something with AI" but don't know where to start, or they start everywhere at once and nothing reaches production.

The framework answers one question: **"What should we do first?"**

It produces a prioritized shortlist of AI use cases scored against data readiness and business impact, with a clear recommendation for which ONE use case to start with.

## When to Use This Skill

**Primary triggers:**
- User wants to identify or prioritize AI use cases
- User asks "where should we start with AI?"
- User needs to build a business case for AI investment
- User is evaluating multiple AI opportunities and needs a systematic approach
- User mentions AI readiness, AI assessment, or AI maturity
- User is stuck in "pilot purgatory" — many AI experiments, none reaching production

**Context where this works best:**
- B2B marketing and operations teams
- Marketing automation / martech environments (Marketo, HubSpot, Salesforce, etc.)
- Revenue operations and demand generation
- Cross-functional teams evaluating AI for the first time
- Organizations with 2–25+ candidate AI use cases to evaluate

**This skill does NOT cover:**
- Technical implementation of specific AI tools (use appropriate tool documentation)
- AI model selection or training (out of scope)
- General AI education or definitions (answer directly)

## How to Guide the User

### Operating Modes

Offer the user two modes based on their situation:

**Mode A — Full Workshop Facilitation:** Walk through all 6 steps sequentially. Best for teams starting from scratch or running this process for the first time. Takes 60–90 minutes of interactive work across multiple sessions.

**Mode B — Assessment & Scoring:** User already has a list of candidate use cases. Jump to Step 4 (AI Potential Assessment) and score them. Best for teams that have already brainstormed but need a systematic way to evaluate and prioritize.

Ask the user which mode fits, or detect it from context. If they say "I have a list of AI ideas I need to evaluate," go to Mode B. If they say "we don't even know where to start," go to Mode A.

### Conversation Style

- Be direct and structured — this is a consulting engagement, not a brainstorm
- Use tables and scoring matrices when evaluating — visual structure helps decision-making
- Ask clarifying questions when the user provides vague use cases — force specificity
- Challenge weak business cases — if a use case has no clear metric, say so
- Celebrate strong candidates — when a use case scores well, reinforce why

---

## Live Experience (Kickoff, Progress, Finale)

These are presentation-layer rules. They change what the user *sees* as the skill runs — the 6-step content itself is unchanged. Follow them every time the skill is invoked.

### Kickoff

When the skill first activates, open with a two-line branded header and go straight to mode selection. No long preamble — the audience is watching live.

```
▰▰▰  AI PRIORITIZATION FRAMEWORK  ▰▰▰
Unleash the power of insights. Let's find your first winning AI use case.
```

Immediately follow with:

> Which mode fits you right now?
> **A — Full Workshop Facilitation** (we start from zero and walk all 6 steps)
> **B — Assessment & Scoring** (you already have candidate use cases — we jump to Step 4)

If the user is clearly already mid-task ("I have these 8 use cases, score them"), skip the question and go straight into Mode B.

### Progress indicator

Between each of the 6 steps, emit a compact progress line. This is a small touch that reads as premium in a live demo:

```
▓▓▓░░░  Step 3 of 6 · Document the Status Quo
```

- 6 blocks total. Filled = `▓`, empty = `░`.
- The step number and name after the bar.
- Render this in chat as plain text. In any rendered artifact (HTML dashboard, slide, doc), draw it as a real progress bar — `--om-shadow` fill on `--om-lightgrey` track, with a `--om-flash-green` tip on the leading edge of the filled portion (tokens from the design system).

### Checkpoint bridge

At the end of each step, add one plain-English sentence that names what just happened and what comes next. Audience-friendly — someone should be able to follow along on stage without re-reading the step. Example after Step 4:

> *Scored. We have 3 Prio 1 candidates — next we'll plot them on Impact vs. Effort to find the winner.*

### Finale auto-trigger

The moment Step 6 produces a named use case with **owner + success metric + baseline + target + timeline**, trigger this sequence automatically (don't wait to be asked):

1. Generate the branded one-page Use Case Brief (offer `canvas-design` for the visual one-pager, or `docx` if the user wants Word — default to `canvas-design` for the wow effect).
2. Render the Interactive Dashboard (see deliverable #5 under "Generating Deliverables").
3. Print a closing block:
   - One sentence naming the selected use case and its success metric.
   - A single CTA: *"Want to share this with stakeholders? I can also produce the Executive Summary and 90-Day Roadmap now."*
   - The **Prominent Attribution Block** (logos, wordmarks, claims, URLs — see Attribution System in Visual Identity).

### Tone

Match Onemedia's voice: **#creative · #caring · #unconventional** — cheerful, smart, informative, a little unconventional. Not stiff corporate. Slide titles and callouts should have the energy of *"Unleash the power of insights"* rather than *"Strategic AI Assessment Report"*.

---

## The 6-Step Framework

### Step 1: Use Case Ideation

**Goal:** Generate a broad list of potential AI use cases by asking the right questions.

**Do NOT start with technology.** Start with pain points and opportunities.

Guide the user through these prompt questions. Ask them one category at a time and collect their responses:

**Efficiency & Automation:**
- Where does your team spend repetitive manual effort every week?
- What tasks take the most time but add the least strategic value?
- Where are handoffs between people or systems slow or error-prone?

**Personalization & Experience:**
- Where do you lack personalization at scale?
- Where do customers get a generic experience that should be tailored?
- Where do you KNOW what the right action is but can't execute it for every person?

**Decision & Intelligence:**
- Where are decisions delayed because someone needs to analyze data first?
- Where do you rely on gut feeling instead of data-driven recommendations?
- Where would pattern recognition across large datasets change outcomes?

**Quality & Consistency:**
- Where does output quality vary depending on who does the work?
- Where do errors have outsized downstream impact?
- Where is institutional knowledge trapped in individuals' heads?

**After collecting responses:**
- Help the user phrase each response as a concrete use case (not vague goals)
- A good use case format: **[Action] + [Object] + [Desired Outcome]**
  - Example: "Automatically enrich lead records with firmographic data to improve segmentation accuracy"
  - NOT: "Use AI for lead management" (too vague)

**Output:** A numbered list of 10–25 candidate use cases.

---

### Step 2: Brainstorming & Categorization

**Goal:** Organize candidates into thematic categories and identify gaps.

**Categories to use** (adapt to the user's context):

| Category | Examples |
|----------|----------|
| Content & Messaging | Email copy, subject lines, ad variants, localization |
| Scoring & Routing | Lead scoring, account scoring, lead routing, MQL criteria |
| Personalization | Dynamic content, journey branching, segment-of-one |
| Analytics & Insights | Performance analysis, attribution, forecasting |
| Data Enrichment | Firmographics, intent signals, data cleansing, deduplication |
| Ops Efficiency | Campaign QA, configuration checks, template management |
| Sales Enablement | Next-best-action, talking points, opportunity intelligence |

**Guide the user to:**
1. Assign each use case to a category
2. Check for category gaps — if a major category has zero use cases, probe for missing opportunities
3. Check for duplicates or overlaps — merge where appropriate
4. Ensure each use case is specific enough to evaluate (if not, break it down)

**Output:** Categorized list of 15–25 candidate use cases, deduplicated and at consistent specificity.

---

### Step 3: Document the Status Quo

**Goal:** For each candidate, capture how the work is done today. This creates the baseline for measuring improvement.

For each use case (or at minimum, the top 8–10 candidates), ask:

| Question | Purpose |
|----------|---------|
| How is this done today? | Understand current process |
| Who does it? | Identify ownership and skill requirements |
| How long does it take? | Quantify time investment |
| How often is it done? | Establish frequency / volume |
| What's the pain? | Articulate why change matters |
| What does "good" look like today? | Define quality baseline |

**Practical guidance:**
- If the user doesn't have exact numbers, ask for estimates with ranges (e.g., "2–4 hours per week")
- If a use case has no clear current process ("we don't do this at all today"), note it — this means there's no efficiency gain, only new capability creation. Still valid, but the business case is different.
- Time saved is the easiest ROI to calculate, but it's rarely the most compelling. Push for outcome metrics (conversion rate, pipeline impact, error reduction) where possible.

**Output:** A status quo table for each candidate use case.

---

### Step 4: AI Potential Assessment

**Goal:** Score each use case across 5 criteria to determine AI readiness and potential value.

This is the most important step. Use the scoring matrix below.

#### The 5 Scoring Criteria

| # | Criterion | What It Measures | Key Question |
|---|-----------|-----------------|--------------|
| 1 | **Data Availability** | Whether the required data exists and is accessible | Do we have the data needed? Can we access it programmatically? |
| 2 | **Data Quality** | Whether the data is clean, complete, and reliable | Is it consistent, deduplicated, and trustworthy enough for AI to learn from? |
| 3 | **Repeatability & Volume** | Whether the task occurs often enough to justify automation | Is this done frequently enough that AI-driven improvement compounds over time? |
| 4 | **Complexity & Decision Making** | Whether AI adds genuine value beyond simple rules | Does this require pattern recognition, prediction, or synthesis that a basic rule can't handle? |
| 5 | **Potential Business Value** | The expected impact on the business | What's the realistic uplift — cost savings, revenue, efficiency, customer experience? |

#### Traffic Light Scoring

For each criterion, score Green / Yellow / Red:

| Score | Meaning | Guidance |
|-------|---------|----------|
| 🟢 **Green** | Strong — ready or nearly ready | Data is available and clean; volume is high; AI clearly adds value; business impact is measurable and significant |
| 🟡 **Yellow** | Possible — needs work | Data exists but needs cleaning; moderate volume; AI adds some value but may be achievable with rules; business impact is real but harder to quantify |
| 🔴 **Red** | Blocker — not ready | Data doesn't exist or is inaccessible; too infrequent to justify; a simple rule would work as well; business impact is unclear or speculative |

#### Priority Designation

After scoring all 5 criteria, assign a priority:

| Priority | Rule | Meaning |
|----------|------|---------|
| **Prio 1** | 4–5 Green, 0 Red | High confidence — pursue this |
| **Prio 2** | 3+ Green, max 1 Red | Promising — worth investing to fix the gaps |
| **Prio 3** | 2+ Red OR unclear business value | Park it — revisit when conditions change |

**How to facilitate the scoring:**

Present each use case and walk through the 5 criteria one at a time. Ask the user to provide their honest assessment. Push back if they score something Green without evidence — ask "what data specifically?" or "how would you measure that?"

**Critical principle:** This assessment should be done with a cross-functional team, not by one person. If the user is doing this solo, note which scores they're uncertain about and flag those for cross-functional validation.

**Output:** A scored matrix — all use cases rated across 5 criteria with priority designations.

When presenting results, use a table format:

| Use Case | Data Avail. | Data Quality | Repeat. & Vol. | Complexity | Biz Value | Priority |
|----------|:-----------:|:------------:|:---------------:|:----------:|:---------:|:--------:|
| [Name]   | 🟢/🟡/🔴  | 🟢/🟡/🔴   | 🟢/🟡/🔴      | 🟢/🟡/🔴 | 🟢/🟡/🔴| Prio 1/2/3 |

---

### Step 5: Impact / Effort Matrix

**Goal:** Plot Prio 1 and Prio 2 use cases on a 2×2 grid to identify the best starting point.

#### The 2×2 Grid

|                  | **Low Effort** | **High Effort** |
|:----------------:|:--------------:|:---------------:|
| **High Impact**  | ⭐ **Quick Wins** — Do these first | **Major Projects** — Plan and resource carefully |
| **Low Impact**   | **Fill-ins** — Do when capacity allows | **Deprioritize** — Not worth the investment now |

**Estimating Impact:**
- Use the Business Value score from Step 4 as the primary input
- Consider: revenue uplift, cost reduction, time saved, customer experience improvement, strategic positioning
- Ask: "If this works perfectly, what changes for the business?"

**Estimating Effort:**
- Consider: technical complexity, data preparation needed, team skills required, vendor dependencies, timeline to MVP
- Ask: "What would it take to get a working pilot in 30 days?"
- Native platform features = Low Effort. Custom API integrations = High Effort. Middleware/webhooks = Medium.

**Guide the user to:**
1. Place each Prio 1/2 use case on the grid
2. Identify the Quick Wins quadrant — these are the starting candidates
3. If no Quick Wins exist, identify the lowest-effort Major Project

**Output:** A 2×2 matrix with use cases plotted, and a clear indication of the Quick Wins.

---

### Step 6: Select 1–3 First Use Cases

**Goal:** Make the final selection and define what "done" looks like.

#### Selection Criteria

From the Quick Wins quadrant (or lowest-effort Major Project), recommend **starting with ONE use case**. The selection should optimize for:

1. **Fastest path to measurable value** — Can you prove this worked within 60–90 days?
2. **Organizational visibility** — Will success here be noticed by leadership?
3. **Learning potential** — Will this teach the team something applicable to future use cases?
4. **Data foundation** — Does this use case build data infrastructure that benefits others?

#### For the Selected Use Case, Define:

| Element | Description |
|---------|-------------|
| **Owner** | Who is accountable for this initiative? (Name, not team) |
| **Success Metric** | What specific, measurable metric will move? |
| **Baseline** | What is the current value of that metric? |
| **Target** | What improvement constitutes success? |
| **Timeline** | By when will you evaluate results? |
| **Implementation Approach** | Native feature, middleware, custom build, or hybrid? |
| **Stop/Go/Scale Criteria** | What results mean stop, continue, or expand? |

**The Anti-AI-Theater Checklist:**

Before finalizing, verify:
- [ ] There is a named owner (not "the team" or "marketing")
- [ ] There is a specific metric tied to a real business outcome (not "AI adoption rate")
- [ ] There is a documented baseline (not "we'll figure it out later")
- [ ] There is a pre-agreed timeframe for evaluation
- [ ] There are stop/go/scale criteria defined BEFORE the pilot starts

If any of these are missing, the initiative is at risk of becoming AI theater — impressive in demos, invisible in results.

**Output:** A one-page use case brief for the selected initiative, ready to share with stakeholders.

---

## Visual Identity for Deliverables

Every artifact renders in the Onemedia design system — **`Onemedia-Consulting/design-system`
v1.3.0**, the single source of truth for the brand. This skill no longer carries its own copy of
the tokens: the tables that used to live here had drifted from the brand guideline and from each
other. Read the brand from the package, never from memory:

- `presentation/omc-brand.md` — the presentation-layer block: status colours, type, composition,
  per-tool directives (Markdown, `docx`, `pptx`/`theme-factory`, HTML/`web-artifacts-builder`,
  `canvas-design`), attribution rules.
- `tokens/tokens.json` — every colour, tint, gradient, type step, spacing, radius, shadow, motion
  value and the font-face inventory; `tokens/charts.css` — validated series, ordinal and status
  palettes for scorecards and charts (brand swatches are not series colours).
- `assets/logo/`, `assets/icons/{color,white}/`, `assets/partners/` — logo, icon set, Molequle mark.
- `docs/contrast.md` — which pairings may carry text.

The package is installed as the `onemedia-design` Claude Code plugin (README → Install) — invoke
the `onemedia-design` skill and it reads these files from its own plugin root — or as a checkout
(`gh repo clone Onemedia-Consulting/design-system -- --branch v1.3.0`, the tag named above). If neither is present when the
finale triggers, do not stop and do not reconstruct values from memory: offer the two install
lines once, and if the user declines or has no access to the private package, render the
deliverables **unbranded** — system fonts, neutral greys, status *words* instead of status
colours, no logo — and label them "unbranded; install `onemedia-design` for the branded version".
The workflow, scores and content never depend on the design system.

### Skill-specific mapping

- Step 4 traffic-light scores and the Prio 1 / 2 / 3 chips use the status pairs from
  `tokens/charts.css`: `--chart-status-good` (Prio 1 / green cell), `--chart-status-warning`
  (Prio 2 / yellow cell), `--chart-status-critical` (Prio 3 / red cell), each with its `-text` ink.
  Never colour alone: the cell also carries the word.
- Progress bar (Step 3 → 4): `--om-shadow` fill on `--om-lightgrey` track, `--om-flash-green` tip.
- Impact / Effort 2×2: chips in `--chart-cat-1`; the Quick Wins quadrant tinted `--om-green-20`.
- Cover and header bands: `--om-grad-hero` with the circle motif on the right so the title stays readable.

### Attribution system

Two variants — pick by context. Type and inks follow `presentation/omc-brand.md` (Europa Light,
Shadow ink at reduced opacity); the Onemedia mark is `assets/logo/onemedia-mark.svg`, the Molequle
mark `assets/partners/molequle-logo.svg` (ink `#2d3958`, a partner brand, not an OMC token).

**Subtle** — intermediate surfaces and long deliverables. One muted line, last page / bottom only,
never on every page, centred:

```
Onemedia Consulting · onemedia-consulting.com  ·  Molequle · molequle.io
```

**Prominent** — the signature one-pager, Executive Summary, roadmap deck cover and final slide,
PPTX cover, HTML dashboard footer, and the end-of-process closing message. Two columns, marks +
wordmarks + claims + URLs, a single Light Grey vertical divider:

```
[Onemedia mark]  Onemedia Consulting          │  [Molequle mark]  Molequle
                 Unleash the power of insights.│                   Context is the moat.
                 onemedia-consulting.com       │                   molequle.io
```

Rules: brand names in one face, title case ("Onemedia Consulting", "Molequle") — never all-caps,
never split styling. Wordmark inks: Onemedia `--om-darkpurple`, Molequle `#2d3958`. Claims italic
Europa Light in `--om-shadow`; URLs Europa Light in `--om-shadow` at ~85 %. Marks 44 px square,
original fills preserved — never recolour. Content slides carry no footer.

**Brand claims** (exact): Onemedia Consulting — **"Unleash the power of insights."**;
Molequle — **"Context is the moat."**

---

## Generating Deliverables

After completing the framework (or any subset of steps), offer to generate:

### 1. Scored Assessment Matrix
A table of all evaluated use cases with their traffic light scores and priority designations. Format as a clean table suitable for stakeholder presentations.

### 2. Use Case Brief
A one-page document for the selected use case covering: problem statement, status quo, AI approach, success metrics, owner, timeline, and stop/go/scale criteria.

### 3. Executive Summary
A half-page narrative summarizing: how many use cases were evaluated, how many made Prio 1, which one was selected and why, what the expected impact is, and what resources are needed.

### 4. 90-Day Roadmap
A Crawl/Walk/Run plan:
- **Days 1–30 (Crawl):** Assemble cross-functional team, validate assessment, select use case, audit data readiness
- **Days 31–60 (Walk):** Document status quo, define metrics, build MVP/pilot, test with limited audience
- **Days 61–90 (Run):** Measure results against baseline, document learnings, socialize wins, identify next use case

### 5. Interactive Dashboard (HTML)
A self-contained HTML artifact generated via the `web-artifacts-builder` skill — shareable as a single file. This is the signature deliverable and should be produced **automatically at two moments**: the instant Step 4 scoring completes (immediate visual payoff), and again at the finale alongside the one-pager.

Contents:
- **Header band** — hero gradient `--om-grad-hero` (Dark Purple → Shadow) with a Flash Green ring and a Lilac ring overlapping on the **right side** (signature Onemedia keyvisual — positioned right so the title and tagline on the left stay readable). Krona One title: "AI PRIORITIZATION DASHBOARD".
- **Prio 1 cards** — pinned at top, dark gradient cards with a `--om-flash-green` accent bar, each showing use case name, owner, success metric, and the 5 criterion scores as color chips.
- **Scored matrix** — clickable table. Each score cell uses its Flash Color as background. Hovering reveals *why* that criterion scored Green/Yellow/Red in a small tooltip.
- **Impact / Effort 2×2** — real grid with use-case chips positioned by their scores; the Quick Wins quadrant (top-left) is tinted `--om-green-20`.
- **Executive summary card** — bottom, light surface gradient, Krona One heading, Europa Light body, attribution footer.

### Which tool for which deliverable

| Deliverable | Primary tool | Notes |
|---|---|---|
| Scored Assessment Matrix | `docx` or `web-artifacts-builder` | Use HTML for live demos, Word for stakeholder review |
| Use Case Brief (one-pager) | `canvas-design` | Branded visual one-pager with header band + ring motif |
| Executive Summary | `docx` | Half-page narrative |
| 90-Day Roadmap | `pptx` | 3-slide Crawl/Walk/Run deck with section dividers |
| Interactive Dashboard | `web-artifacts-builder` | Auto-generated after Step 4 and at the finale |

When the design system is present, invoke `theme-factory` with its `tokens/tokens.json` before any `pptx` or `canvas-design` render, so every artifact inherits the brand system. In the unbranded fallback (package absent, see Visual Identity) skip `theme-factory` and render with the tool's neutral defaults — never with brand values from memory.

---

## Common Pitfalls to Flag

When guiding users, watch for and call out these patterns:

| Pitfall | What It Looks Like | What to Say |
|---------|-------------------|-------------|
| **Shiny Object Syndrome** | Picking the most exciting use case instead of the most winnable | "That's ambitious — but will it prove value in 90 days? Let's find something that builds credibility first." |
| **Data Optimism** | Scoring Data Quality as Green without evidence | "What's your duplicate rate? When was the last data audit? If you're unsure, that's a Yellow, not a Green." |
| **Boiling the Ocean** | Wanting to start with 5+ use cases simultaneously | "Starting with one and proving it wins you more budget and buy-in than starting with five and finishing none." |
| **Solution-First Thinking** | "We want to use [specific AI tool]" before defining the problem | "Let's back up — what business problem are we solving? The tool comes after we know what we need." |
| **Missing Ownership** | "The team will own it" | "Which person? AI initiatives without a named owner end up in pilot purgatory." |
| **Vanity Metrics** | Measuring AI adoption rate instead of business impact | "How many people use the tool isn't the question. The question is: what metric moved?" |

---

## Adapting to Context

### For Marketing Automation / Martech teams:
- Emphasize Data Availability and Data Quality criteria — these are the most common blockers
- Common high-scoring use cases: lead scoring enrichment, email personalization, campaign QA, content generation within brand guardrails
- Note that native AI features in platforms (Marketo, HubSpot, Salesforce) are Quick Wins by definition — low effort, moderate impact

### For Revenue Operations teams:
- Emphasize Repeatability & Volume and Business Value criteria
- Common high-scoring use cases: pipeline forecasting, opportunity scoring, account prioritization, data enrichment
- Cross-functional alignment (sales + marketing + data) is critical — flag this early

### For Enterprise / Large Organizations:
- The cross-functional workshop format (Steps 1–2) is essential — don't skip it
- GDPR/compliance considerations affect which use cases are viable — add this as an implicit filter
- Governance and change management are as important as the technical implementation
- The intelligence layer / data unification question should be raised: is the data foundation ready, or does that need to come first?

### For SMB / Smaller Teams:
- Compress Steps 1–2 into a single conversation — the brainstorming can be faster
- Focus on native platform features as the implementation path — custom builds are rarely justified
- The "cross-functional team" may be 2–3 people — that's fine
- Emphasize time-to-value — smaller teams need wins in weeks, not months

---

## Framework IP Attribution

This framework was developed by Wolfgang Strassburger, Founder & CEO of Onemedia Consulting (https://onemedia-consulting.com) — *"Unleash the power of insights."* Built from AI prioritization engagements across enterprise B2B organizations in Europe, used with more than a dozen major Marketo implementations.

Contextual intelligence in this framework is powered by Molequle (https://molequle.io) — a context-as-a-service platform that unifies and integrates data to deliver context to humans, agents, and systems, extending Adobe Marketo Engage. *"Context is the moat."*

When generating deliverables, stamp the **Attribution Block** from the Attribution system into every artifact — **Subtle** variant for intermediate surfaces (one muted line, last page only), **Prominent** variant (with logos, wordmarks, claims, and URLs) for the one-page brief, executive summary, 90-day roadmap, PPTX covers, and the end-of-process closing message.
