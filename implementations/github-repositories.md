# Open-Source Implementations

Repositories implementing the papers and benchmarks discussed in the taxonomy. Links
were spot-checked at the time of writing; verify they still resolve before relying on
them, in the same spirit as the citation-integrity audit in this repo.

| Project | Repository | Relevance |
|---|---|---|
| AgentBench | https://github.com/THUDM/AgentBench | Multi-environment agent evaluation (§2.2, §3.1, §5.4 of the paper) — **[verified]** |
| ReAct | https://github.com/ysymyth/ReAct | Reference implementation of the reasoning–acting loop (§2.1, §5.2) |
| Reflexion | https://github.com/noahshinn/reflexion | Verbal reinforcement learning / self-reflection agent (§2.3, §5.3) |
| Voyager | https://github.com/MineDojo/Voyager | Embodied agent with iterative self-verification (§2.3) |
| ToolLLM / ToolBench | https://github.com/OpenBMB/ToolBench | Large-scale real-world API tool-use dataset and training (§2.1, §3.2) |
| WebArena | https://github.com/web-arena-x/webarena | Realistic long-horizon web-agent benchmark (§2.2, §5.4) |
| AgentDojo | https://github.com/ethz-spylab/agentdojo | Prompt-injection / untrusted-data agent security benchmark (§3.6, §5.4, §7.8) |

## Notes

- Only **AgentBench** was directly re-confirmed via a fresh search while compiling this
  file; the others reflect commonly cited canonical repositories for these projects but
  were **not individually re-verified** here. Treat unverified rows as leads, and check
  the repo (and that it matches the paper you expect) before using it.
- If you fork or clone any of these, note the commit hash you used — long-horizon agent
  repos change quickly, and reproducibility depends on pinning a version.

