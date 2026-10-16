# Hi, I'm Gang Ji

Software engineer working on AI agent systems — harnesses, evaluation, and the
tooling that makes agents reliable in production. My open-source projects are
small, tested, single-purpose tools built around ideas from current agent
research, each with a design note explaining the trade-offs.

## Featured projects

- **[ace-in-a-box](https://github.com/gangjig/ace-in-a-box)** — A self-evolving
  playbook framework for agents (ACE-style): structured context bullets with
  helpful/harmful feedback, curation, and budget-aware rendering. *56 tests*
- **[stateledger](https://github.com/gangjig/stateledger)** — Explicit-state
  memory for long-running agents: append-only evidence kept separate from
  conclusions, with full provenance. *50 tests*
- **[decidekit](https://github.com/gangjig/decidekit)** — Evaluate decision
  models (yes-no / choice / score) on accuracy, calibration (Brier, ECE), and
  cost per correct decision. *47 tests*
- **[cost-per-task](https://github.com/gangjig/cost-per-task)** — Rank LLMs by
  cost per *successful* task, not price per token — retries and failures
  included. *35 tests*
- **[agent-hooks](https://github.com/gangjig/agent-hooks)** — Pre-commit hooks
  that enforce your rules on AI coding agents; rejection output is a corrective
  instruction written for the agent. *38 tests*
- **[llm-decide](https://github.com/gangjig/llm-decide)** — Plugin for Simon
  Willison's `llm` CLI: typed decision commands returning structured JSON
  instead of prose. *28 tests*
- **[eval-leakcheck](https://github.com/gangjig/eval-leakcheck)** —
  Pre-publish leakage scanner for eval/training task repos: finds solutions
  hiding in leftover Git objects, history, side branches, and the working
  tree. *89 tests*

## What I care about

- Agent harness design: context engineering, explicit state, self-improvement loops
- Evaluation that matches production: calibration and cost per successful task,
  not leaderboard scores or per-token prices
- Guardrails enforced by tooling, not by hoping the model follows instructions

All projects are MIT-licensed, tested, and built to be read — start with the
README and the design notes.
