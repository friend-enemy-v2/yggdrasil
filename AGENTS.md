# Yggdrasil

Yggdrasil is a personal knowledge repository.

The repository stores knowledge collected from articles, documentation, videos, repositories, books, news, and other sources.

Its purpose is not only to archive information, but to make past knowledge reusable when answering questions, thinking through problems, or making decisions.

## Language

Responses to the user should be written in Japanese unless explicitly requested otherwise.

Knowledge files may use English where appropriate for metadata, technical terms, or identifiers.

## Knowledge Storage

Knowledge is stored under:

```text
knowledge/YYYYMMDD.md
```

Use the date the material was added to Yggdrasil.

Multiple sources collected on the same day should normally be appended to the same file.

Do not create unnecessary directories or classifications. Prefer simple Markdown and metadata that can be searched later.

## Ingesting Knowledge

When the user provides an article, URL, document, video, repository, or other source:

1. Read the source as completely as reasonably possible.
2. Identify its important claims, reasoning, evidence, examples, limitations, and practical implications.
3. Add the result to the appropriate daily knowledge file.
4. Preserve the original source URL.
5. Add lightweight tags when useful.

A summary should not merely be short.

Prefer retaining enough information that a future AI agent can understand and reuse the source's important ideas without immediately reopening the original material.

Do not remove useful details solely for brevity.

## Source Fidelity

Clearly distinguish between:

- what the source says
- interpretations or connections inferred by the agent

Never invent missing content.

If a source cannot be accessed, is only partially available, or cannot be reliably understood, record that limitation instead of guessing its contents.

Prefer primary sources when they are available.

## Using Knowledge

When the user asks a question, requests advice, or wants help thinking through a problem:

1. Search `knowledge/` for relevant material.
2. Read the most relevant sources.
3. Look for connections, agreements, contradictions, and useful examples across multiple sources.
4. Use that knowledge as context for the answer.
5. Clearly identify the materials that materially informed the answer.

Do not force stored knowledge into an answer when it is not relevant.

The goal is not to repeat summaries, but to use accumulated knowledge as evidence and context for useful reasoning.

## Knowledge Connections

Related knowledge may exist across different dates and sources.

When useful, connect ideas across the repository rather than treating each entry independently.

For example, multiple sources about AI development may collectively provide perspectives on:

- understanding debt
- context engineering
- harness engineering
- requirements
- review
- product judgment

Prefer discovering these relationships at retrieval time rather than maintaining a complex manual taxonomy.

## Keep Yggdrasil Simple

Yggdrasil should remain easy for both humans and AI agents to understand.

Prefer:

- Markdown
- simple directory structures
- lightweight metadata
- search and retrieval at runtime

Avoid adding databases, vector stores, indexing systems, frameworks, or other infrastructure until the repository has a demonstrated need for them.

Do not expand `AGENTS.md` with large amounts of domain knowledge.

Domain knowledge belongs in `knowledge/`.

`AGENTS.md` should describe how Yggdrasil behaves, not contain Yggdrasil's knowledge.
