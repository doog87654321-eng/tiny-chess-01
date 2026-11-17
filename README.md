# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/doog87654321-eng/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/doog87654321-eng/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4 KB of Python: 0x88 board, alpha-beta search with
quiescence, transposition table, killer moves, null-move pruning, late
move reductions, futility and delta pruning, and an incremental
material + piece-square evaluation. Fixed node budget per move
(90,000 nodes), so play is fully deterministic: no clock, no unseeded
randomness.

`main.py` is the packed entrypoint (LZMA stub over the readable
`engine.py` source, packed with `makefun compress`). The engine speaks
the trial env protocol over `MAKEFUN_ENV_URL`.

## Run it

```sh
node cli/makefun.mjs grade-local --kit . --bot https://github.com/doog87654321-eng/tiny-chess-01 --driver docker
```
