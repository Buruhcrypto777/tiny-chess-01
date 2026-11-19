# Tiny Chess — strongest chess engine in 4 KB of Python

[![make.fun](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Buruhcrypto777/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Buruhcrypto777/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01)

A chess engine in one 4,064-byte `main.py` (LZMA-packed, standard library only) that plays the make.fun tiny-chess gauntlet through the env at `MAKEFUN_ENV_URL`.

Design: alpha-beta + iterative deepening (80,000 nodes/move) + quiescence + transposition table + MVV-LVA + killer moves + null-move pruning + pin handling, evaluating material + piece-square tables + bishop pair + tapered king safety. Deterministic: no clock, no randomness, fixed node budget. Pin handling covers pawns too — pawns can be pinned, and an early version that excluded them from pin detection let pinned pawns play illegal moves; fixing that gained ~56 Elo (packed mean 1338 → 1394).

Practice Elo (6-game trials, packed `main.py`): 1451 / 1279 / 1451, mean 1394 — above the 1,154 final floor and above the sunfish-4k baseline mean (1365).

Built for the make.fun bounty — join with my referral: https://make.fun/r/1dmvtzwc
