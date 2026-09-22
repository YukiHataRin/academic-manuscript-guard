# Dimension-specific manuscript review

## Roles and boundaries

Use four bounded reviewer roles. Roles may run in batches when concurrency is limited; do not exceed available slots or recursively delegate. Each reviewer receives the same immutable source with paragraph IDs, the user's instructions, relevant study facts and terminology decisions, and SKILL.md. Include sufficient surrounding context. Reviewers return findings without editing shared files or communicating externally.

| Reviewer | Question | Important boundary |
| --- | --- | --- |
| Drafting residue | Does prose narrate author–AI discussion, naming negotiations, revision plans, or instructions to the author? | Keep settled definitions and useful reader signposting. |
| Framing and scope | Does an irrelevant denial or defensive appeal obscure the actual research aim? | Retain scientific negation, scope boundaries, exclusions, and limitations; do not invent an aim. |
| Scientific fidelity | Are claims faithful to supplied evidence, and would proposed edits alter their strength or qualifications? | Preserve numbers, citations, equations, population, uncertainty, negative findings, methodological rationale, and attribution. Do not claim external fact-checking. |
| Terminology and voice | Are names, abbreviations, and manuscript voice consistent with supplied decisions and genre? | Do not settle tentative terminology or flatten direct quotations, methods rationale, or legitimate metadiscourse. |

For each role, use this task template with the specific row's remit:

```text
Read the supplied SKILL.md and review only the assigned dimension: [role and remit].
User instructions and genre: [constraints].
Known scientific context and finalized terminology: [facts, with unknowns explicit].
Source manuscript: [immutable text with paragraph IDs].
Return actionable findings with paragraph ID, exact excerpt, explanation, proposed
minimal edit or clarification, and scientific information that must be preserved.
Label each finding as meaning risk, manuscript-voice issue, or optional style.
List unresolved dependencies and relevant passages that should remain unchanged.
Do not invent findings to fill a quota. Do not edit files or spawn agents.
```

## Coordination and integration

1. Preserve the source separately. For drafting tasks, also supply the underlying study facts so the generated draft cannot become its own evidence. For long manuscripts, give each reviewer coherent sections plus shared definitions and relevant cross-section context; record any unreviewed sections.
2. Dispatch independent reviews with bounded scopes. With three available worker slots, run three roles concurrently and the fourth after a slot frees. The coordinator can map protected facts and manuscript boundaries while they work.
3. Deduplicate findings by passage and cause. Judge suggestions against the source, not majority vote. Factual fidelity and explicit user constraints take precedence over stylistic preferences. Preserve limitations when removing defensive wrappers. Reject unsupported changes and identify consequential unknowns separately.
4. Produce one integrated candidate for revision or drafting. For audit-only tasks, integrate proposed edits without rewriting the whole manuscript.
5. Send the original, study context, and integrated candidate (or audit suggestions) to the scientific-fidelity reviewer for a comparison pass. Require exact locations for any changed numbers, conditions, citations, claim strength, or missing caveats. Then resolve supported findings and inspect the affected passages. Re-run comparison only for substantive new changes; do not iterate to stylistic unanimity.
6. Deliver the requested artifact. When review reporting is appropriate, state which roles actually completed, any material coverage gaps, and unresolved author decisions outside manuscript prose. If the user requests only clean text, omit the process report. Never label a local sequential pass an independent multi-agent review.

If an agent fails, retry once when useful or complete that dimension locally, accurately recording the substitution. Do not silently omit the dimension or claim that a timed-out reviewer approved the text. A request for review does not authorize uploading unpublished text to another external service.
