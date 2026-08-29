# Viper 2800

A human-like ~2800 FIDE chess engine that plays **sharp, attacking, sacrificial** chess — Boa 2800's tactical sibling. Same architecture, opposite instincts: the strike, not the squeeze.

## Architecture

Same three engines as Boa:

- **Policy net** — trained on the attacking players (the Tal / Polgar / Shirov lineage) instead of the grinders.
- **All-seeing eye** — the same veto interface. Also not settled, and Viper may end up with a different engine here than Boa: sacrifices need an eval that respects initiative.
- **Opponent model** — Maia-3. Boa uses it to squeeze; Viper leans on it harder — more of the move choice goes to "what will this human get wrong."

## Status

Waiting on Boa to ship. The data pipeline, training, and calibration get proven there first; Viper is then a new player roster and a re-tune. Code and release binaries once it's calibrated.

Positional sibling: [Boa 2800](https://github.com/LinkLikesLattes/Boa2800).
