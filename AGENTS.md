# For AI assistants

This repository is a book in AsciiDoc, "Enterprise AI in Java, Objective by Objective: The AI
Architect's Domains Through the Nasdanika SDK", and later the code its sections show. This file says
how to find your way and what the conventions are.

## What the book is

A view of two semantic domains for one stakeholder. The first domain is AI architecture: the seven
domains and thirty-nine skills of version 1.1 of Anthropic's exam guide for the Claude Certified
Architect, Professional certification. The second is the Nasdanika SDK: its released runtime and its
roadmap. Each section relates one skill to the capabilities of the SDK that serve it.

## Where things are

| You need | Look at |
|---|---|
| What the book is, and the stakeholder's concerns | `book/src/docs/asciidoc/chapters/01-a-view-for-the-ai-architect.adoc` |
| The premise: what before how | `chapters/02-enterprise.adoc` |
| The SDK on a few pages | `chapters/03-the-sdk-in-brief.adoc` |
| A skill | `chapters/05-` to `11-`, one chapter for each domain, one section for each skill, with an id that starts with `skill-` |
| Every capability named, with its standing | `appendices/b-capabilities.adoc` |
| Skills against capabilities and concerns | `appendices/a-blueprint-map.adoc` |
| When something changed | `appendices/c-revisions.adoc` |
| What a capability really is | The Nasdanika SDK Runtime book, https://runtime.sdk.nasdanika.org, and the Nasdanika SDK Roadmap book, https://roadmap.sdk.nasdanika.org. They are the authority, not this book. |

## Status

- A section is a **sketch** until it has code in this repository. A sketch shows no code.
- A section is **available** when it has a module here, compiled and tested with the book, and its
  listings are tagged regions of that module. Do not write a listing by hand.
- A capability of the SDK is named with its standing, AVAILABLE, SKETCH or PLANNED, as the SDK's own
  books give it. Do not present a planned capability as something that works.

## Conventions

- Every skill section has five lines in a horizontal list: Asks, Concerns, Have, Missing, To show.
  Keep the five, in that order.
- "Asks" is in this book's own words. Do not copy the exam guide's description of a skill. The
  section title is the skill's name as the guide gives it.
- "Concerns" uses the attributes `{c-platform}`, `{c-telemetry}` and so on, defined in `book.adoc`.
- Prose: plain, first person where the author speaks, no em or en dashes, one sentence to a line.
- The book names LangChain4j, Spring AI and Python in `chapters/04-other-ways.adoc` and does not
  compare features. Keep it so.
- Nothing from an exam, and nothing from a course that is not public, goes into this repository. The
  book has no exam questions and no practice questions.
- The book does not claim a credential for its author.
- A change of what a section says, and each move from sketch to available, gets a dated row in the
  Revisions appendix. Do not rewrite history silently.
- After changing a section's Concerns line, or adding or renaming a section, make
  `appendices/a-blueprint-map.adoc` again. Its two tables are derived from the sections.
- Java 25, JPMS, tabs for indentation, and dependencies through the runtime's bill of materials, for
  modules that come later.

## Build and check

```
mvn verify                               # the book: PDF, EPUB, HTML, and the site
mvn verify -Dbook.editor-notes=false     # as published
```

A warning from Asciidoctor fails the build: a broken cross-reference, a missing image, a missing tag.
State what you ran and what you only read. Do not claim that something works unless a test shows it.
