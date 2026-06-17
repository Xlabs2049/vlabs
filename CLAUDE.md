# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

This is a **document repository**, not a software project. It contains a curated
collection of long-form research PDFs on crypto / DeFi topics. There is no source
code, build system, package manifest, test suite, or CI configuration — so there
are no build, lint, or test commands to run. The only meaningful operations here
are managing (adding, removing, renaming) the PDF files and the git history that
tracks them.

## Contents

The PDFs are deep technical/financial analyses, most written in Chinese (a few
titles in English). Current topics include:

- **AMM / Uniswap** — automated market makers and Uniswap V1→V4 architecture evolution
- **Dynamic Bonding Curve** — bonding-curve mechanics
- **Hyperliquid** — on-chain orderbook to institutional risk engine, plus a postmortem of the 2025 JELLY attack
- **X402** — a proposed web standard for machine payments and protocol-layer settlement
- **Polymarket / binary options** — decentralized financial derivatives
- **Macro → on-chain** — broad systemic studies of crypto knowledge maps, liquidity, and market cycles

## Conventions

- **Filenames are the primary metadata.** Each PDF's (often long, descriptive)
  title in its filename is how content is identified — there is no index file,
  database, or manifest. Preserve descriptive titles when renaming; the Chinese
  punctuation (e.g. `《》`) and emoji prefixes (e.g. `📘`) in some names are
  intentional and part of the title.
- **Non-ASCII filenames are normal.** Git displays these as escaped octal byte
  sequences (e.g. `\345\270\201`). Use `git ls-files`/`git status` carefully and
  quote paths when scripting against them.
- **History is upload-driven.** Commits are predominantly GitHub "Add files via
  upload" actions rather than authored code changes. A `README.md` and a
  `public.zip` existed earlier and were deliberately deleted.

## Working in this repo

- This repo has no programmatic interface, so requests will generally be about
  the *content* of the PDFs (summarizing, comparing, extracting) or about
  *managing the files* (adding, organizing, renaming). To read a PDF's content,
  use the Read tool with the `pages` parameter.
- When adding documents, follow the existing pattern: a single descriptive-title
  PDF at the repository root (the repo is currently flat — no subdirectories).
