# RECONSTITUTED POST-DATA-COLLECTION TRANSPARENCY PROTOCOL & RECONSTRUCTED ANALYSIS PLAN
**Repository (GitHub):** https://github.com/EmilienB-Bop/preregistration_inattentional_blindness_brochet_1
**Permanent Archive & DOI (Zenodo):** https://doi.org/10.5281/zenodo.[RECORD_ID]
**Original OSF Overview Container:** https://osf.io/c5v6g/overview
**Target Journal:** *Psychonomic Bulletin & Review* (Empirical Brief Report)
**Study Title:** Kinematic Speed in Attentional Control Settings: Contingent Capture Outweighs Exposure Duration in Inattentional Blindness
**Authors:** Emilien Brochet, Julien Tardieu, & Céline Lemercier
**Institutional Affiliation:** CLLE (CNRS, Université de Toulouse Jean Jaurès), MSHS-T, France
**Institutional Ethics Approval:** CER Université de Toulouse (CER 2025-1048)
**Date of first Deposit on OSF:** 26 March 2025

---

## 1. FORMAL STATEMENT CONCERNING PREREGISTRATION INTEGRITY & POST-DATA ARCHIVING

### 1.1 Technical Incident & Status of Preregistration
An a priori prospective preregistration was drafted and initiated on the Open Science Framework (OSF) prior to the completion of data harvesting. Due to an unintended platform manipulation error, the internal timestamped registration record was deleted, leaving only the project overview container (https://osf.io/c5v6g/overview).

In strict adherence to Open Science standards, Level 1 Transparency and Openness Promotion (TOP) guidelines, and standard methodological recommendations (Lakens, 2024; Simmons et al., 2011), the authors state that:
1. **This document is NOT a prospective a priori preregistration.** It is a post-data-collection transparency protocol.
2. It explicitly documents: (a) what was originally tested in the empirical study; (b) the critique and evaluation points raised during initial peer review (Cognition submission); (c) the empirical justifications for each post-hoc analytical specification; and (d) the archiving of all raw materials via GitHub and Zenodo.
3. To ensure long-term, immutable traceability, this file and the underlying code/data pipelines are placed under version control on GitHub and minted with a citable, permanent DOI via Zenodo.

---

## 2. STUDY DESIGN & INITIAL PROTOCOL (AS TESTED)

### 2.1 Theoretical Rationale
The experiment investigated whether kinematic motion velocity—a continuous and computationally distinct visual dimension—can operate as an endogenous dimension of an observer's attentional control settings (attentional set), or whether detection of an unexpected event is driven strictly by bottom-up salience or physical exposure duration (Kreitz et al., 2016; Most et al., 2005; Wallisch et al., 2023).

### 2.2 Factorial 2 × 2 Design
A between-subjects 2 × 2 factorial design crossed:
1. **Target Velocity / Attended Speed:** Slow (80 px/s) vs. Fast (200 px/s).
2. **Critical Stimulus Velocity:** Slow (80 px/s) vs. Fast (200 px/s).

- **Apparatus & Canvas:** Fixed 800 × 600 px canvas rendered with jsPsych (v7.3) hosted on Cognition.run, running on desktop/laptop displays at 60 ± 2 Hz (mobile/tablet devices screened out).
- **Dynamic Array:** 8 black circles (radius r = 20 px). 4 circles served as targets (moving at the attended speed) and 4 as distractors (moving at the alternate speed). Circles rebounded elastically off canvas borders.
- **Critical Trial (Trial 3):** An unexpected 9th black circle (r = 20 px) entered horizontally from the right boundary at y = 300 px after 10.0 s and traversed to the left edge:
  - *Slow unexpected stimulus (80 px/s):* Physical display exposure duration ≈ 10.25 s.
  - *Fast unexpected stimulus (200 px/s):* Physical display exposure duration ≈ 4.10 s.

### 2.3 Procedure & Trial Structure
1. **Interactive Demo & Training:** Two 20-second tracking practice trials (targets and distractors identified via initial green/red coloring). Observers required ≥ 80% counting accuracy on two consecutive trials before proceeding.
2. **Trials 1 and 2 (Pre-critical):** 30-second tracking trials without the unexpected stimulus. Mental counting of target edge bounces reported at trial offset via text input.
3. **Trial 3 (Critical Trial 3.1):** MOT task with the unexpected circle traversing the screen.
   - Target bounces reported first.
   - Explicit detection probe: *"Did you notice anything unusual during this trial?"* (YES / NO).
   - If YES: Forced-choice identification of trajectory (right-to-left, vertical, diagonal, random) and velocity (very slow, slow, fast, very fast), each accompanied by a 0–100 continuous confidence slider.
   - If NO: Trial repeated up to twice (Trials 3.2 and 3.3).
4. **Trial 4 (Divided-Attention):** MOT tracking with the unexpected stimulus presented again.
5. **Trial 5 (Full-Attention Control):** Passive viewing without tracking or bounce counting.
6. **Prior Knowledge Assessment:** Forced-choice probe evaluating prior familiarity with inattentional blindness or the "invisible gorilla" experiment.

---

## 3. PEER REVIEW FEEDBACK (COGNITION EVALUATION) & CORRESPONDING METHODOLOGICAL DEVIATIONS

Following evaluation by three expert reviewers and the handling editor at *Cognition* (here this original draft submited: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=6677514), several substantial concerns were identified regarding theoretical framing, analytical choices, and transparency. Below is an itemized breakdown of reviewer critique and the exact analytical adjustments implemented in response:

### 3.1 Theoretical Status of Kinematic Velocity & Theoretical Claims
- **Reviewer Feedback (R1, R2, R3, Editor):** Reviewers noted that testing whether speed affects capture is not inherently surprising if framed as an arbitrary feature, and questioned the contribution relative to Kreitz et al. (2016) and Wallisch et al. (2023). Reviewers also warned against overstated claims ("gates access to conscious perception", "absolute barrier").
- **Protocol Adjustment:** 
  1. The theoretical justification was sharpened: prior studies manipulated speed *exogenously* (speed was not task-defining), leading to conflicting findings across paradigms (exposure duration vs. fast salience). Here, speed is the *endogenous* selection criterion.
  2. Language has been moderated throughout: kinematic speed modulates the threshold of conscious access and imposes dynamic constraints on selective attention within a continuous sensitivity gradient (Nartker et al., 2025).

### 3.2 Factorial Model (2 × 2) vs. Collapsed Match/Mismatch Contrast
- **Reviewer Feedback (Editor, R3):** The study originally set up four conditions, but the empirical text reported a collapsed two-group comparison (Match vs. Mismatch) without fully clarifying the departure from the original factorial structure.
- **Protocol Adjustment:** 
  1. Both statistical levels are reported simultaneously and transparently:
     - The full 2 × 2 binomial generalized linear model (*Target Speed* × *Stimulus Speed*) yielding a significant interaction, χ²(1) = 5.42, p = .020 (Wald z = 2.03, p = .042).
     - The planned focused congruence contrast (*Match* vs. *Mismatch*), yielding χ²(1) = 5.12, p = .024, OR = 0.19, 95% CI [0.03, 0.78].
  2. Theoretical justification: collapsing identical speed pairs directly tests relational contingent capture (feature congruence with the attentional set across both velocity baselines) while preserving statistical power against experimental attrition.

### 3.3 Quantification of the Null Effect of Pure Exposure Duration
- **Reviewer Feedback (R2, R3):** The non-significant difference between slow and fast stimuli in isolation (7.46% vs. 9.80%, p = .652) was claimed to refute exposure-duration accounts without quantifying evidence for the null ("absence of evidence is not evidence of absence").
- **Protocol Adjustment:** 
  1. Default Bayesian binomial analysis (Cauchy prior r = 0.707) was computed, yielding BF₀₁ = 4.12 in favor of the null hypothesis of speed invariance over Kreitz et al.'s exposure account.
  2. Two One-Sided Equivalence Tests (TOST) against the moderate effect size (φ = 0.24) observed by Kreitz et al. confirmed statistical equivalence within bounds Δ = ± 12% (p_TOST = .018).

### 3.4 Direct Interaction Test on Primary-Task Accuracy Cost (Non-Noticers)
- **Reviewer Feedback (R2):** The reported tracking accuracy cost on Trial 3 was claimed to reflect pre-conscious capture, but lacked a formal interaction model and needed strict restriction to non-noticers.
- **Protocol Adjustment:**
  1. Analysis was restricted strictly to confirmed *non-noticers* on Trial 3.1 (n = 108).
  2. A formal linear mixed-effects model testing the interaction:
     `Accuracy ~ Period (Pre-critical vs. Critical 3.1) × Condition (Match vs. Mismatch) + (1 | Subject)`
     was fitted, demonstrating a significant interaction, F(1, 106) = 4.88, p = .029, η_p² = .044.
  3. Non-noticers in the match condition suffered a significant accuracy decrement (p = .014), whereas mismatch non-noticers showed no decline (p = .781, BF₀₁ = 6.81).

### 3.5 Sample Demographics & Online Display Constraints
- **Reviewer Feedback (R1, R3):** Real demographic distributions were missing from the text, and online display variability (lack of millimeter visual angle calibration, lack of gaze-tracking) was insufficiently discussed.
- **Protocol Adjustment:**
  1. Full demographic distributions were inserted:
     - Uncurated recorded cohort (N = 285): 182 females, 96 males, 4 non-binary, 3 undisclosed; ages 18–25 (n = 212), 26–35 (n = 41), 36–50 (n = 21), ≥51 (n = 11).
     - Confirmatory analytical sample (N = 118): 78 females, 38 males, 2 non-binary; ages 18–25 (n = 94), 26–35 (n = 15), 36–50 (n = 6), ≥51 (n = 3).
  2. Methodological caveats are explicitly stated: browser frame-rate filtering (60 ± 2 Hz) and desktop enforcement were applied, but unmonitored online settings precluded remote eye-tracking to guarantee strict foveal cross fixation.

### 3.6 Inattentional Amnesia & Cognitive Neuroscience Integration
- **Reviewer Feedback (R3):** Reviewer suggested discussing inattentional amnesia (Wolfe, 1999) and integrating neuroscientific ERP/fMRI evidence (e.g., Pitts et al., 2012; Dellert et al., 2021).
- **Protocol Adjustment:**
  1. Addressed in Discussion: online primary-task tracking cost operates as a concurrent behavioral marker recorded during stimulus presentation, arguing against pure retrospective memory decay.
  2. Neuroimaging literature on visual awareness negativity (VAN) and late frontoparietal ignition (P3b) is integrated to contextualize how attentional sets modulate sensory gain in area MT/V5 prior to explicit report.

### 3.7 Elimination of Textbook Boxes & Ambiguous Acronyms
- **Reviewer Feedback (R1, R3):** Excised all pedagogical callout boxes (Box 1, Box 2, Box 3). Banned the ambiguous acronym "US" (commonly used for unconditioned stimulus), replacing it uniformly with "unexpected stimulus" or "unexpected circle". Standardized all Methods and Results verbs into the past tense.

---

## 4. CONFIRMATORY SAMPLING, FILTERING & MULTIVERSE PIPELINE

### 4.1 Sample Size Planning
- A priori target power: (1 - β) = .90, α = .05, two-tailed test based on Kreitz et al. (2016, φ = 0.241), requiring N = 108–120 evaluable participants.
- A fixed stopping rule was set at ~300 initial online submissions to accommodate anticipated >50% attrition from standard IB filters.
- Total unique sessions collected: N = 290.

### 4.2 Inclusion and Exclusion Criteria (Canonical Pipeline)
To be retained in the primary confirmatory sample (N = 118; Match: n = 54; Mismatch: n = 64):
1. **Primary-task compliance:** Average bounce-counting accuracy ≥ 80% across pre-critical trials (Trials 1 and 2).
2. **Full-attention detection:** Detection and feature reporting on Trial 5.
3. **Naivety:** Absence of prior familiarity with inattentional blindness paradigms.
4. **Strict Noticer Definition:** Affirmative response ("YES") on Trial 3.1 combined with accurate forced-choice reporting of both motion direction (right-to-left) and velocity category.

### 4.3 Multiverse Robustness Specification (320 Pipelines)
To ensure empirical conclusions do not depend on arbitrary operational decisions, a 320-universe multiverse analysis was computed across:
- Prior knowledge: Exclude familiar observers vs. retain all (2 options).
- Counting accuracy threshold: No filter vs. 20% to 80% cutoffs in steps of 10% (8 options).
- Full-attention trial: Exclude deniers vs. retain deniers (2 options).
- Detection threshold: 10 graded levels from simple "YES" report to multi-attribute accuracy across attempts 1–3 (10 options).

**Multiverse Summary:**
- 105 of 320 universes reached statistical significance (p < .05).
- 98 of these 105 significant pipelines (93.3%) yielded odds ratios strictly below 1.0 (canonical model: OR = 0.19, p = .026), substantiating the robust detection advantage of the match condition.
- The 7 universes (6.7%) exhibiting an inverted effect (OR > 1.0) shared an indefensible operational profile: retaining prior-knowledge participants, retaining full-attention deniers, and scoring detection only on the third critical attempt (Trial 3.3).

---

## 5. COMPUTATIONAL REPRODUCIBILITY & ARCHIVE CONTENTS
All files are archived in the repository and minted with a permanent Zenodo DOI:
1. `datasethighspeed5.csv` and `datasetlowspeed5.csv`: Raw data tables exported from Cognition.run.
2. `dataset_combined.csv`: Harmonized analysis dataset across Trials 1 to 5.
3. `high speeded targets.js` and `low speeded targets.js`: Full jsPsych experimental scripts.
