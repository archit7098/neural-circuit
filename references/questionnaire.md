# The 24-Item Neural Circuit Intake

The operational screening instrument. **This mirrors `index.html` exactly** —
same items, scoring, normalization, and thresholds — so the web app and the
skill/project produce identical results. Use it to administer the intake in
conversation or to score answers a user pastes in.

## Answer scale (per item)

Rate each item for the **last 2 weeks**:

| Value | Label |
|---|---|
| 0 | Not at all / Never |
| 1 | Several days |
| 2 | More than half the days |
| 3 | Nearly every day |

- 4 items per circuit → 6 circuits → **24 items**.
- One **reverse-scored** item (Q14, marked ⤴): score it as `3 − answer`
  (so "Not at all" = 3 points of dysfunction, "Nearly every day" = 0).

## Items (grouped by circuit)

### Default Mode — `DMN` (Rumination)
1. Do you often get stuck in a "loop" of negative thoughts that you cannot voluntarily stop? *(Thought Patterns)*
2. Do you have trouble falling asleep specifically because your mind is racing? *(Sleep)*
3. Do you find yourself analyzing conversations or events long after they are over? *(Thought Patterns)*
4. Do you often miss parts of a conversation because you were lost in your own thoughts? *(Focus)*

### Salience — `SAL` (Anxious Avoidance)
5. Do you feel anxiety primarily in your body (e.g., racing heart, tight chest, stomach knots)? *(Physical Sensations)*
6. Are you easily overwhelmed or startled by bright lights, loud noises, or chaotic environments? *(Sensory Sensitivity)*
7. Do you avoid social situations mainly because they make you feel physically uncomfortable? *(Avoidance)*
8. Do you worry excessively about your health or specific physical sensations? *(Health Anxiety)*

### Negative Affect — `NEG` (Threat)
9. Do you often feel intense sadness, misery, or guilt? *(Mood State)*
10. Do you tend to expect the worst possible outcome in uncertain situations (catastrophizing)? *(Outlook)*
11. Are you extremely sensitive to criticism or feeling rejected by others? *(Rejection Sensitivity)*
12. Do neutral interactions often feel threatening or negative to you? *(Perception)*

### Positive Affect — `POS` (Reward)
13. Do you often feel "numb", "flat", or "empty" rather than explicitly sad? *(Mood State)*
14. ⤴ **(reverse-scored)** If you were told you won a prize today, would you feel genuine excitement? *(Reward Response)*
15. Have you lost interest in hobbies or activities you used to enjoy? *(Interest)*
16. Do you feel a lack of motivation or energy to start simple tasks? *(Motivation)*

### Attention — `ATT` (Inattention)
17. Do you have trouble reading a book or watching a movie without your mind drifting? *(Sustained Attention)*
18. Do you often feel lethargic, slow, or "checked out"? *(Energy Level)*
19. Do you find yourself "zoning out" even when you are trying to listen? *(Focus)*
20. Do you struggle to keep information in your head for short periods (forgetting why you walked into a room)? *(Working Memory)*

### Cognitive Control — `COG` (Cognitive Dyscontrol)
21. Do you struggle to make simple decisions, like what to eat for dinner? *(Decision Making)*
22. Do you feel like you can't control your emotional reactions (e.g., sudden anger or crying)? *(Emotional Regulation)*
23. Do you experience "brain fog" that makes it hard to think clearly? *(Clarity)*
24. Is it difficult for you to switch from one task to another? *(Cognitive Flexibility)*

## Scoring procedure

1. **Raw circuit score** = sum of that circuit's 4 items (apply the reverse rule
   to Q14). Range 0–12 per circuit.
2. **Normalized score (0–100%)** = `round(raw / 12 × 100)`.
3. **Primary finding** = the circuit with the highest normalized score.
4. **Relevance threshold** = a circuit is flagged clinically relevant at
   **≥ 40%**; report the primary circuit plus every other circuit ≥ 40% as
   secondary/co-occurring.

### Worked example

Raw `DMN = 10` → `round(10/12×100) = 83%` → above 40%, and if it is the max it is
the **primary finding**: Default Mode (Rumination) biotype.

## Reporting template

```
NEURAL CIRCUIT ASSESSMENT — SCREENING SUMMARY
Date: <date>

PRIMARY FINDING: <Circuit name> (<Alias>) — <score>%
  Mechanism: <one line from biotypes.md>
  Treatment considerations: <Rx / Tx from treatment-matrix.md>

CO-OCCURRING (≥40%):
  <Circuit>: <score>%  ...

ALL CIRCUITS: DMN <>%, SAL <>%, NEG <>%, POS <>%, ATT <>%, COG <>%

Note: Screening tool based on the Williams Neural Circuit Taxonomy.
Not a diagnosis. Assumes honest self-report. Share with a licensed clinician.
```

## Interpretation cautions

- The answer scale is **frequency-based**; item 14 is a hypothetical/capability
  question — score its *degree of endorsement* on the same 0–3 scale, then reverse.
- High scores across **many** circuits suggest either high symptom load or
  non-specific distress; weight the qualitative tie-breakers in
  `assessment-protocol.md` over raw percentages.
- The percentages are a **triage heuristic**, not a validated cut-off from the
  source study. Confirm with clinical interview and, where available, the
  behavioral proxies (WebNeuro/IntegNeuro) and scales (BRISC, SHAPS, GAD-7, CTQ).
