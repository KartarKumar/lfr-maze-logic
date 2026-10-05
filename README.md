# Line-following maze robot — Submission 2

Digital Logic Design phase 1. Five sensors, 74HC gates, L298N. No Arduino.

**A, B, C = walls. D, E = line.** Dead end `A=B=C=1` → reverse both wheels.

Group: Raman Kumar 32373, Kartar Kumar 32379, Bilal Ahmed 32351, Ramsha Qasim 32362.

## Download for the instructor

The file to submit is `LFR_Submission_2.zip` in this repo (`submission/LFR_Submission_2/` unzipped).

## Equations

```
LEFT     = A'BC + A'BD + A'B E' + D B' E'
RIGHT    = A B C' + B' D' E + C' D' E
STRAIGHT = B'(DE + D'E')
REVERSE  = A B C

LF = STRAIGHT + RIGHT
LB = LEFT + REVERSE
RF = STRAIGHT + LEFT
RB = RIGHT + REVERSE
```

Clone:

```bash
git clone https://github.com/KartarKumar/lfr-maze-logic.git
```
