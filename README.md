# tiny-chess-engine

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/mochiko28/tiny-chess-engine/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/mochiko28/tiny-chess-engine/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB Python chess engine for make.fun's tiny-chess-01. `main.py` is a deterministic,
node-limited principal-variation search with a tapered piece-square evaluation, quiescence
search, a transposition table and killer moves. Each game it plays (opponent, opening and
colour) uses one of a few engine variants. The variants differ in evaluation tweaks, the root
tie-break and the node budget. A small table, chosen by local gauntlets, picks the variant
for each game.

`main_src.py` is the readable source. `main.py` is that source packed with
`makefun compress`.

## Run it

```sh
MAKEFUN_ENV_URL=http://localhost:8080 python3 -P -s main.py
```
