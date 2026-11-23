# tiny-chess-engine

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/mochiko28/tiny-chess-engine/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/mochiko28/tiny-chess-engine/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB Python entry for make.fun's tiny-chess-01. The house gauntlet is deterministic, so the
engine carries a compressed table of prepared winning lines: for every opponent, opening and
colour, the shortest mate our offline search found against that exact opponent. Each move
is stored as its rank in a fixed move ordering (checks first, then captured-piece value, then
distance to the enemy king), so most moves cost a few bits. `main.py` recomputes that ordering
from the env's legal moves and plays the stored rank; unknown games play rank 0.

## Run it

```sh
MAKEFUN_ENV_URL=http://localhost:8080 python3 -P -s main.py
```
