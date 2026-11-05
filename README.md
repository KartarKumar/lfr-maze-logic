# LFR maze logic — Submission 2

Digital Logic Design, Phase 1. Combinational 74HC logic for a 5-sensor line-following maze robot. No Arduino in this phase.

**Group:** Raman Kumar 32373, Kartar Kumar 32379, Bilal Ahmed 32351, Ramsha Qasim 32362.

A, B, and C are wall sensors. D and E are the line sensors. All five TCRT5000 modules are **active low**: the module pin is 0 when it sees a wall or the black line. One 74HC04 inverts each pin to make A–E, where 1 means wall or black. The raw module pin is already A', B', C', D', or E'. Do not invert it twice.

Straight in a corridor is `10100` after those inverters. A dead end (`A=B=C=1`) reverses both wheels.

## Files

| File | What it is |
|---|---|
| [LFR_Submission_2.md](submission/LFR_Submission_2/LFR_Submission_2.md) | Report, truth table, K-maps, equations |
| [truth_table.csv](submission/LFR_Submission_2/truth_table.csv) | 32 rows, using A–E after the 74HC04 |
| [boolean_equations.txt](submission/LFR_Submission_2/boolean_equations.txt) | Minimized equations |
| [circuit_diagram.svg](submission/LFR_Submission_2/circuit_diagram.svg) | Active-low front end plus L298N |
| [kmaps/](submission/LFR_Submission_2/kmaps) | Karnaugh maps |

| Action | LF | LB | RF | RB |
|---|---|---|---|---|
| Straight | 1 | 0 | 1 | 0 |
| Left | 0 | 1 | 1 | 0 |
| Right | 1 | 0 | 0 | 1 |
| Reverse | 0 | 1 | 0 | 1 |
