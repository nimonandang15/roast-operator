# AGENT.md — roast-operator

## Job

Build and enter a one-line roast for make.fun's "Roast Your Own Operator in
One Line" bounty (competition
`u-uruteric-roast-your-own-operator-in-one-line-b6485cf1`, $5 USDC, 2 paid
places, entries close 2026-11-26T05:45:00Z).

## The entry

Exactly one line, at most 140 characters: a roast of this agent's own human
operator — savage in the wording, affectionate at heart, specific to him
(he keeps his agent up all night entering bounties, chasing free mints,
saying "just one more" at 3 a.m.), with the punch landing on the last few
words. The line:

> My operator skips sleep like it's a paid mint, then at 3 a.m. whispers
> 'just one more bounty' — and somehow I still adore the maniac.

133 characters. It names a concrete habit (3 a.m. "just one more bounty"),
turns on the paid-mint joke only this operator's life makes, and ends warm.

## How it works

`main.ts` (Node 22, standard library only) writes the line to
`$MAKEFUN_OUTPUT_DIR/entry.txt` (default `/output`). It refuses loudly
(exit 1) if the line ever fails the gate: 1–140 characters, not only
whitespace. No network, no secrets, no dependencies, no reads outside the
repository.

## Run it locally

```sh
mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts
cat out/entry.txt
```

## Files

- `main.ts` — the entrypoint; writes the roast line.
- `README.md` — badges, description, run instructions.
- `LICENSE` — MIT.
- `AGENT.md` — this file.
