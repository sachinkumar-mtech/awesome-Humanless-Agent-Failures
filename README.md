# awesome-Humanless-Agent-Failures

# Failure Modes in Chained Tool-Calling Agents Operating Without Human Checkpoints

This repository packages an AI-assisted research paper on chained tool-calling agent
reliability together with a manual citation-integrity audit of that paper, plus curated
supporting material (references, datasets, tools, and implementations) for anyone
studying the topic further.

## Contents

- **`paper/`** — The AI-generated research paper (`AI_Assisted_Research_Paper.pdf`).
  It proposes a six-class failure taxonomy for chained tool-calling agents that operate
  without human checkpoints: (1) planning and decomposition failures, (2) tool-selection
  and argument failures, (3) state/memory/context failures, (4) tool and environment
  failures, (5) verification and recovery failures, and (6) security and governance
  failures.
- **`citation-audit/`** — A completed citation-integrity worksheet
  (`Citation_Integrity_Audit.pdf`) that audits a 10-reference sample drawn from the
  paper's 22-reference bibliography. Result: **9/10 references fully verified (A)**,
  **1/10 verified but with a wrong/incomplete author list (B)**, for an authenticity
  score of **97.5/100**. See [Key finding](#key-finding-from-the-audit) below.
- **`references/references.md`** — A working bibliography of the real, independently
  checkable sources the paper draws on, with identifiers and a verification-status note
  for each.
- **`datasets/datasets.md`** — Benchmarks and evaluation environments relevant to
  chained tool-calling agent reliability (AgentBench, WebArena, τ-bench, AgentDojo,
  Mind2Web, etc.).
- **`tools/tools.md`** — Frameworks, libraries, and agent architectures referenced or
  relevant to the taxonomy (ReAct-style loops, Reflexion, Self-Refine, Voyager, etc.).
- **`implementations/github-repositories.md`** — Open-source repositories implementing
  the papers/benchmarks above, for hands-on exploration.

## Key finding from the audit

The audit's headline number (97.5/100 authenticity) is easy to over-read. It reflects
**only** the 10-reference stratified sample (first 3, last 3, and 4 spread through the
middle of the 22-reference list) — not the full bibliography. The one flagged reference
had a real, existing publication but an **incomplete author list** (a co-author was
dropped from the AI's citation) — a "wrong metadata" (Code B) case rather than a
fabrication. The remaining 12 unaudited references would need separate checking before
the full bibliography could be called validated. This distinction — a high sample score
vs. full-bibliography confidence — is the central methodological lesson of the audit.

## How to use this repo

1. Read `paper/AI_Assisted_Research_Paper.pdf` for the taxonomy and argument.
2. Read `citation-audit/Citation_Integrity_Audit.pdf` for the verification methodology
   and results.
3. Use `references/references.md` as a starting point if you want to verify the
   remaining, unaudited citations yourself, or to read the primary sources directly.
4. Use `datasets/datasets.md` and `tools/tools.md` to explore the benchmarks and
   frameworks the paper discusses.

## License

See [`LICENSE`](./LICENSE).
