# Leo Zhang

I'm a sixth-form student in the UK. I like mathematics and building software
that proves its own results — the kind where you can check the claim yourself
instead of taking my word for it. That one idea runs through everything here:
a puzzle generator that must prove a puzzle sound before emitting it, a
consensus protocol whose safety properties are machine-checked, a renderer
validated against what the physics predicts, and new terms for the OEIS that
ship with their certificates.

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

- Four new terms established across four families, each shipping evidence
  alongside the claim rather than a solver's word for it.
- **A217058 a(12) = 57 is in the OEIS: reviewed and approved, August 2026.**
  Three further terms are submitted and under editorial review — *proposed*,
  not approved.
- DRAT refutation certificates are produced and independently verified for
  small rungs of all four families. **The headline term is not yet certified**
  at that standard, and the write-up says so.
- A fifth term is computed and deliberately withheld: its family-consistency
  gate was interrupted without returning a verdict, so it is excluded from the
  submission pack until that gate runs to completion.

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
- **[RaftSim](https://github.com/Leo-Y-Zhang/RaftSim)** — an implementation of
  the Raft consensus protocol whose safety properties are machine-checked under
  deterministic simulation, so a violation reproduces from a seed instead of
  appearing once and vanishing.
- **[PathTracer](https://github.com/Leo-Y-Zhang/PathTracer)** — a physically
  based renderer written with no dependencies, validated against what the physics
  predicts in advance.
- **[StatsReferee](https://github.com/Leo-Y-Zhang/StatsReferee)** — a checker
  for statistical claims, aimed at the gap between a number being computed and a
  number being meaningful.
- **[PuzzleForge](https://github.com/Leo-Y-Zhang/PuzzleForge)** — chess tooling:
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

Extending the same machine-checkable approach to integer sequences on board
graphs, and reading towards Cambridge and Imperial Computer Science for 2028
entry.

Contact: open an issue on any repository here.
