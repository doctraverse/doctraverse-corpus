# Doc Traverse Corpus

**Document intelligence for people, teams, and AI agents.**

Doc Traverse Corpus is a document intelligence platform in early development.
It is designed to turn PDF, DOCX, Markdown, and other documents into structured,
searchable knowledge with references back to the source. The planned platform
combines document conversion, retrieval, and agent access, with self-hosted and
managed SaaS deployment under consideration.

> **Status: Design stage.** This repository currently contains project
> documentation and licensing. A runnable application, installation instructions,
> and verified format support are not available yet. The scope below describes
> the product direction; the first workflow and release scope are still being
> evaluated.

## Why Doc Traverse Corpus?

Document work often spans reports, specifications, policies, manuals, and
support material. A useful search result needs enough context to understand
the passage and a reference that lets a person or agent inspect the original.

The goal of Doc Traverse Corpus is to make a collection of documents usable
throughout that workflow: import the material, preserve its structure, find
relevant passages, and follow their sources. People could use the same document
corpus that supplies context to AI agents and connected applications.

## Planned document workflow

The intended workflow starts with a collection of documents and a question:

1. **Import documents.** Start with PDF, DOCX, and Markdown; define and test
   support for additional formats as development progresses.
2. **Build a structured corpus.** Normalize content into a Markdown-like or
   structured representation, retaining headings, sections, tables, and source
   metadata where the input allows it.
3. **Find relevant material.** Search the corpus and retrieve passages with
   their surrounding document structure and references to the original source.
4. **Use the evidence.** Make the retrieved material available to people,
   applications, and AI agents through appropriate interfaces, including a
   planned API and Model Context Protocol (MCP) integration.
5. **Manage shared use.** Add access controls, document updates, and team
   workflows as the product and deployment requirements become clearer.

Conversion quality, source-reference accuracy, retrieval quality, and data
boundaries will need published tests before these become supported capabilities.

## Modular product direction

The proposed architecture separates layers so they can be combined or used
independently. Module contracts and packaging remain design questions.

| Planned layer | Purpose |
| --- | --- |
| Document ingestion and conversion | Bring supported file formats into a common representation. |
| Document structure and provenance | Preserve useful structure, source identity, and references to the original material. |
| Search and retrieval | Find passages that can supply evidence and context for a task. |
| API and MCP access | Connect the corpus to applications and AI agents. |
| Team governance | Define permissions, update behavior, and shared document access. |
| Document workflows | Combine the layers for research, support, operations, and other document tasks. |

## Who is it for?

The intended audience includes people and teams working with document
collections, along with developers and integrators building document-based
applications or agent workflows. Examples being explored include:

- **Research and analysis:** compare reports and trace findings to source passages.
- **Support and operations:** locate relevant policies, procedures, and manuals.
- **Engineering and product work:** navigate specifications, technical references,
  and project decisions.
- **Agent integrations:** provide structured document context with references
  that an agent can follow.

These are candidate workflows. The first supported workflow will be chosen
through product discovery and implementation testing.

## Doc Traverse MCP and Doc Traverse Corpus

[Doc Traverse MCP](https://github.com/doctraverse/doctraverse) is the separate,
MIT-licensed developer project for AI coding agents exploring local Markdown
documentation. Doc Traverse Corpus extends the product direction to broader
document collections and team workflows.

Both projects are at the design stage. This table compares their intended scope:

| Aspect | Doc Traverse MCP | Doc Traverse Corpus |
| --- | --- | --- |
| Primary audience | Developers and open-source maintainers | People, teams, developers, and integrators working with documents |
| Initial document focus | Local Markdown documentation | PDF, DOCX, and Markdown, subject to format testing |
| Product scope | Documentation search and navigation through MCP | Conversion, structured retrieval, agent access, and document workflows |
| Deployment direction | Local developer tooling | Free self-hosted, paid Enterprise, and managed SaaS options under consideration |
| Current repository license | MIT | GNU AGPL v3.0 |

The MCP project retains its MIT license. Corpus has its own repository and
licensing policy.

## Self-hosted, Enterprise, and SaaS plans

The proposed delivery model includes a free self-hosted version, a paid
self-hosted Enterprise offering, and a managed SaaS service. These are plans;
there is no released deployment or hosted service yet.

Feature boundaries, infrastructure requirements, model-provider choices,
security controls, and pricing are still being worked out. Self-hosting alone
does not define where an AI client or a configured model provider sends data.
Verified data flows will be documented with the implementation.

## Installation and development

Doc Traverse Corpus does not have an installable release or a runnable service
yet. Setup commands, development instructions, and a small reproducible example
will be added when the first implementation is available.

## Contributing

Workflow feedback is welcome. [Open an issue](https://github.com/doctraverse/doctraverse-corpus/issues)
with the document task, the expected output, and a small public or synthetic
example. Include how you would verify that a retrieved passage and its source
reference are useful for the task.

Keep confidential documents and personal data out of public issues. Read
[CONTRIBUTING.md](CONTRIBUTING.md) before proposing code or documentation patches.
External patches will not be merged until contribution terms and their
acceptance process are ready for the planned dual-licensing model.

## License

This repository currently uses the [GNU Affero General Public License v3.0](LICENSE)
only (`AGPL-3.0-only`), except where separate applicable notices identify a
different license.
AGPL permits commercial use subject to its terms.

An alternative commercial license is planned for eligible project-owned code.
Commercial terms and the scope of any separately licensed Enterprise features
are being developed; they are not granted by this README. See
[LICENSING.md](LICENSING.md) for the current scope and
[dual-licensing readiness](docs/licensing-readiness.md) for the remaining work.

Product status last updated: **2026-10-14**.
