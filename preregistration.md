# POST-DATA-COLLECTION TRANSPARENCY PROTOCOL & RECONSTITUTED ANALYSIS PLAN
Project Title: Kinematic Speed in Attentional Control Settings: Contingent Capture in Inattentional Blindness


### 1. Statement Regarding Preregistration History
An initial preregistration was drafted on OSF (Repository: https://osf.io/c5v6g/) prior to the completion of data collection. 
Due to an inadvertent manipulation error on the platform interface, the original registration 
entry was corrupted/deleted. 
In strict compliance with Open Science and Level 1 TOP guidelines (Lakens, 2024; Simmons et al., 2011), 
we declare this document not as an original prospective preregistration, but as a fully transparent, 
reconstituted documentation of the intended experimental protocol, the actual analytical pipeline, 
and all departures from the initial plan.

### 2. Confirmatory Hypotheses
1. Attentional Set Velocity Congruence (Primary Hypothesis):
   Detection rates of the unexpected critical stimulus will be significantly higher when its velocity 
   matches that of the tracked targets compared to when it matches the velocity of the ignored distractors 
   (Match vs. Mismatch condition).
2. Pure Exposure Duration / Velocity Salience (Secondary / Replicative Test):
   Isolated physical velocity (and its concomitant display duration: 10.25 s for slow vs. 4.10 s for fast) 
   will not predict noticing once velocity is task-relevant, contrary to pure exposure duration accounts (Kreitz et al., 2016).

### 3. Design and Manipulations
- Design: 2 (Target Velocity: 80 px/s [slow] vs. 200 px/s [fast]) x 2 (Critical Stimulus Velocity: 80 px/s vs. 200 px/s).
- Primary Task: Multiple Object Tracking (MOT) requiring mental counting of edge bounces of 4 targets among 4 distractors 
  across a fixed 800 x 600 px canvas (refresh rate: 60 ± 2 Hz).
- Critical Trial (Trial 3): An unexpected black circle (radius 20 px) enters from the right edge after 10 s, moving horizontally 
  to the left edge.

### 4. Sampling and Exclusion Criteria
- Target sample size: ~300 initial submissions to obtain >= 100 evaluable participants after standard inattentional blindness attrition.
- Primary Inclusion Criteria:
  a. >= 80% counting accuracy on pre-critical trials (Trials 1-2);
  b. Detection of the unexpected stimulus on the full-attention control trial (Trial 5);
  c. Self-reported absence of prior familiarity with inattentional blindness paradigms.
- Strict Noticer Demarcation:
  A participant is categorized as a conscious noticer only if they answer "YES" to the unexpected event probe on Trial 3.1 
  AND correctly report both the motion direction (right-to-left) and velocity category.

### 5. Documented Protocol Departures & Rationales
1. Factorial Model vs. Collapsed Match/Mismatch Contrast:
   - Initial plan: Evaluation of 4 independent cells.
   - Revised implementation: Full 2 x 2 factorial binomial GLM testing the interaction (Target Speed x Stimulus Speed), 
     complemented by the targeted Match vs. Mismatch congruence contrast.
   - Rationale: Collapsing into Match vs. Mismatch directly tests the relational contingent capture hypothesis 
     (Folk et al., 1992) and preserves statistical power against sample attrition.
2. Multiverse Specification:
   - A 320-pipeline multiverse analysis was instituted post hoc to demonstrate that statistical conclusions do not 
     hinge on the specific 80% accuracy cutoff or the inclusion of full-attention deniers.
3. Online Primary-Task Cost in Non-Noticers:
   - Analysis of tracking decrement on Trial 3.1 restricted strictly to observers who failed to detect the unexpected stimulus.

All raw data, analysis scripts (R Markdown/Quarto), and jsPsych experimental code remain permanently public and accessible.
