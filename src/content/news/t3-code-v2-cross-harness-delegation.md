---
title: "T3 Code V2 brings cross-harness delegation to its agent control plane"
description: "T3 Code 0.1.0 makes Orchestrator V2 stable, with delegated child threads, MCP coordination and restart-aware queues; provider handoffs and upgrades have explicit limits."
date: 2026-10-17T10:22:34Z
playerSlug: "t3-code"
sourceName: "T3 Code v0.1.0 release"
sourceUrl: "https://github.com/pingdotgg/t3code/releases/tag/v0.1.0"
category: "Release"
tags:
  - coding-agents
  - delegation
  - multi-harness
  - MCP
  - open-source
draft: false
ogImage: "/images/players/t3-code/t3-code-official-desktop.webp"
---

[T3 Code 0.1.0](https://github.com/pingdotgg/t3code/releases/tag/v0.1.0), published October 15, 2026 at 23:18 UTC, makes Orchestrator V2 stable. The MIT-licensed control plane now lets a parent agent use `delegate_task` to start child threads on another provider or model, continue working or wait, and receive their results.

That makes T3 Code relevant beyond running several coding sessions side by side. Its [release notes](https://github.com/pingdotgg/t3code/releases/tag/v0.1.0) document an MCP surface for creating, launching, messaging, waiting on and interrupting threads, plus worktree handoffs. Child threads retain their own provider-native histories, while lineage shows their model, status and results. Server-side queues retain their order across restarts and wait for the operator to resume them.

![T3 Code desktop interface with project threads, an agent response and a pull-request diff.](/images/players/t3-code/t3-code-official-desktop.webp)

*Product image supplied on the [official T3 Code website](https://t3.codes/), retrieved October 17, 2026; not a local test run or a demonstration of every V2 feature.*

The attention is visible, but should stay in proportion. GitHub reported **28,030 stars and 7,503 forks on October 17**. An [October 17 comparison post on X](https://x.com/zqkrq/status/2111296531470889444) discussing V2 had **174 likes, 32 replies and 19,328 views** when checked. That is a useful discussion signal, not a benchmark, active-user count or 30-day growth rate. A [September 30 Reddit thread](https://www.reddit.com/r/codex/comments/1wtspqv/will_openai_forbid_subscription_usage_in/) also mentions T3 Code among third-party harnesses, but centers on subscription-access concerns rather than product adoption.

There are practical limits. Switching providers passes a budgeted selection of messages, omitting the prior provider's reasoning, tool calls, results and attachments; the release recommends delegation for combining harnesses. V2 copies the V1 database once, and V1 clients cannot connect to a V2 server. Provider setup and charges remain separate. The [permission guide](https://github.com/pingdotgg/t3code/blob/v0.1.0/docs/user/permission-modes.md) says new threads initially default to Full access, so operators should choose their permission policy deliberately. The [README](https://github.com/pingdotgg/t3code/blob/v0.1.0/README.md) still cautions that the project is early and bugs should be expected.

## Provider apps and feature fit

T3 is a fit for consolidating coding-agent work; keep the provider apps for native workflows you depend on. Its [Codex guide](https://github.com/pingdotgg/t3code/blob/v0.1.0/docs/user/providers-codex.md) supports a ChatGPT plan or existing Codex login, while its [Claude guide](https://github.com/pingdotgg/t3code/blob/v0.1.0/docs/user/providers-claude.md) uses Claude Code's login and configuration. OpenAI explicitly says [plan sharing does not grant access to ChatGPT conversations or memories](https://learn.chatgpt.com/docs/sign-in-with-chatgpt). No T3-specific support was verified for embedding or syncing a [dot](https://learn.chatgpt.com/docs/dots), or [Space](https://learn.chatgpt.com/docs/space) collaboration and permissions. T3 does document [ChatGPT calling its environment through separately authorized MCP](https://github.com/pingdotgg/t3code/blob/v0.1.0/docs/user/outside-agents.md); that is a connection between systems.

T3 has [sandboxed HTML replies and Codex-only MCP Apps rendering](https://github.com/pingdotgg/t3code/blob/v0.1.0/docs/user/html-renders.md). Anthropic also supports [Artifacts in Claude Code](https://support.claude.com/en/articles/17153992-what-are-artifacts-and-how-do-i-use-them), but the complete artifact editing, publishing and synchronization workflow inside T3 was not verified. T3's own schedules and [supported-iOS voice transcription into a draft](https://github.com/pingdotgg/t3code/blob/v0.1.0/docs/internals/voice-input.md) likewise do not establish native automation or real-time voice parity; its voice implementation explicitly lacks environment-backed transcription.

For Agent Analytics, the useful follow-up starts after the coding work ships. A T3 parent can delegate an onboarding change and its review; after deployment, a separately configured analytics task can verify `signup_completed` and `first_project_created`, then compare their observed counts and conversion with the prior period. Those events measure the product users receive. T3's child-thread status, token usage and queue recovery remain orchestration telemetry. This is an optional workflow, with tracking and authorized analytics access configured separately; no native T3 Code–Agent Analytics integration was verified, and a before/after change alone does not establish causation.

Source confidence: High for documented release behavior, MIT license and upgrade limits; moderate for traction, which consists of cumulative repository counts and a small public-discussion sample. Runtime reliability was not tested in this pilot.

Evidence:

- [T3 Code v0.1.0 release](https://github.com/pingdotgg/t3code/releases/tag/v0.1.0)
- [Repository metadata](https://api.github.com/repos/pingdotgg/t3code) and [MIT license at v0.1.0](https://github.com/pingdotgg/t3code/blob/v0.1.0/LICENSE)
- [Official product website and image](https://t3.codes/)
- [October 17 X discussion](https://x.com/zqkrq/status/2111296531470889444)
- [September 30 Reddit discussion](https://www.reddit.com/r/codex/comments/1wtspqv/will_openai_forbid_subscription_usage_in/)
- [Agent Analytics documentation](https://docs.agentanalytics.sh/)
