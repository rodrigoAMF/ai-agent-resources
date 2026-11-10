---
name: technical-writing-guidelines
description: Use when writing or reviewing technical documentation, design docs, RFCs, proposals, ADRs, or architecture documents, or when a technical document feels too long, repetitive, or padded.
---

# Technical Writing Guidelines

## Core Philosophy

Optimize for clarity, not completeness.

Technical documentation communicates decisions, trade-offs, and implementation details. It does not demonstrate how much the author knows.

Prefer a short, understandable document over a comprehensive document that nobody wants to read.

## Before Writing

Settle three things first. Take them from the request; ask only if one is missing and cannot be inferred.

1. **Reader:** who reads it and what they already know.
2. **Decision:** what the reader must understand or approve.
3. **Size:** the length target from Document Length. If the request gives no size, assume small.

A length stated in the request overrides the suggested targets.

## Writing Style

- Be direct and concise.
- Use simple, natural language.
- Prefer active voice.
- Use short sentences.
- Keep paragraphs focused on one idea.
- Avoid corporate language and unnecessary formalities.
- Do not repeat information in different words.
- Prefer concrete statements over abstract descriptions.
- Do not use filler introductions or conclusions.

## Scope Control

- Document only what is relevant to the proposal.
- Do not introduce requirements that were not requested.
- Do not invent hypothetical scenarios to justify additional sections.
- Do not document obvious implementation details.
- Do not explain existing systems unless necessary to understand the proposed change.
- Avoid speculative future-proofing.
- Move genuinely useful but non-essential details to an appendix.
- Omit these sections unless the request asks for them or the change cannot be understood without them: Goals/Non-goals, Success Metrics, Risks and Mitigations, Rollout Plan, Monitoring, Security, Testing Strategy, Future Work, Glossary, Executive Summary.

## Self-Contained References

The reader has the document and the codebase. The reader does not have your conversation.

- Refer only to things the reader can find: real files, services, tickets, docs. Check each name against the code before using it.
- Do not invent facts: numbers, benchmarks, dates, owners, prior decisions, links, citations. If a fact is unknown, state it as an assumption or an open question.
- Do not coin labels ("Approach A", "Phase 2", "the Resilience Layer"). Use the names the codebase and team already use.
- Spell out an acronym at first use, unless the reader already knows it.
- Do not write "as discussed", "as mentioned earlier", or "the previous approach" unless the document itself contains it.

## Technical Decisions

- Clearly distinguish facts, assumptions, and decisions.
- Explain why the proposed solution is necessary.
- Include alternatives only when they were genuinely considered.
- Describe trade-offs only when they affect the decision.
- Avoid explaining concepts already familiar to the target audience.

## Anti-Patterns

NEVER:

- Repeat the same argument across multiple sections.
- Add generic "Benefits" sections that restate the proposal.
- Create lengthy introductions that repeat the problem statement.
- Add sections solely to make the document look comprehensive.
- Inflate simple ideas with unnecessary technical terminology.
- Use phrases like:
  - "It is important to note that..."
  - "It is worth mentioning that..."
  - "In order to..."
  - "Furthermore, it is important to highlight..."
  - "This provides a robust and scalable foundation..."

### Language Tells

Models swap a banned phrase for a synonym. Check the pattern, not just the words.

| Tell | Write instead |
|------|---------------|
| "serves as", "stands as", "boasts", "offers", "features" | "is", "has" |
| "leverage", "utilize", "facilitate", "ensure" | "use", "help", "make sure" |
| "robust", "seamless", "comprehensive", "holistic", "crucial", "pivotal" | A concrete property, or nothing |
| Trailing "-ing" clauses: "..., ensuring scalability" | A separate sentence with a fact, or cut it |
| "not just X, but Y" | State Y |
| Groups of three adjectives or nouns | Keep only the ones that carry information |
| Bullets that start with a bold label | Plain bullets or a sentence |
| Headings shaped "X and Y", or a heading above two sentences | Merge into the previous section |
| Many em dashes | Commas, periods, parentheses |

Test: if a sentence could appear in any document on any topic, delete it.

## Document Length

Use the smallest document that adequately communicates the proposal.

Suggested targets (not hard limits):

| Change size | Length | Words (about 500 per page) |
|-------------|--------|----------------------------|
| Small | 1-3 pages | 500-1,500 |
| Medium | 3-5 pages | 1,500-2,500 |
| Large architectural change | 5-10 pages | 2,500-5,000 |

If the document exceeds these targets, explain why the additional detail is necessary.

Never write more than 10 pages (5,000 words) unless the request asks for it.

## Final Review

Before delivering the document:

1. Remove redundant sentences and paragraphs.
2. Remove sections that do not contribute to a decision.
3. Replace unnecessarily complex language with simpler words.
4. Check whether every paragraph adds new information.
5. Verify that the proposal has not expanded beyond the original scope.
6. Prefer deleting content over adding explanations.

When in doubt, make the document shorter.
