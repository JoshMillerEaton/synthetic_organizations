You are editing a markdown document that contains exactly two top-level subsections:

- `## GPT Generated`
- `## Claude Generated`

Treat these two sections as completely independent citation systems.

## Objective

Normalize inline citations and add a section-specific references list for each section without changing any non-citation text.

## Required Changes (apply separately to each section)

1. Detect all inline citations matching this pattern:  
   `[N](URL)` where `N` is any integer and `URL` is any `http`/`https` link.

2. Build a section-local citation map by **first appearance of each unique URL**:
   - First unique URL in that section becomes `[1]`
   - Second unique URL becomes `[2]`
   - Continue sequentially.

3. Replace every inline citation `[N](URL)` with plain numeric form `[k]` using the new map.

4. Collapse immediate duplicates after replacement:
   - `[k][k]` -> `[k]`
   - `[k] [k]` -> `[k]`
   Repeat until no adjacent duplicates remain.

5. Append a references block at the end of each section:
   - GPT references block must be inserted immediately before `## Claude Generated`
   - Claude references block must be inserted at end of file
   - Format exactly:

```markdown
### References

[1] https://example.com/first-url
[2] https://example.com/second-url
```

## Strict Constraints

- Do **not** modify prose, headings, punctuation, spacing, capitalization, wording, or ordering of non-citation content.
- Do **not** merge GPT and Claude reference numbering.
- Do **not** renumber based on old citation numbers; renumber only by first URL appearance in that section.
- Preserve all original URLs exactly (no rewriting, no decoding/encoding changes).
- If a URL appears multiple times in a section, it must always reuse the same number in that section.

## Validation Checklist (must pass before finishing)

- No inline markdown citation links remain (`[N](URL)` should be zero occurrences).
- GPT section has its own `### References` block with sequential numbering starting at 1.
- Claude section has its own `### References` block with sequential numbering starting at 1.
- Every inline `[k]` in each section has a corresponding `[k] URL` in that section’s references block.
- No adjacent duplicate inline citations remain.

Return only the updated document content.