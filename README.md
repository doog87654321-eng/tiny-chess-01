# tiny-chess-01

A chess engine in 4 KB of Python: 0x88 board, alpha-beta search with
quiescence, transposition table, killer moves, null-move pruning, late
move reductions, futility and delta pruning, and an incremental
material + piece-square evaluation. Fixed node budget per move
(90,000 nodes), so play is fully deterministic: no clock, no unseeded
randomness.

`main.py` is the packed entrypoint (LZMA stub over the readable
`engine.py` source, packed with `makefun compress`). The engine speaks
the trial env protocol over `MAKEFUN_ENV_URL`.
