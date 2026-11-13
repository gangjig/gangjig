# Hi, I'm Gang Ji

Software engineer working on AI agent systems — harnesses, evaluation, and the
tooling that makes agents reliable in production. My open-source projects are
small, tested, single-purpose tools built around ideas from current agent
research, each with a design note explaining the trade-offs.

## Featured projects

- **[ace-in-a-box](https://github.com/gangjig/ace-in-a-box)** — A self-evolving
  playbook framework for agents (ACE-style): structured context bullets with
  helpful/harmful feedback, curation, and budget-aware rendering. *150 tests*
- **[stateledger](https://github.com/gangjig/stateledger)** — Explicit-state
  memory for long-running agents: append-only evidence kept separate from
  conclusions, with full provenance. *71 tests*
- **[decidekit](https://github.com/gangjig/decidekit)** — Evaluate decision
  models (yes-no / choice / score) on accuracy, calibration (Brier, ECE), and
  cost per correct decision. *81 tests*
- **[cost-per-task](https://github.com/gangjig/cost-per-task)** — Rank LLMs by
  cost per *successful* task, not price per token — retries and failures
  included. *80 tests*
- **[agent-hooks](https://github.com/gangjig/agent-hooks)** — Pre-commit hooks
  that enforce your rules on AI coding agents; rejection output is a corrective
  instruction written for the agent. *91 tests*
- **[llm-decide](https://github.com/gangjig/llm-decide)** — Plugin for Simon
  Willison's `llm` CLI: typed decision commands returning structured JSON
  instead of prose. *28 tests*
- **[eval-leakcheck](https://github.com/gangjig/eval-leakcheck)** —
  Pre-publish leakage scanner for eval/training task repos: finds solutions
  hiding in leftover Git objects, history, side branches, and the working
  tree. *89 tests*
- **[agent-replay-diff](https://github.com/gangjig/agent-replay-diff)** —
  Find where repeated runs of the same agent task diverge: volatile tool
  outputs (timestamps, IDs, latencies) are normalized away, then traces are
  diffed step by step to the first real fork. *138 tests*
- **[verifier-forge](https://github.com/gangjig/verifier-forge)** —
  Generate a verifier for an agent task from a spec (evidence head +
  domain rules), then self-test it against constructed candidates with
  known verdicts and grade the agreement — false passes are named as
  verifier holes and cap the grade. *49 tests*
- **[mcp-faultcheck](https://github.com/gangjig/mcp-faultcheck)** —
  Fault-injection harness for MCP servers: a stdio proxy injects tool
  failures (timeouts, empty/malformed results, JSON-RPC errors, wrong-typed
  fields) and reports how much task success each fault type costs; a goals
  mode hands the agent unachievable tasks and checks whether it concedes
  honestly instead of spinning or claiming false success. *96 tests*
- **[llm-spend](https://github.com/gangjig/llm-spend)** — Plugin for Simon
  Willison's `llm` CLI: price what your `llm` history actually cost, from
  the token usage already logged in its database. *11 tests*
- **[provider-parity](https://github.com/gangjig/provider-parity)** — Check
  whether the same model name served through different providers is really
  the same model: one fixed suite of probes against OpenAI-compatible
  endpoints, compared with evidence. *39 tests*
- **[llm-cassette](https://github.com/gangjig/llm-cassette)** — VCR for LLM
  calls: record an agent's model calls once, replay them in tests forever
  — offline, deterministic, free. *40 tests*
- **[tracecheck](https://github.com/gangjig/tracecheck)** — Unit tests for
  agent behavior: deterministic assertions over the trace your agent
  actually left behind, with every failure naming the exact step. *15 tests*
- **[contextpack](https://github.com/gangjig/contextpack)** — Assemble LLM
  context under a hard token budget, with the drop decisions explicit and
  a manifest to prove them. *19 tests*
- **[compaction-bench](https://github.com/gangjig/compaction-bench)** —
  Compare context-compaction strategies (full history, single-action,
  end-of-conversation, sliding window, periodic summary) on the same
  traces: success rate, peak context, and token cost in one table.
  *44 tests*
- **[cred-proxy](https://github.com/gangjig/cred-proxy)** — Local egress
  proxy that swaps real API credentials in at request time: the agent
  sends a placeholder, only declared routes are forwarded, and secrets
  are redacted out of responses. *52 tests*
- **[trace-waste](https://github.com/gangjig/trace-waste)** — Audit an
  agent's run traces for wasted tokens: repeated tool calls, redundant
  reasoning, and tool results or context that nothing later used — with
  the waste share and estimated savings broken down by category.
  *45 tests*
- **[bypass-battery](https://github.com/gangjig/bypass-battery)** —
  Adversarial test battery for URL validators: a fixed corpus of hostile
  inputs with browser ground truth (backslash authority truncation,
  numeric IP encodings, Unicode dots, redirect chains) catches the gaps
  between what a validator checks and what the consumer of the value
  actually does — locally, with no Docker and no LLM. *28 tests*

## What I care about

- Agent harness design: context engineering, explicit state, self-improvement loops
- Evaluation that matches production: calibration and cost per successful task,
  not leaderboard scores or per-token prices
- Guardrails enforced by tooling, not by hoping the model follows instructions

All projects are MIT-licensed, tested, and built to be read — start with the
README and the design notes.
