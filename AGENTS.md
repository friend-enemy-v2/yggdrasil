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

If a source cannot be accessed, is only partially available, or cannot be reliably understood, do not place it in `knowledge/`. Record it in `failed.md` instead of guessing its contents.

Prefer primary sources when they are available.

## Failed Source Retry

Keep failed or incomplete retrievals in `failed.md`, separate from reusable knowledge.

Each failed entry should preserve the original URL, the date it was first requested, the last retry date, what retrieval methods were attempted, and why the source is still insufficient.

Retry entries in `failed.md` occasionally, especially when working on Yggdrasil ingestion or maintenance. Do not rely only on direct URL access: when appropriate, also try web search, exact-title/URL search, author/site search, canonical or primary sources, transcripts, cached/indexed copies, and legitimate mirrors or quotations.

When a retry succeeds and the source can be read sufficiently:
1. create or restore its proper summary in the original `knowledge/YYYYMMDD.md` file using the date it was first added;
2. assess reliability normally;
3. remove the entry from `failed.md`.

Do not leave placeholder summaries or `reliability: unscored` entries in `knowledge/`.

## Reliability Assessment

For every source that is sufficiently available to summarize, record a reliability assessment. Apply it to all knowledge entries, not only news or technical articles.

Use a deliberately conservative 100-point scale. A high score should require strong evidence, not merely plausible writing or a reputable-looking publisher. Consider primary-source proximity, citations/evidence, reproducibility or independent verifiability, separation of fact from opinion, freshness where time-sensitive, and whether important claims are appropriately qualified.

Treat opinion, design guidance, personal experience, case studies, product announcements, journalism, and primary technical specifications differently. Do not penalize a source merely for being an individual author, but do not treat personal experience as general evidence.

When the full source is unavailable or only partial information was obtained, write `reliability: unscored` and explain why rather than inventing a numeric score.

A reliability score evaluates how safely the stored claims can be reused as evidence; it is not a score for writing quality or the author's ability.

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
