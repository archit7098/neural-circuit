# Neural Circuit Biotypes — Precision Psychiatry Toolkit

A clinician-facing toolkit for identifying the **six neural-circuit biotypes of
depression and anxiety** (the Williams Neural Circuit Taxonomy; Stanford Precision
Mental Health; iSPOT-D) **without fMRI** — from symptoms, self-report scales, and
computerized cognitive proxies.

Developed by Dr. Archit Mehta. Grounded in the source document
*"Brain Circuits: Clinical Identification for Psychiatrists."*

> ⚠️ **Screening and education aid for licensed clinicians — not a diagnostic tool
> and not a medical device.** It does not prescribe, diagnose, or replace clinical
> judgment. Route acute risk (suicidal ideation, self-harm) to emergency services.

## Three ways to use this repo

### 1. Interactive web app
Open [`index.html`](index.html) in a browser (or host it — it's a single static
file). A patient completes the 24-item intake and gets a circuit profile, chart,
and shareable summary.

### 2. Anthropic Agent Skill (Claude Code / Agent SDK)
[`SKILL.md`](SKILL.md) + [`references/`](references/) form a self-contained
[Agent Skill](https://docs.claude.com/en/docs/agents-and-tools/agent-skills). To
install it for Claude Code, copy the skill into your skills directory:

```bash
# project-scoped
mkdir -p .claude/skills/neural-circuit-biotypes
cp SKILL.md .claude/skills/neural-circuit-biotypes/
cp -r references .claude/skills/neural-circuit-biotypes/

# or user-scoped: ~/.claude/skills/neural-circuit-biotypes/
```

The skill auto-triggers on neural-circuit / biotype / precision-psychiatry
questions, administers and scores the intake, differentiates look-alike
presentations, and surfaces biotype-matched treatment considerations.

### 3. Claude Project (claude.ai) knowledge connector
- Upload the four [`references/*.md`](references/) files (and optionally
  `SKILL.md`) as the Project's **knowledge**.
- Paste [`project/claude-project-instructions.md`](project/claude-project-instructions.md)
  into the Project's **custom instructions**.

The same content also works as knowledge for other assistants (custom GPTs, RAG
pipelines) — the `references/*.md` files are plain, self-describing Markdown.

## Repository layout

```
.
├── index.html                          # Interactive 24-item assessment web app
├── SKILL.md                            # Agent Skill entry point (frontmatter + overview)
├── references/                         # Progressive-disclosure knowledge (skill + project)
│   ├── biotypes.md                     #   Full per-circuit clinical reference
│   ├── questionnaire.md                #   24-item intake + scoring (matches index.html)
│   ├── treatment-matrix.md             #   Bedside biotype → Rx/Tx matrix
│   └── assessment-protocol.md          #   Triangulation workflow + differential tie-breakers
├── project/
│   └── claude-project-instructions.md  # Ready-to-paste Claude Project custom instructions
└── README.md
```

## The six biotypes

| Biotype | Alias | Mechanism | First-line Rx | SSRI-friendly? |
|---|---|---|---|---|
| Default Mode | Rumination | PCC↔mPFC hyperconnectivity | SSRI / Vortioxetine | Yes (can be sluggish) |
| Salience | Anxious Avoidance | Insula / dACC hyperactivity | SSRI + beta-blocker | Yes (+ autonomic dampener) |
| Negative Affect | Threat | Amygdala / sgACC hyperactivation | SSRI (escitalopram) | **Yes — classic responder** |
| Positive Affect | Reward | Striatal / VTA hypoactivation | DA agent (pramipexole/bupropion) | **No — SSRI-resistant** |
| Attention | Inattention | Fronto-parietal hypoconnectivity | SNRI (venlafaxine) | Prefer SNRI; Rx before therapy |
| Cognitive Control | Cognitive Dyscontrol | DLPFC / dACC dysfunction | SNRI / TMS | **No — ~38% vs ~47% remission** |

## Keeping the app and the knowledge in sync

`index.html` and `references/questionnaire.md` intentionally encode the **same**
24 items, scoring, reverse-scoring rule, normalization, and 40% relevance
threshold. If you change one, change the other so the web app and the
skill/project agree.

## Source & license

Clinical content is derived from *"Brain Circuits: Clinical Identification for
Psychiatrists"* (Williams Neural Circuit Taxonomy; Stanford Center for Precision
Mental Health; iSPOT-D). For educational and clinical decision-support use only.
Not a medical device.
