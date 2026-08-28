# Datasets and Benchmarks

Interactive benchmarks and evaluation environments relevant to chained tool-calling
agent reliability, as discussed in the paper. These are the datasets where failure
modes in the six-class taxonomy have been empirically observed.

| Benchmark | Focus | Reported in paper |
|---|---|---|
| **AgentBench** | Evaluates agents across eight diverse environments; identifies long-term reasoning, decision-making, and instruction-following as major failure sources. | §2.2, §3.1, §5.4 |
| **WebArena** | Realistic, functioning websites with long-horizon tasks; large human vs. agent performance gap (78.24% human vs. 14.41% for the strongest GPT-4-based agent in the paper's cited figures). | §2.2, §5.4 |
| **Mind2Web** | Realistic websites spanning many domains and interface patterns, used to test generalization beyond simplified environments. | §2.2 |
| **τ-bench** | Dynamic user–agent conversations with APIs and policy rules; introduces `pass^k` for repeated-trial reliability, reporting sub-50% task success and trial-to-trial inconsistency for leading function-calling agents. | §2.2, §4, §5.4, §7.2 |
| **AgentDojo** | Evaluates agents operating on untrusted data (email, banking, travel tasks); demonstrates prompt-injection-style hijacking of subsequent tool use. | §3.6, §5.4, §7.8 |
| **Agent Security Bench (ASB)** | Benchmarks vulnerabilities across system prompts, user prompts, tool usage, and memory retrieval. | §3.3, §3.6, §6.3, §7.8 |
| **AgentHarm** | Measures harmful multi-step agent behavior when safeguards are bypassed or insufficiently robust. | §3.6 |
| **SafeToolBench** | Prospective (pre-execution) safety evaluation of intended tool invocations, rather than retrospective harm assessment. | §5.5 |
| **Agent-SafetyBench** | Referenced alongside ASB as part of the shift toward interactive, safety-focused benchmarking. | §5.4, §6.3 |

## Notes

- These benchmarks are cited in the paper by name; only a subset of the paper's
  underlying citations were independently verified in the citation-integrity audit
  (see `../references/references.md` for verification status of the associated papers).
- Before using any of these benchmarks in your own work, check the original
  publication/repository directly rather than relying solely on this summary table.
