<div align="center">
  <img alt="Hello, World!  |  A217236(4) = 84  |  s VERIFIED"
       src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=22&pause=900&center=true&vCenter=true&multiline=true&repeat=false&width=520&height=118&color=58A6FF&lines=Hello%2C%20World!;A217236(4)%20%3D%2084;s%20VERIFIED" />
</div>

# Leo Zhang

I'm a sixth-form student in the UK. I like mathematics and building software
that proves its own results — the kind where you can check the claim yourself
instead of taking my word for it. That one idea runs through everything here:
a puzzle generator that must prove a puzzle sound before emitting it, a
consensus protocol whose safety properties are machine-checked, a renderer
validated against what the physics predicts, and new terms for the OEIS that
ship with their certificates.

<p align="center">
  <b>Proof and verification</b>
  <br />
  <img alt="Lean 4" src="https://img.shields.io/badge/-Lean%204-2E2E2E?style=flat-square" />
  <img alt="kissat / CaDiCaL" src="https://img.shields.io/badge/-kissat%20%2F%20CaDiCaL-4B32C3?style=flat-square" />
  <img alt="DRAT / LRAT" src="https://img.shields.io/badge/-DRAT%20%2F%20LRAT-6E40C9?style=flat-square" />
  <img alt="Vitest" src="https://img.shields.io/badge/-Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=ffffff" />
  <img alt="Playwright" src="https://img.shields.io/badge/-Playwright-2EAD33?style=flat-square" />
</p>

<p align="center">
  <b>Languages</b>
  <br />
  <img alt="Python" src="https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=ffffff" />
  <img alt="TypeScript" src="https://img.shields.io/badge/-TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=ffffff" />
  <img alt="Rust" src="https://img.shields.io/badge/-Rust-000000?style=flat-square&logo=rust&logoColor=ffffff" />
  <img alt="C++" src="https://img.shields.io/badge/-C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=ffffff" />
  <img alt="LaTeX" src="https://img.shields.io/badge/-LaTeX-008080?style=flat-square&logo=latex&logoColor=ffffff" />
</p>

<p align="center">
  <b>Tools and platforms</b>
  <br />
  <img alt="Vite" src="https://img.shields.io/badge/-Vite-646CFF?style=flat-square&logo=vite&logoColor=ffffff" />
  <img alt="Docker" src="https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=ffffff" />
  <img alt="GNU Bash" src="https://img.shields.io/badge/-GNU%20Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=ffffff" />
  <img alt="GitHub Actions" src="https://img.shields.io/badge/-GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=ffffff" />
  <img alt="Raspberry Pi" src="https://img.shields.io/badge/-Raspberry%20Pi-C51A4A?style=flat-square&logo=raspberrypi&logoColor=ffffff" />
  <img alt="RISC-V" src="https://img.shields.io/badge/-RISC--V-283272?style=flat-square&logo=riscv&logoColor=ffffff" />
</p>

## Mixed van der Waerden numbers

I have been computing new terms in families of mixed van der Waerden numbers
whose OEIS entries were last extended by Tanbir Ahmed in 2012 and were still
unchanged when I checked them against the OEIS API on 29 July 2026.

For colour targets `t_1..t_r` and a budget of `j` wildcards,

```
w(j+r; 2^j, t_1..t_r) = 1 + max{ n : [1,n] splits into j singleton classes and
                                 r colour classes, where colour class i contains
                                 no t_i-term arithmetic progression }
```

Each new term needs two independent halves. The lower bound is a colouring, and
a colouring is a certificate — you read the string and apply the definition, no
solver involved. The upper bound asserts that *no* colouring exists, which is
only as trustworthy as the encoding behind it, so that half is where the work is.

**Status, stated exactly.**

- Five new terms established across five families, each shipping evidence
  alongside the claim rather than a solver's word for it.
- **All five are in the OEIS, approved between 6 and 13 August 2026:**
  A217058 a(12) = 57, A217005 a(19) = 52, A217007 a(7) = 68,
  A217236 a(4) = 84 and A217059 a(9) = 74.
- The headline refutation is reduced to formally checked proof objects — 4,487
  per-cube DRAT proofs, each replayed to `s VERIFIED` by `drat-trim`, plus a
  checked proof that the cube set is exhaustive. **The other four upper bounds
  rest on cross-checked solver verdicts rather than on checked proofs**, and
  the write-up says exactly that.

Method, encoding, symmetry breaking and the limits of what has actually been
proved are written up in [MathRecords](https://github.com/Leo-Y-Zhang/MathRecords).
The standalone certificate verifier depends on nothing but the Python standard
library.

## What I build

Roughly one idea, applied repeatedly: a result is worth what its verification is
worth. Each of these is public, and each is built so that what it claims can be
checked rather than believed.

- **[QuantumCompiler](https://github.com/Leo-Y-Zhang/QuantumCompiler)** — a
  compiler for quantum circuits, its transformations stated as properties that
  are tested rather than asserted.
- **[DeterministicRaft](https://github.com/Leo-Y-Zhang/DeterministicRaft)** — an implementation of
  the Raft consensus protocol whose safety properties are machine-checked under
  deterministic simulation, so a violation reproduces from a seed instead of
  appearing once and vanishing.
- **[PathTracer](https://github.com/Leo-Y-Zhang/PathTracer)** — a physically
  based renderer written with no dependencies, validated against what the physics
  predicts in advance.
- **[QuantumClaimReferee](https://github.com/Leo-Y-Zhang/QuantumClaimReferee)** — a checker
  for statistical claims, aimed at the gap between a number being computed and a
  number being meaningful.
- **[ChessPuzzleForge](https://github.com/Leo-Y-Zhang/ChessPuzzleForge)** — chess tooling:
  an engine, an analyser, and a puzzle generator that must prove a puzzle sound
  before it will emit it.
- **[TerminalAgent](https://github.com/Leo-Y-Zhang/TerminalAgent)** — a
  terminal-based agent, built around the question of what such a thing should
  refuse to do.
- **[EndeavourRacing](https://github.com/Leo-Y-Zhang/EndeavourRacing)** — the
  web applications for a student motorsport team: the marketing site, a lap-time
  prediction tool, and a project, risk and budget dashboard.
- **[TradingEngineResearch](https://github.com/Leo-Y-Zhang/TradingEngineResearch)** —
  the research core of a systematic trading platform: a fail-closed engine, a
  default-deny validation gate, and a pre-registered alpha search whose honest
  result was negative.
- **[MeltSim](https://github.com/Leo-Y-Zhang/MeltSim)** — an interactive
  thermodynamics sandbox: enthalpy-method melting, solidification and boiling in
  the browser, with zero runtime dependencies.
- **[IaCScanner](https://github.com/Leo-Y-Zhang/IaCScanner)** — an offline
  infrastructure-as-code misconfiguration scanner: Terraform, Kubernetes,
  Actions and Dockerfile rule packs, SARIF output, and a fail-only-on-new CI
  baseline.
- **[DocRedact](https://github.com/Leo-Y-Zhang/DocRedact)** — a local-first,
  policy-driven document redaction CLI that never sends a document anywhere.
- **[VisionCheckR](https://github.com/Leo-Y-Zhang/VisionCheckR)** — a
  privacy-first educational vision self-check that runs entirely in the browser,
  with a pure, unit-tested scoring core. Not a medical device.
- **[Understudy](https://github.com/Leo-Y-Zhang/Understudy)** — an
  interview rehearsal studio that runs entirely in the browser: on-device
  face and speech analysis with an annotated replay of your answer. The
  privacy claim is enforced rather than promised — a CI test records a real
  session and fails the build if any request leaves the origin. Live at
  [leo-y-zhang.github.io/Understudy](https://leo-y-zhang.github.io/Understudy/).
- **[ClimateMesh](https://github.com/Leo-Y-Zhang/ClimateMesh)** — a Raspberry
  Pi environmental sensing mesh with explainable early-warning risk scoring,
  built by two sixth-form students for the PA Raspberry Pi Competition 2026.
- **[FireTurret](https://github.com/Leo-Y-Zhang/FireTurret)** — a camera-guided
  fire-suppression turret demonstrator: simulation, vision and safety interlocks
  behind one supervised control loop, with the safety case written down.
- **[FilingsLab](https://github.com/Leo-Y-Zhang/FilingsLab)** — an SEC-filings
  event-study backtester: disclosure ingestion, deflation-robust validation, and
  a research loop that must prove an edge before believing it.

Some work stays private: a live web application with real users, and the
live-trading side of the platform whose research core is published above.
Neither is private for want of finishing.

Mostly Python and TypeScript, with SAT solvers, DRAT/LRAT proof checking, and
whatever numerical method the problem happens to need.

## Currently

The same machine-checkable approach applied to other integer sequences.
[GraphRecords](https://github.com/Leo-Y-Zhang/GraphRecords) turns bishop
arrangements into rook arrangements and has put fourteen new terms into seven
OEIS sequences on board graphs.
[RadoRecords](https://github.com/Leo-Y-Zhang/RadoRecords) carries the 2-colour
Rado numbers for `x_1^2 + ... + x_n^2 = z^2` from a(30) to a(60) with
DRAT-certified refutations — a(31) approved, the rest a proposed draft awaiting
an editor as I write this.
[Refute](https://github.com/Leo-Y-Zhang/Refute) is the second opinion on those
certificates: an independent DRAT/LRAT checker in Rust, with a browser
playground where the files never leave the tab.

Contact: open an issue on any repository here.
