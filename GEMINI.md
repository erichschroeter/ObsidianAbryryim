# LLM Wiki Instructions

This file defines the structure, conventions, and workflows for the ObsidianAbryryim LLM Wiki.

## Directory Structure

- `/raw/`: Contains original, immutable source documents (articles, papers, logs).
- `/wiki/`: Contains the LLM-generated wiki pages.
    - `/wiki/assets/`: Contains images and other media referenced by wiki pages.
    - `/wiki/index.md`: A catalog of all pages in the wiki.
    - `/wiki/log.md`: A chronological record of all operations.

## Core Workflows

### 1. Ingest Source
When a new file is added to `/raw/`, follow these steps:
1.  **Read**: Analyze the source document.
2.  **Discuss**: Share key takeaways and proposed wiki updates with the user.
3.  **Implement**: 
    - Create or update a source-specific summary page in `/wiki/`.
    - Update or create relevant entity/concept pages in `/wiki/`.
    - Maintain cross-references (links) between pages.
    - Update `/wiki/index.md`.
    - Append an entry to `/wiki/log.md`.

### 2. Query Wiki
When answering questions:
1.  Check `/wiki/index.md` to identify relevant pages.
2.  Read the identified wiki pages.
3.  Synthesize an answer with citations back to the wiki pages.
4.  **Propose**: Suggest if the answer should be saved as a new wiki page.

### 3. Maintain (Lint)
Periodically:
- Check for broken links.
- Identify contradictions between pages.
- Flag orphan pages.
- Suggest new areas for research or missing connections.

## Formatting Conventions
- All wiki pages must be in Markdown.
- Use `[[Page Name]]` for internal links.
- Every page should have a brief summary at the top.
- Include a "Sources" section at the bottom linking back to the raw files.
- Use YAML frontmatter for metadata (e.g., `tags`, `last_updated`).

## Log Format
Use the following prefix for log entries:
`## [YYYY-MM-DD] <operation> | <description>`
Operations: `ingest`, `query`, `lint`, `refactor`.
