# Heima Labs

**Building local-first, intelligent home automation — no cloud, no rules, no manual configuration.**

Heima Labs is an open-source organization dedicated to making homes genuinely smart. Not programmable — *smart*. The kind of smart that works in the background without anyone having to think about it.

---

## The idea

Home automation today is still largely manual. You write rules. You maintain them. You fight them when they break. The home does exactly what you told it — nothing more, nothing less.

We're working on something different: a home that observes what happens, learns patterns over time, detects when something is off, and acts accordingly. Transparently, locally, without sending your data anywhere.

---

## Projects

### [ha-heima-component](https://github.com/heima-labs/ha-heima-component)
The core project. An intent-driven home intelligence engine for Home Assistant.

- Deterministic domain pipeline (presence, occupancy, house state, lighting, heating, security)
- Local behavioral learning: detects patterns, generates proposals, applies them after user approval
- Reactive behavior engine: fires pre-conditioned actions based on learned patterns
- No cloud. No ML libraries. No external dependencies.

**Status:** Active development · v0.4.x · installable via HACS

---

## What's coming

Heima v2 is in design. The roadmap includes:

- **Plugin framework** — any new home control domain (ventilation, energy, irrigation…) registers with a `depends_on` declaration and is evaluated in the correct DAG order automatically
- **IBehaviorAnalyzer** — unified interface for pattern detection and anomaly detection
- **Structural invariant checks** — per-cycle cross-domain consistency validation
- **Contextual inference** — multi-signal reasoning using conditional probability tables, no ML required
- **Outcome tracking** — verifies whether a fired reaction's predicted event materialized; feeds confidence back to the learning system

---

## How this is built

~99% of the code is written by LLM tools (Claude, ChatGPT). The human contribution is architecture, specifications, and roadmap decisions. This is partly a deliberate experiment in LLM-driven software development, and partly practical: the founder hasn't worked as a developer for several years. The specs exist before any code is written.

This changes what "contributing" means here. The most valuable input is real-world testing, architectural feedback, and domain knowledge — exactly what LLMs are not equipped to provide.

---

## Get involved

- **Try it** — [install via HACS](https://github.com/heima-labs/ha-heima-component#install-hacs-custom-repo) and report what happens in your environment
- **Contribute** — open issues are tagged; Python + HA async patterns required
- **Discuss** — open an issue or join the HA Community thread *(link coming soon)*

---

*The success metric is invisibility. If the people living in the home never notice the system and things simply happen at the right moment — it's working.*
