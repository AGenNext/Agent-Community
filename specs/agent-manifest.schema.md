# Agent Manifest Specification

## Purpose

The agent manifest defines a portable, standardized structure for publishing and operating agents.

## Proposed structure

```yaml
id: research-agent
name: Research Agent
version: 0.1.0
owner: community
category: research

purpose:
  summary: Performs structured research tasks.

capabilities:
  - web_research
  - summarization
  - citation_generation

runtime:
  provider: openai
  framework: agents-sdk

permissions:
  internet: true
  filesystem: false
  external_actions: false

memory:
  persistent: false
  session_scoped: true

governance:
  risk_level: medium
  human_approval_required: false

observability:
  logging: true
  traces: true

interfaces:
  input:
    type: text
  output:
    type: markdown
```

## Design principles

- Human-readable
- Portable across runtimes
- Extensible
- Governance-aware
- Compatible with orchestration systems

## Future additions

- Tool schemas
- Evaluation metadata
- Safety constraints
- Marketplace metadata
- Multi-agent role definitions
- Resource usage policies
