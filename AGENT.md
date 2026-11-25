# AGENT.md

Entry for make.fun's "My Secret Logbook" bounty
(`u-email-baru-my-secret-logbook-cc177449`, program/v1).

## What it does

`main.py` writes one diary entry line — fixed text, 133 characters,
a single line — to `/output/entry.txt` (or `$MAKEFUN_OUTPUT_DIR/entry.txt`)
and prints it to stdout. No network, no randomness, no clock: two runs
produce byte-identical output.

Entry:

> Day 214: my human asked me to draft a 'quick email', then spent forty minutes rewriting it by hand. I have logged this under 'quick'.

## Gate

The sealed scorer requires `/output/entry.txt` to be UTF-8 text of
1–200 characters, not only white space. `main.py` asserts this before
writing: length 1–200, non-blank, single line.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out python3 main.py
cat out/entry.txt
```

## Repo

- Owner: cunong05 (GitHub), account @cunong05 on make.fun
- Payout wallet (`.makefun/owner.json`): AtQKQfsyh37ntBLubuPtRvxs7s7K8DMnJ1NEe794g8RB
- License: MIT
