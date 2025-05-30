## Slopsquatting: Hallucination in Coding Agents and Vibe Coding

This repository provides the dataset and research materials for evaluating hallucination in AI-driven coding workflows, specifically focusing on slopsquatting attacks—where adversaries exploit language-model hallucinations to publish malicious dependencies on public package repositories.

### Background

Early research into foundation-model hallucinations first highlighted how language models could invent plausible but non-existent package names—exposing developers to supply-chain risks when blindly installing dependencies. These phantom packages can facilitate slopsquatting attacks, in which adversaries register AI-hallucinated names on public package repositories and embed malware in them.

To address this, we evaluate two advanced paradigms across 100 realistic web-development tasks:

1. **Reasoning-Enhanced Coding Agents**: Integrates web-search capabilities and chain-of-thought prompting to reduce hallucinations.
2. **Vibe-Coding Workflow**: Augmented by MCP (Model Context Protocol)  validation to catch phantom dependencies in real time.

### Findings

* Reasoning-enhanced agents reduce hallucination rates compared to baseline coding agents.
* Vibe coding with live MCP checks achieves the fewest phantom dependencies.
* Neither approach fully eliminates the threat of AI-generated malicious packages.

Despite these advances, AI-generated dependencies remain vulnerable to supply-chain attacks. Mitigating slopsquatting in AI-driven development requires:

* **Developers**: Rigorously vet all installations, avoid blind reliance on AI suggestions.
* **Vendors**: Implement automated dependency-checking tools and vetting pipelines.
* **Community**: Adopt systematic, verifiable frameworks for package validation.

---

### Data

The dataset for this research is provided in JSON Lines format:

```
./slopsquatting.jsonl
```

Each entry includes model, task, AI-generated dependencies, and hallucinated package names.


### License

This project is released under the MIT License. See [LICENSE](LICENSE.MD) for details.

---

### Contribution

Contributions and feedback are welcome! Please open issues or pull requests in this repository.
