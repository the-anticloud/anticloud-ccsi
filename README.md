# CCSI

![license](https://img.shields.io/badge/license-MIT-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-carbon_capture-lightgrey)

> Anticloud-hardened packaging of the upstream project `CCSI` in category **CARBON CAPTURE**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** CARBON CAPTURE · **Upstream:** https://github.com/the-anticloud/anticloud-ccsi.git · **Upstream pin:** `904da5dfc6db75c836acfaa46c0f9cfb1838081c` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

<p align="center">
  <img src="assets/wordmark.svg" alt="ccsidekick" width="620">
</p>

<p align="center"><b>A Claude Code status line with a character that reacts to your session.</b> Full cost, git, and usage at a glance, at zero token spend.</p>

<p align="center">
  <img src="https://img.shields.io/badge/Claude%20API-none-2ea44f" alt="No Claude API">
  <img src="https://img.shields.io/badge/token%20spend-zero-2ea44f" alt="Zero token spend">
  <img src="https://img.shields.io/badge/data-local--first-2ea44f" alt="Local-first">
  <a href="https://github.com/krayong/ccsidekick/actions/workflows/ci.yml"><img src="https://github.com/krayong/ccsidekick/actions/workflows/ci.yml/badge.svg" alt="CI"></a>
  <a href="https://www.npmjs.com/package/ccsidekick"><img src="https://img.shields.io/npm/v/ccsidekick.svg" alt="npm version"></a>
  <!-- npm downloads badge hidden until launch (shows 0/month pre-adoption); restore once traffic ramps:
  <a href="https://www.npmjs.com/package/ccsidekick"><img src="https://img.shields.io/npm/dm/ccsidekick.svg" alt="npm downloads"></a>
  -->
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License: MIT"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/themes-75%2B-8a63d2" alt="75+ themes">
  <img src="https://img.shields.io/badge/widgets-33-8a63d2" alt="33 widgets">
  <img src="https://img.shields.io/badge/characters-18%20packs-8a63d2" alt="18 character packs">
  <img src="https://img.shields.io/badge/built%20with-Bun-f9f1e1?logo=bun&logoColor=000" alt="Built with Bun">
  <img src="https://img.shields.io/badge/TypeScript-3178c6?logo=typescript&logoColor=fff" alt="TypeScript">
</p>

<p align="center">
  <img src="assets/characters.gif" alt="Animated reel cycling through ccsidekick's character packs (Batman, Spider-Man, Yoda, and more), each an ASCII figure in its own theme beside a live Claude Code status line of git, cost, context, and usage with an in-character comment" width="900">
</p>

## What you get

- **A character that reacts.** It notices what Claude is doing (tests passing, builds breaking,
  commits landing, a struggle and then a recovery) and comments in character, warming to you across
  sessions through familiarity tiers.
- **A real status line.** 33 toggleable widgets: directory, model, git (branch, ahead/behind,
  staged/unstaged/untracked, uncommitted changes, stash, worktree, conflicts), token context, cost,
  usage limits, PR state, burn rate, and more. Threshold-colored.
- **75+ built-in themes.** Dark, high-contrast, and retro palettes (Dracula, Nord,
  Catppuccin, Tokyo Night, Gruvbox, Rosé Pine, Synthwave '84, and dozens more), including one tuned
  to each character pack.
- **Cost at a glance.** Chat, per-project, and all-time spend, read straight from your Claude Code
  transcripts. No token spend and nothing extra to install.
- **Character spinner verbs.** The active character rewrites Claude Code's spinner verbs, so even
  the loading text stays in persona.

## Install

```bash
npx ccsidekick
```

Running `ccsidekick` in a terminal opens the setup UI. On a first run it walks you through a short
guided **wizard** (character → theme → comments); later runs open the full **dashboard** to change
config or view stats, and either view can switch to the other with Ctrl+W / Ctrl+D. It wires
everything into Claude Code's `settings.json` (backing the file up first). Run
`npx ccsidekick --help` for every command, including a clean uninstall.

Prefer no TTY? `npx ccsidekick setup --character spiderman --theme houston --mode fixed` configures
and wires everything from flags. See [Non-interactive setup](#non-interactive-setup).

### From inside Claude Code

The project is its own plugin marketplace, so you can wire everything up without leaving Claude Code:

```
/plugin marketplace add krayong/ccsidekick
/plugin install ccsidekick@ccsidekick
```

That adds a `/ccsidekick-setup` slash command. Describe what you want in plain words
(`/ccsidekick-setup batman with the dracula theme and no cost widgets`) and Claude picks the flags
and runs the setup for you. The plugin carries the command and nothing else; the engine still comes
from npm the first time you run it.

New characters and widgets land regularly.
[Watch this project for releases](https://github.com/krayong/ccsidekick/subscription) to hear about
them.

## Characters

Every character ships bundled with the engine, so a fresh install has them all — no download or
install step. Pick and switch between them in the **Character** section (or the wizard): fixed mode
pins one, random mode rotates a roster.

Each pack is data, never code: a single sourced ASCII figure (credited to its original artist; mood
adds color-only effects, never a new frame), a curated message library, and at least twenty-five
in-voice spinner verbs. Out of the box ccsidekick runs in random mode over the full roster, picking
a character per session; `spiderman` is the default only when you pin one in fixed mode.

**Available packs:**

- **Barbie**: a bright, upbeat pack in signature pink, with a matching theme.
- **Batman**: an edgy, cowled sidekick in a dark cowl-and-night palette, with a matching theme.
- **Ben 10**: a mild, cocky kid-hero pack in Omnitrix lime.
- **Darth Vader**: an edgy, imperious Sith pack in ember red and cold steel.
- **Deadpool**: an offensive-tone merc pack in Deadpool red, with a matching theme.
- **Gandalf**: a mild, wise wizard pack in White Rider silver and gold.
- **Harry Potter**: a wizarding pack in Gryffindor scarlet and gold.
- **Hello Kitty**: a sweet, wholesome pack with a soft blush-pink theme.
- **Iron Man**: an edgy, quippy genius pack in hot-rod red, gold, and arc-reactor cyan.
- **James Bond**: an edgy secret-agent pack in cool gunmetal blue, with a matching theme.
- **Joker**: an edgy, chaos-loving pack in Joker purple and acid green.
- **Naruto**: a mild, hot-blooded ninja pack in ramen orange and Rasengan blue.
- **Pikachu**: a mil

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Node.js / npm** (manifests: package.json; scanned in UPSTREAM_CLONE)
- Top-level source layout: `assets/`, `commands/`, `packages/`, `scripts/`, `website/`
- Snapshot size: **508 files**, **39120 lines of code** (measured; see Benchmarks)
- Primary languages: `.ts` (279), `.tsx` (75), `.json` (49), `.md` (46), `.svg` (21), `(none)` (8)
- Upstream commit pinned for this packaging: `904da5dfc6db75c836acfaa46c0f9cfb1838081c`

---

## Installation

commits landing, a struggle and then a recovery) and comments in character, warming to you across
  sessions through familiarity tiers.
- **A real status line.** 33 toggleable widgets: directory, model, git (branch, ahead/behind,
  staged/unstaged/untracked, uncommitted changes, stash, worktree, conflicts), token context, cost,
  usage limits, PR state, burn rate, and more. Threshold-colored.
- **75+ built-in themes.** Dark, high-contrast, and retro palettes (Dracula, Nord,
  Catppuccin, Tokyo Night, Gruvbox, Rosé Pine, Synthwave '84, and dozens more), including one tuned
  to each character pack.
- **Cost at a glance.** Chat, per-project, and all-time spend, read straight from your Claude Code
  transcripts. No token spend and nothing extra to install.
- **Character spinner verbs.** The active character rewrites Claude Code's spinner verbs, so even
  the loading text stays in persona.

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

<p align="center">
  <img src="https://img.shields.io/badge/Claude%20API-none-2ea44f" alt="No Claude API">
  <img src="https://img.shields.io/badge/token%20spend-zero-2ea44f" alt="Zero token spend">
  <img src="https://img.shields.io/badge/data-local--first-2ea44f" alt="Local-first">
  <a href="https://github.com/krayong/ccsidekick/actions/workflows/ci.yml"><img src="https://github.com/krayong/ccsidekick/actions/workflows/ci.yml/badge.svg" alt="CI"></a>
  <a href="https://www.npmjs.com/package/ccsidekick"><img src="https://img.shields.io/npm/v/ccsidekick.svg" alt="npm version"></a>
  <!-- npm downloads badge hidden until launch (shows 0/month pre-adoption); restore once traffic ramps:
  <a href="https://www.npmjs.com/package/ccsidekick"><img src="https://img.shields.io/npm/dm/ccsidekick.svg" alt="npm downloads"></a>
  -->
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License: MIT"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/themes-75%2B-8a63d2" alt="75+ themes">
  <img src="https://img.shields.io/badge/widgets-33-8a63d2" alt="33 widgets">
  <img src="https://img.shields.io/badge/characters-18%20packs-8a63d2" alt="18 character packs">
  <img src="https://img.shields.io/badge/built%20with-Bun-f9f1e1?logo=bun&logoColor=000" alt="Built with Bun">
  <img src="https://img.shields.io/badge/TypeScript-3178c6?logo=typescript&logoColor=fff" alt="TypeScript">
</p>

<p align="center">
  <img src="assets/characters.gif" alt="Animated reel cycling through ccsidekick's character packs (Batman, Spider-Man, Yoda, and more), each an ASCII figure in its own theme beside a live Claude Code status line of git, cost, context, and usage with an in-character comment" width="900">
</p>

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

<img src="https://img.shields.io/badge/token%20spend-zero-2ea44f" alt="Zero token spend">
  <img src="https://img.shields.io/badge/data-local--first-2ea44f" alt="Local-first">
  <a href="https://github.com/krayong/ccsidekick/actions/workflows/ci.yml"><img src="https://github.com/krayong/ccsidekick/actions/workflows/ci.yml/badge.svg" alt="CI"></a>
  <a href="https://www.npmjs.com/package/ccsidekick"><img src="https://img.shields.io/npm/v/ccsidekick.svg" alt="npm version"></a>
  <!-- npm downloads badge hidden until launch (shows 0/month pre-adoption); restore once traffic ramps:
  <a href="https://www.npmjs.com/package/ccsidekick"><img src="https://img.shields.io/npm/dm/ccsidekick.svg" alt="npm downloads"></a>
  -->
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License: MIT"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/themes-75%2B-8a63d2" alt="75+ themes">
  <img src="https://img.shields.io/badge/widgets-33-8a63d2" alt="33 widgets">
  <img src="https://img.shields.io/badge/characters-18%20packs-8a63d2" alt="18 character packs">
  <img src="https://img.shields.io/badge/built%20with-Bun-f9f1e1?logo=bun&logoColor=000" alt="Built with Bun">
  <img src="https://img.shields.io/badge/TypeScript-3178c6?logo=typescript&logoColor=fff" alt="TypeScript">
</p>

<p align="center">
  <img src="assets/characters.gif" alt="Animated reel cycling through ccsidekick's character packs (Batman, Spider-Man, Yoda, and more), each an ASCII figure in its own theme beside a live Claude Code status line of git, cost, context, and usage with an in-character comment" width="900">
</p>

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Node.js / npm |
| Manifests detected | package.json |
| Files in snapshot | 508 |
| Lines of code | 39120 |
| Dependency references | 43 |
| Dependencies by ecosystem | npm: 43 |
| Upstream license | MIT |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| npm | @changesets/cli | ^2.31.0 | package.json |
| npm | @eslint-community/eslint-plugin-eslint-comments | ^4.7.2 | package.json |
| npm | @happy-dom/global-registrator | ^20.10.6 | package.json |
| npm | @types/bun | ^1.3.0 | package.json |
| npm | @types/node | ^20.19.0 | package.json |
| npm | @typescript-eslint/eslint-plugin | ^8.62.0 | package.json |
| npm | @typescript-eslint/parser | ^8.62.0 | package.json |
| npm | eslint | ^9.39.0 | package.json |
| npm | eslint-import-resolver-typescript | ^4.4.5 | package.json |
| npm | eslint-plugin-boundaries | ^6.0.2 | package.json |
| npm | eslint-plugin-import-x | ^4 | package.json |
| npm | eslint-plugin-react-hooks | ^7.1.1 | package.json |
| npm | eslint-plugin-regexp | ^3.1.1 | package.json |
| npm | eslint-plugin-sonarjs | ^4.1.0 | package.json |
| npm | eslint-plugin-unicorn | ^70.0.0 | package.json |
| ... | (28 more) | | |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

everything into Claude Code's `settings.json` (backing the file up first). Run
`npx ccsidekick --help` for every command, including a clean uninstall.

Prefer no TTY? `npx ccsidekick setup --character spiderman --theme houston --mode fixed` configures
and wires everything from flags. See [Non-interactive setup](#non-interactive-setup).

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

*Excerpt from upstream `CONTRIBUTING.md`:*

# Contributing to ccsidekick

Thanks for your interest. ccsidekick is a Claude Code status line with a reactive ASCII character
and a full widget layer. Bug fixes, new widgets, and new character packs are all welcome.

By participating you agree to abide by the [Code of Conduct](CODE_OF_CONDUCT.md).

## Development setup

The project is a Bun workspace. The engine is `packages/core` (published as `ccsidekick`); each
character is `packages/packs/<name>` (published as `@ccsidekick/pack-<name>`).

```bash
bun install
bun test
```

`bun install` also points git at the project's native hooks (`core.hooksPath = .githooks`). The
`pre-commit` hook runs Prettier, ESLint, the type-checker, and the test suite; the `pre-push` hook
runs trufflehog when it is installed.

## Toolchain

| command                | what it does                                        |
| ---------------------- | --------------------------------------------------- |
| `bun test`             | the test suite; the source of truth for correctness |
| `bun run typecheck`    | `tsc --noEmit`, strict and maximal-pedantic         |
| `bun run lint`         | ESLint (`strictTypeChecked`)                        |
| `bun run format:check` | Prettier in check mode (printWidth 100, tabs)       |
| `bun run format`       | Prettier in write mode                              |
| `bun run build`        | the two-bundle Bun build into `packages/core/dist`  |
| `bun run pack:lint`    | the pack gate (see below)                           |

The TypeScript config is strict with `exactOptionalPropertyTypes`, `noUncheckedIndexedAccess`,
`noPropertyAccessFromIndexSignature`, and `verbatimModuleSyntax`, so loose access and implicit `any`
are errors, not warnings. Keep all four green; the `pre-commit` hook enforces them anyway.

## Conventions

- **TypeScript, ESM.** `"type": "module"`; never `require()` in shipped modules.
- **TDD.** Write the failing test first, watch it fail for the right reason, then the minimal
  implementation. Commit often.
- **Node-portable core.** The shipped library avoids Bun-only runtime APIs so it runs on Node;
  `bun:test` and `Bun.spawn` are test-only. Setup-time code (the TUI and the bundle build) may use
  Bun APIs.
- **Match the surrounding style.** Touch only what your change needs.
- **State facts, not plan history.** Comments and docs describe what the code does and why, never
  what some prior plan or phase said. Leave no pointers to scratch docs.

The load-bearing invariants (pack f

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: MIT** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
The MIT License (MIT)

Copyright (c) 2026 Karan Gourisaria (https://github.com/krayong/)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original MIT terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `MIT` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `CCSI` (category: CARBON CAPTURE)
- **Upstream URL:** https://github.com/the-anticloud/anticloud-ccsi.git
- **Pinned commit (SHA):** `904da5dfc6db75c836acfaa46c0f9cfb1838081c`
- **Branch:** main
- **Pin provenance:** resolved during the second documentation pass. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`572c818a47e0cd190fb0f525d84aa9ee02dc53dbc700c4052d7119f191c3e3cd`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

