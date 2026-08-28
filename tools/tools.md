# Tools, Frameworks, and Methods

## Tools used to produce this project

- **Paper generation**: ChatGPT (GPT-5.6 "Luna"), as recorded in Part B of
  `../citation-audit/Citation_Integrity_Audit.pdf`. Used per the assignment
  requirement to generate the research paper with an AI tool.
- **Citation verification**: [arxiv.org](https://arxiv.org/) and
  [Springer.com](https://www.springer.com/), used to check whether each audited
  reference's publication, title, authors, year, venue, and identifier (DOI/arXiv ID)
  actually matched what the AI-generated paper claimed (Part G of the audit).

This is the actual toolset behind this repository, separate from the sections below,
which summarize the tools/frameworks the *paper itself discusses* as part of its
subject matter (chained tool-calling agent reliability).

## Tools and frameworks discussed in the paper

Frameworks, training approaches, and architectural patterns discussed in the paper as
mitigations (partial) for chained tool-calling agent failure modes.

## Tool-use training / invocation

- **Toolformer** — self-supervised training for when/how to invoke external APIs.
- **ToolLLM** — large-scale tool-use dataset and evaluation across 16,000+ real-world
  APIs, addressing tool-selection and argument-generation failures (taxonomy §3.2).

## Reasoning–acting loops

- **ReAct** — interleaves reasoning ("thought") and acting ("action") steps with
  environment observation, reducing (but not eliminating) hallucination and premature
  commitment (taxonomy §3.1).

## Self-correction / reflection

- **Self-Refine** — iterative self-feedback and revision without weight updates.
- **Reflexion** — stores verbal reflections derived from environment feedback for use
  in future attempts; illustrates both the value and the "verification-ceiling problem"
  of self-correction (paper §2.3, §5.3).
- **Voyager** — embodied agent incorporating execution errors, environment feedback,
  and self-verification into an iterative loop.

## Prospective / architectural safety mechanisms

- **SafeToolBench-style prospective safety assessment** — evaluates whether an
  intended tool call is unsafe *before* execution rather than after harm occurs.
- **Verifiably safe tool use (constraint-based)** — translates hazards into explicit
  constraints on tool sequences and data flows (capability, confidentiality, trust
  labels), aiming for system-level guarantees independent of model judgment (paper
  §5.5, §7.3, §7.7).

## Architectural patterns proposed in the paper (not yet named tools/libraries)

These are conceptual, not existing software packages — useful as a checklist when
evaluating or building agent frameworks:

- **Role separation**: planner / executor / verifier / policy engine / monitor,
  instead of a single LLM performing all functions (§7.5).
- **Transactional execution**: plan → stage/simulate → validate → execute → verify
  postconditions → commit or roll back (§7.4).
- **Adaptive checkpointing**: trigger human or stronger-verification review when a
  computed risk score `R_t = f(U_t, I_t, P_t, C_t)` (uncertainty, impact, privilege,
  consequence) exceeds a threshold (§7.1).
- **Security-aware / provenance-tagged memory**: distinguish observed facts,
  model-generated hypotheses, user assertions, and untrusted external content, each
  with provenance, confidence, and access control (§7.6).

## Notes

- This list summarizes what the paper describes; it does not constitute independent
  verification of each cited work's existence or accuracy. Cross-reference with
  `../references/references.md`.

