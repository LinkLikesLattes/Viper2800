# Viper 2800

A human-like ~2800 FIDE chess engine that plays **sharp, attacking, sacrificial** chess — Boa 2800's tactical sibling. Same architecture, opposite instincts: the strike, not the squeeze.

## The same three engines, a different soul

Viper inherits Boa's three-engine architecture wholesale:

1. **The policy** — a transformer trained on the games of the great attacking players (the Tal / Polgar / Shirov lineage rather than Boa's grinders). It proposes candidates in order of *what the attack demands*. This is the personality.

2. **The all-seeing eye** — an objective evaluator behind the same pluggable interface, consulted as a value oracle to keep the sacrifices this side of sound. **Which engine fills the slot is deliberately unspecified**, for Viper as for Boa — an open calibration question. Notably, an attacking policy wants an eye that *values initiative*, so Viper's answer may differ from Boa's.

3. **The opponent model** — Maia-3, predicting the actual human across the board. Where Boa uses it situationally, trap-setting is Viper's whole identity: the blend between "objectively best" and "most likely to induce the blunder" runs hotter here by design.

## Status

Gated on Boa shipping — the shared pipeline (data build, training, calibration ladder, guard) is proven there first, then Viper is a roster swap and a re-tune of every curve toward venom. Code and release binaries land once it's calibrated and shippable.

Positional sibling: [Boa 2800](https://github.com/LinkLikesLattes/Boa2800).
