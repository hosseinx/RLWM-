# RLWM + spatial conflict (Simon-based)
RLWM with cognitive conflict extention task (online)
**Task Overview**
A cognitive task combining Reinforcement Learning (RL), Working Memory (WM) load, and the Simon Effect (response conflict). The design is based on the interactive RLWM model (Collins, 2018) with the addition of spatial response conflict.
**1. Task Structure & WM Load**
Total Blocks: 14 blocks.
**WM Load Conditions:**
Low Load: 8 blocks with Set Size = 3.
High Load: 6 blocks with Set Size = 6.
Block Constraints: The very first and the very last blocks must be Low Load (Set Size = 3).
Stimuli: Each block features a distinct semantic category (e.g., animals, fruits). Each category contains 3 or 6 unique stimuli, each mapped to a fixed correct response.
**2. Learning Mechanism & Timing**
Learning: Participants learn stimulus-response mappings via trial-and-error.
Feedback: Binary feedback (+1 for correct, 0 for incorrect) is provided after each response.
Timing: Fixation cross (500 ms) ➔ Stimulus presentation (1500 ms) ➔ Feedback (500 ms).
**3. Simon Effect & Trial Design**
Spatial Conflict: Stimuli appear pseudo-randomly on the left or right side of the screen.
Response Keys: 'Z' for left, 'M' for right.
Congruency: Each block contains an equal 50/50 split of congruent (stimulus location matches correct response side) and incongruent trials.
Trial Distribution: Trials are pseudo-randomized with equal repetitions per stimulus within a block (e.g., 12 repetitions per stimulus).
**4. Practice & Data Logging**
Practice: Unrecorded practice trials are administered before the main task begins.
Logged Variables (per trial):
    Block number
  Trial number
  Stimulus ID
  Stimulus position (left/right)
  Correct response
  Given response
  Congruency (congruent/incongruent)
  Set size (3 or 6)
  Accuracy (correct/incorrect)
  Reaction Time (RT)
