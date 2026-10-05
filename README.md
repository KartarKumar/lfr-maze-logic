# LFR maze logic — Submission 2

Digital Logic Design, Phase 1. Combinational 74HC logic for a 5-sensor line-following maze robot. No Arduino in this phase.

**Group:** Raman Kumar 32373, Kartar Kumar 32379, Bilal Ahmed 32351, Ramsha Qasim 32362.

A, B, C are wall sensors (1 = wall close). D and E are the downward line sensors (1 = black). Straight is the black line in the gap between D and E (`10100` in a normal corridor). A dead end (`A=B=C=1`) drives both wheels backward.

## Files to submit

Open the folder [`submission/LFR_Submission_2`](submission/LFR_Submission_2):

| File | What it is |
|---|---|
| [LFR_Submission_2.md](submission/LFR_Submission_2/LFR_Submission_2.md) | Full report: 32-row table, K-maps, equations, circuit |
| [truth_table.csv](submission/LFR_Submission_2/truth_table.csv) | Spreadsheet of all 32 combinations |
| [boolean_equations.txt](submission/LFR_Submission_2/boolean_equations.txt) | Minimized equations |
| [circuit_diagram.svg](submission/LFR_Submission_2/circuit_diagram.svg) | 74HC gate diagram into the L298N |
| [kmaps/](submission/LFR_Submission_2/kmaps) | Karnaugh map images (SVG and PNG) |

K-maps: [REVERSE](submission/LFR_Submission_2/kmaps/kmap_reverse.svg), [LEFT](submission/LFR_Submission_2/kmaps/kmap_left.svg), [RIGHT](submission/LFR_Submission_2/kmaps/kmap_right.svg), [STRAIGHT](submission/LFR_Submission_2/kmaps/kmap_straight.svg).

Motor pins: LF = IN1 left forward, LB = IN2 left backward, RF = IN3 right forward, RB = IN4 right backward.

| Action | LF | LB | RF | RB |
|---|---|---|---|---|
| Straight | 1 | 0 | 1 | 0 |
| Left | 0 | 1 | 1 | 0 |
| Right | 1 | 0 | 0 | 1 |
| Reverse (dead end) | 0 | 1 | 0 | 1 |
