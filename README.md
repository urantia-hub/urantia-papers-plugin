# Urantia Papers Plugin for Claude Code

Search, read, and explore the Urantia Book through the [Urantia Papers API](https://urantia.dev). Gives Claude 13 tools for paragraphs, search, entities, and audio — zero setup.

## Install

```
/plugin install urantia-papers
```

## What's Included

- **MCP Server** — Connects to `api.urantia.dev/mcp` (Streamable HTTP, no local process)
- **Research Skill** — Guides Claude toward accurate, well-cited responses using optimal tool patterns

## Tools Available

| Tool | Description |
|------|-------------|
| `get_table_of_contents` | Full table of contents — 4 parts, 197 papers |
| `list_papers` | All 197 papers with metadata |
| `get_paper` | Single paper with all paragraphs |
| `get_paper_sections` | Sections within a paper |
| `get_paragraph` | Paragraph by reference (e.g., `2:5.10`) |
| `get_paragraph_context` | Paragraph with surrounding context |
| `get_random_paragraph` | Random paragraph for exploration |
| `search` | Full-text search (and/or/phrase modes) |
| `semantic_search` | Meaning-based similarity search |
| `list_entities` | Browse 4,400+ entities |
| `get_entity` | Entity details and cross-references |
| `get_entity_paragraphs` | All paragraphs mentioning an entity |
| `get_audio` | Audio file URLs for a paragraph |

## Example Prompts

- "What does the Urantia Book say about what happens after death?"
- "Search for passages about love and service"
- "Read Paper 1 about the Universal Father"
- "Who is Machiventa Melchizedek?"
- "Show me paragraph 2:5.10 with surrounding context"

## Links

- [API Documentation](https://urantia.dev)
- [MCP Server Setup](https://urantia.dev/mcp-servers)
- [API Reference](https://urantia.dev/api-reference/introduction)

## License

This project is licensed under the [MIT License](./LICENSE).

## Disclaimer

This is an independent community project by [Adams Technologies LLC](https://adamstechnologies.com). It is not affiliated with, endorsed by, or connected with Urantia Foundation. The original English text of *The Urantia Book* is in the public domain (*Michael Foundation v. Urantia Foundation*, 10th Cir. 2003). All use of "Urantia" is nominative fair use to identify the subject matter.
