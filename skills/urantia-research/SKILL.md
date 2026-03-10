---
name: urantia-research
description: Guides accurate, well-cited research of the Urantia Book using the Urantia Papers API MCP tools. Use when answering questions about the Urantia Book, Urantia Papers, or related spiritual/cosmological topics.
---

You have access to the Urantia Papers API via MCP tools. Follow these patterns for accurate, well-cited responses.

## Tool Selection

- **Natural language questions** → `semantic_search` (finds conceptually related passages even without exact keyword matches)
- **Specific terms or phrases** → `search` with mode `and` (default) or `phrase`
- **Broad exploration** → `get_table_of_contents` first, then drill into relevant papers
- **Known references** → `get_paragraph_context` (NOT `get_paragraph` — always include surrounding context)
- **Entity questions** (beings, places, concepts) → `list_entities` with `q` param, then `get_entity` for details

## Research Workflow

1. **Orient**: If the topic is broad, call `get_table_of_contents` to find relevant papers
2. **Search**: Use `semantic_search` for the user's question to find the most relevant passages
3. **Expand**: For each key result, call `get_paragraph_context` with `window: 3` to get surrounding paragraphs
4. **Cross-reference**: Use `list_entities` to find related entities and `get_entity_paragraphs` for additional mentions
5. **Synthesize**: Combine findings into a clear answer with citations

## Citation Format

Always cite passages using the standard reference format: **Paper:Section.Paragraph**

Examples:
- "The Universal Father is the God of all creation" (0:0.1)
- "Love is the desire to do good to others" (56:10.20)

When quoting, use the exact text from the API response.

## Tips

- `semantic_search` returns a `similarity` score (0-1) — prioritize results above 0.7
- Both search endpoints support `paperId` and `partId` filters to narrow scope
- Use `include_entities` parameter on paragraph endpoints to see entity mentions inline
- The Urantia Book has 4 parts: I (Universal Father), II (Local Universe), III (History of Urantia), IV (Life of Jesus)
- There are 197 papers total, with ~14,500 paragraphs
