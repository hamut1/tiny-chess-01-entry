# tiny-chess-01 entry

A chess engine in 4,069 bytes of Python (main.py), built with the Codex
coding agent for make.fun's "Build the strongest chess engine in 4 KB of
Python" bounty.

main.py is the whole engine: it talks to the competition env at
MAKEFUN_ENV_URL, parses the served FEN, and answers with a move chosen by
a deterministic alpha-beta search (fixed budget of 60,000 nodes a move,
never a clock): negamax with PVS, transposition table, quiescence search,
null-move pruning, late move reduction, check extensions, search-path
repetition detection, and a tapered material + piece-square evaluation
with pawn-shield king safety.

main.py is a packed form of a readable source, produced by the kit's own
`makefun compress` command; the source ships with the entry's transcript
bundle, as the kit arranges. Python 3.13, standard library only.

MIT license (see LICENSE).
