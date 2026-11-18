# Enterprise AI in Java, Objective by Objective

*The AI Architect's Domains Through the Nasdanika SDK*

A book that takes the decisions an architect of AI systems makes, one at a time, and asks of each: how
is this done in Java, with the [Nasdanika SDK](https://sdk.nasdanika.org)?

- **The book:** [nasdanika-sdk.github.io/enterprise-ai-in-java](https://nasdanika-sdk.github.io/enterprise-ai-in-java),
  also as [PDF](https://nasdanika-sdk.github.io/enterprise-ai-in-java/enterprise-ai-in-java.pdf) and
  [EPUB](https://nasdanika-sdk.github.io/enterprise-ai-in-java/enterprise-ai-in-java.epub).
- **The order:** the seven domains and thirty-nine skills of a public blueprint for AI architects, the
  content outline of Anthropic's exam guide for the Claude Certified Architect, Professional
  certification, version 1.1.
- **The lens:** what the Nasdanika SDK has released, has sketched and has planned for each skill.

It is a view of two semantic domains, AI architecture and the Nasdanika SDK, for one stakeholder, the
AI architect, in the vocabulary of the
[Nasdanika enterprise model](https://enterprise.models.nasdanika.org/).

## What state it is in

Every section of this edition is a sketch: it says how a thing would be done and has no code. Much of
what the blueprint asks for stands on capabilities of the SDK that are planned and not built, and
each section says which. Sections become available one at a time, with code that is compiled and
tested when the book is built.

This edition is the baseline. An AI assistant drafted it from public sources: the exam guide,
Anthropic's public documentation, the SDK's two books, and the author's outline. The colophon of the
book lists them.

The book is not affiliated with or endorsed by Anthropic, it is not an exam preparation guide, and it
has no exam questions in it.

## What is in it

| Path | What it is |
|---|---|
| `book` | The book in AsciiDoc, and the site built from it |
| `book/src/docs/asciidoc/chapters` | Four opening chapters, then one chapter for each domain with one section for each skill |
| `book/src/docs/asciidoc/appendices` | The blueprint map, the capabilities and their standing, revisions, building, sources |

Modules with code will sit beside `book` as sections move from sketch to available.

## Build

Java 25 and Maven 3.9.

```
mvn verify
```

renders the book into `book/target/book` and the site into `book/target/site`. The look of the HTML
comes from the released runtime, from Maven Central.

```
mvn verify -Dbook.editor-notes=false     # as published, without editor's notes
```

## How it is kept

The chapters say what holds now, and the "Revisions" appendix says when it came to hold. If you work
with an AI assistant, point it at this repository: `AGENTS.md` tells it how the book is laid out and
what its conventions are.

## License

The code is licensed under the [Eclipse Public License 2.0](LICENSE). The text and figures of the
book are licensed under the
[Creative Commons Attribution 4.0 International License](book/LICENSE). Neither license covers the
Nasdanika name or logo.
