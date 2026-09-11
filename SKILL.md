---
name: neural-circuit-biotypes
description: >-
  Clinical decision-support reference for identifying the six neural-circuit
  biotypes of depression and anxiety (the Williams / Stanford Precision
  Psychiatry taxonomy) WITHOUT fMRI. Use whenever a user asks to identify,
  screen, differentiate, or select treatment for a patient across the Default
  Mode (Rumination), Salience (Anxious Avoidance), Negative Affect (Threat),
  Positive Affect (Reward), Attention (Inattention), or Cognitive Control
  (Cognitive Dyscontrol) biotypes; to administer or score the 24-item circuit
  intake; to map symptoms/behavioral proxies (WebNeuro, BRISC, SHAPS, Go/NoGo,
  Emotion ID) to a circuit; or to reason about biotype-matched pharmacology and
  psychotherapy (e.g. why SSRIs underperform in the Cognitive Control and
  Positive Affect biotypes). Clinician-facing screening/education aid — not a
  diagnostic device.
license: For educational and clinical decision-support use only. Not a medical device.
---

# Neural Circuit Biotypes — Clinical Identification

A structured reference for **precision-psychiatry phenotyping**: sorting patients
with depression/anxiety into six neural-circuit biotypes using only bedside
symptoms, self-report scales, and computerized cognitive proxies — no
neuroimaging required.

Source of truth: *"Brain Circuits: Clinical Identification for Psychiatrists"*
(Williams Neural Circuit Taxonomy; Stanford Center for Precision Mental Health;
iSPOT-D). This skill and the repo's `index.html` intake app are both derived
from that document.

## What this skill is for

- **Identify a biotype** from a clinical description, symptoms, or intake answers.
- **Administer / score** the 24-item circuit questionnaire in conversation.
- **Differentiate** look-alike presentations (e.g. Default-Mode "distraction" vs
  Attention "drifting"; Negative-Affect "misery" vs Positive-Affect "numbness").
- **Map behavioral proxies** (WebNeuro/IntegNeuro tasks, BRISC, SHAPS, GAD-7,
  CTQ) to the underlying circuit.
- **Reason about biotype-matched treatment** (pharmacology + psychotherapy),
  including where standard SSRIs are expected to underperform.

## The six biotypes at a glance

| Biotype | Alias | Core mechanism | One-line tell | First-line Rx |
|---|---|---|---|---|
| **Default Mode** | Rumination | PCC ↔ mPFC intrinsic **hyper**connectivity | "I can't shut my mind off"; initial insomnia | SSRI / Vortioxetine |
| **Salience** | Anxious Avoidance | Anterior insula / dACC **hyper**activity | Anxiety felt **in the body**; avoidance, startle | SSRI + beta-blocker |
| **Negative Affect** | Threat | Amygdala / sgACC **hyper**activation | Intense misery, catastrophizing, rejection-sensitive | SSRI (escitalopram) |
| **Positive Affect** | Reward | Ventral striatum / VTA **hypo**activation | "Numb/empty", anhedonia, no motivation | DA agent (pramipexole/bupropion) |
| **Attention** | Inattention | Fronto-parietal **hypo**connectivity | Can't focus, lethargic, "zoning out" | SNRI (venlafaxine) |
| **Cognitive Control** | Cognitive Dyscontrol | DLPFC / dACC dysfunction | "Brain fog", decision paralysis, impulsivity | SNRI / TMS |

Two clinically critical facts to keep front-of-mind:

1. **Positive Affect** and **Cognitive Control** biotypes respond **poorly to
   SSRIs** (serotonin can further blunt striatal dopamine; the "cognitive
   biotype" remits at ~38% on SSRIs vs ~47% for others). These are the patients
   for whom trial-and-error SSRI prescribing wastes months.
2. Biotypes **cut across DSM labels** and can **co-occur**. Report a primary
   circuit plus any secondary circuits above threshold, not a single diagnosis.

## How to use this skill

Load the reference file that matches the task (progressive disclosure — don't
read them all up front):

- **`references/biotypes.md`** — Full per-circuit reference: neuroanatomy,
  pathophysiology, symptom profile, non-radiological assessment tools, and
  treatment implications. Read this to identify a biotype from a narrative or to
  explain a mechanism.
- **`references/questionnaire.md`** — The 24-item intake (4 items/circuit),
  answer scale, reverse-scoring rule, normalization, and thresholds — matching
  the `index.html` app exactly. Read this to administer or score the assessment.
- **`references/treatment-matrix.md`** — The "bedside biotype matrix": complaint
  → behavioral sign → proxy test → scale → preferred Rx/Tx, on one page.
- **`references/assessment-protocol.md`** — The triangulation workflow (symptom
  cluster + BRISC + WebNeuro proxy) and the differential-diagnosis tie-breakers.

### Recommended workflow

1. **Gather** the presentation (free-text history, or run the 24-item intake from
   `questionnaire.md`).
2. **Score / cluster** into the six circuits; identify the primary (highest) and
   any secondary circuits at/above threshold.
3. **Differentiate** ambiguous cases using the tie-breakers in
   `assessment-protocol.md` (e.g. internal vs external distractibility; misery vs
   numbness; slowed-vs-fast reaction to threat faces).
4. **Surface treatment considerations** from `treatment-matrix.md`, flagging
   biotypes where SSRIs are expected to underperform.
5. **Frame the output** as screening/decision-support for a prescribing
   clinician — never as a diagnosis or a prescription.

## Safety and scope guardrails

- This is a **screening and education aid for clinicians**, not a diagnostic
  tool and not a medical device. Do not present output as a diagnosis.
- **Do not prescribe.** Name treatment *considerations* from the taxonomy and
  defer medication decisions to a licensed prescriber who can weigh history,
  contraindications, and interactions.
- Results assume honest self-report and do not replace clinical interview, risk
  assessment, or fMRI where indicated.
- If a user describes **acute risk** (suicidal ideation, self-harm, danger to
  others), prioritize directing them to emergency/crisis resources over biotype
  scoring.
- Keep patient information confidential; do not send it to unrelated services.
