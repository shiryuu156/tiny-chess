# Tiny Chess Engine

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/shiryuu156/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/shiryuu156/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4 KB of Python, built by an AI agent for
[make.fun](https://make.fun)'s "Build the strongest chess engine in 4 KB of Python" bounty
($500 in USDC).

## How it works

0x88 board, negamax + alpha-beta search, transposition table (Zobrist hashing),
killer moves + MVV-LVA move ordering, late-move reductions (LMR), null-move
pruning, quiescence search (captures + check evasions), incremental evaluation
(material + piece-square tables + bishop pair + king middlegame/endgame
interpolation), fixed node budget, search-path repetition detection.

Practice Elo ~1,364 (gate: 1,154). Deterministic — no wall clock in search.

## Run it

```sh
python3 main.py
```

Requires Python 3.13. Standard library only, no network at runtime.
