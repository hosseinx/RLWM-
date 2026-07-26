# Interactive RLWM Task with Simon Effect

A cognitive task combining **Reinforcement Learning (RL)**, **Working Memory (WM) load**, and the **Simon Effect** (response conflict). 

The design is based on the interactive RLWM model ([Collins, 2018]) with the addition of a spatial response conflict mechanism to investigate the interaction between cognitive control, memory load, and learning.

---

## 🧠 Task Overview

Participants learn stimulus-response mappings via trial-and-error. The task manipulates working memory load (via set size) and introduces spatial response conflict (Simon effect) to measure cognitive control and learning dynamics under varying cognitive demands.

### Key Features
- **Learning Mechanism:** Trial-and-error reinforcement learning with binary feedback.
- **WM Load Manipulation:** Low load (Set Size = 3) vs. High load (Set Size = 6).
- **Response Conflict:** Simon effect integrated into all trials.
- **Semantic Categorization:** Distinct stimulus categories (e.g., animals, fruits) per block.

---

## 🏗️ Task Structure

The experiment consists of **14 blocks** in total. 

| Condition | Set Size | Number of Blocks | Notes |
| :--- | :---: | :---: | :--- |
| **Low WM Load** | 3 | 8 | First and last blocks **must** be Low Load. |
| **High WM Load** | 6 | 6 | - |

- **Stimuli:** Each block features a distinct semantic category. Within a block, each unique stimulus is mapped to a fixed correct response.
- **Trial Distribution:** Trials are pseudo-randomized. All stimuli appear an equal number of times per block (e.g., 12 repetitions per stimulus).

---

## ⏱️ Trial Timeline & Mechanics

Each trial follows a strict temporal sequence:

1. **Fixation Cross:** `500 ms`
2. **Stimulus Presentation:** `1500 ms` (Appears on the left or right side of the screen)
3. **Feedback:** `500 ms` (`+1` for correct, `0` for incorrect)

*Note: Unrecorded practice trials are administered before the main task begins to familiarize participants with the mechanics.*

---

## ⚔️ Simon Effect (Response Conflict)

To introduce spatial response conflict, the Simon paradigm is integrated into every trial:

- **Spatial Positions:** Stimuli appear pseudo-randomly on the **Left** or **Right** side of the screen.
- **Response Keys:** 
  - `Z` key ➔ Left response
  - `M` key ➔ Right response
- **Congruency:** Each block contains an exact **50/50 split** of:
  - **Congruent trials:** Stimulus location matches the correct response side.
  - **Incongruent trials:** Stimulus location conflicts with the correct response side.

---

## 💾 Data Logging

At the end of each trial, the following variables are saved to the output dataset:

| Variable | Description |
| :--- | :--- |
| `block_num` | Current block number (1 to 14) |
| `trial_num` | Current trial number within the block |
| `stimulus_id` | Unique identifier for the presented stimulus |
| `stim_position` | Spatial location of the stimulus (`left` / `right`) |
| `correct_resp` | The correct key for the current stimulus |
| `given_resp` | The key pressed by the participant |
| `congruency` | Trial type (`congruent` / `incongruent`) |
| `set_size` | Working memory load condition (`3` / `6`) |
| `accuracy` | Response correctness (`1` = correct, `0` = incorrect) |
| `RT` | Reaction time in milliseconds |

---

## 🛠️ Requirements & Setup

*This task was built using [PsychoPy].*

### How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/[YourUsername]/[YourRepoName].git
