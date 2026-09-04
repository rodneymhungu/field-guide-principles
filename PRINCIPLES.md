# Field guide principles

How I build single-page technical guides, and why. These rules came out of the [Agent 365 field guide](https://rodneymhungu.github.io/agent-365-guide/) in September 2026 and now apply to every guide I publish. Each page links back here. If a page and this document disagree, this document wins and the page gets fixed.

A field guide is one HTML page about one product or one problem, written for the engineer who has to make it work. It is sourced, opinionated, and honest about what is not ready. It is not a brochure, a course, or a summary of the docs.

## 1. Content

**Name the product that enforces each control, and the role that owns it.** A control plane, portal or dashboard is never described as the enforcer. Every capability is mapped to the product that actually does the work and the administrator who runs that product. If the mapping is unclear, that is the finding, and the guide says so.

**Status is data, not prose.** Whether a capability is generally available, in preview, gated behind a programme, or roadmap lives in one data object at the top of the file. Badges, the phrases in the prose, and any "what you can deploy today" table render from that object. Status is never hand-edited in a sentence. Changing one value updates the whole page.

**Every claim traces to a primary source at the point of use.** Product facts link to the vendor's documentation in the sentence that makes the claim, not in a bibliography at the end. Screenshots carry a manifest that records where each one came from, how it was cropped, and which section uses it. Secondary sources, blog posts and slide decks are named as such.

**Opinion is quarantined.** Judgement calls live in named, numbered field notes, visibly separate from the sourced facts. The footer says whose opinions they are. A reader can always tell which sentences the vendor would sign and which ones are mine.

**Order follows dependency.** Chapters run in the order the work has to happen, and the guide says why. If you cannot govern what you have not found, discovery comes first. Chapter titles read as a sequence, so the shape of the argument is visible in the table of contents.

**Verdict first, then evidence.** A section opens with the sentence that matters and follows with the proof. Tables carry a "what actually happens" column rather than a feature name. Every catalogue closes on a so-what. A list of accurate facts with no conclusion is not finished.

**Say what the source does not say.** If a vendor template leaves weeks unassigned, the guide says the weeks are unassigned. If a capability appears only in a blog post, it is labelled roadmap. If a service is not yet covered by a contractual term, the gap is stated so the reader can record it. Smoothing over a gap is a form of lying.

**End in action.** The last chapters are a handoff: a short, numbered list of moves and a table of what can be deployed today. No closing summary that restates the guide.

## 2. Writing

Plain English. Short sentences. UK spelling. Formal register without padding.

- No em dashes or en dashes. Use a comma, a colon or a full stop.
- No buzzwords. Delve, leverage, robust, seamless, unlock, landscape, empower and their relatives do not appear.
- No negative-parallel templates as a habit. "Not X, but Y" is allowed once when it is the actual argument. It is not a rhythm.
- One job per section. Sections are mutually exclusive and together cover the topic. If two sections explain the same thing, one of them goes.
- Product names in full and consistent. Status words (preview, GA, licence-dependent) are precision, not hedging, and are never cut for style.
- Interface copy, button labels and captions follow the same rules as body text. A button says where it goes, in the words of the heading it lands on.
- Every draft goes through an AI-writing review before it is published, and the author decides each flag. The review may not rewrite.

## 3. Visual identity: the routed field manual

The page should look like a working document someone carries, not a marketing site. Quiet confidence, one memorable detail, nothing that makes a sceptical reader wonder whether the substance is thin.

- **Paper and ink.** Colour tokens are named for what they are: paper, paper-2, paper-3 for surfaces; ink, ink-2, ink-3 for text; rule for hairlines. One accent colour for links and interaction, one signal colour for emphasis. Status colours (GA, preview, programme, roadmap) each have a text and a background token and are used only for status.
- **Three typefaces with three jobs.** A serif with optical sizes for display and reading, a sans for interface and body, a mono for labels, captions, sources and anything that is data. A hand-drawn face appears only inside sketches.
- **Hand-drawn sketches for concepts, screenshots for facts.** When the point is an idea (a guard at a door, three rings around a laptop), it is drawn by hand in SVG with a slight wobble. When the point is what the portal shows, it is a real screenshot with numbered callouts and a source line.
- **Diagrams are built, not pasted.** SVG authored in the file, using the page's tokens, with one moving part at most. A stepper reveals one object at a time. An animated path shows one request. If a diagram needs a legend longer than one line, it is two diagrams.
- **One interactive per concept.** A plan picker for licensing, a stepper for a token flow, hover pillars for a product map. Each interactive answers one question the reader has at that point. There is no interactive for its own sake.
- **Media never autoloads.** Video embeds are a still with a title, chapters and a play button. The page says "nothing loads until you press play" and means it.
- **Light and dark, both designed.** Tokens are redefined for dark mode. The dark page is not an inverted light page.
- **Motion is polish.** One staggered reveal, one animated route. Everything honours reduced motion.
- **Mobile scrolls, it does not shrink.** Wide tables and drawings scroll inside their own container. The page body never scrolls sideways. Sketches stay legible on a phone rather than becoming thumbnails.
- **Accessibility floor.** WCAG AA contrast, visible focus, semantic headings, every image with alt text and intrinsic dimensions, every diagram with a title and description.

## 4. Mechanics

- One HTML file. No build step, no framework, no dependency beyond fonts. Anyone can read the source and see how it works.
- The data block sits at the top of the file with a comment that explains how to update the page. The comment is written for a stranger.
- Images live in one folder with a manifest and a README listing source and crop for every file.
- Every image has width and height attributes so the layout does not shift as it loads.
- Search and a "GA only" filter are built in, because the reader's first question is usually "what can I use now".
- Published on GitHub Pages from the main branch. The repository has a README that says what the guide is, who it is for, how it is built, and links here.
- The footer names the author, the review date, the sources, and links to these principles.

## 5. Before publishing

1. Every status badge and phrase renders from the data block. Nothing is hand-set.
2. Every product claim links to a primary source in the sentence that makes it.
3. Every image has a manifest entry, alt text, and intrinsic dimensions.
4. Field notes are numbered, named, and visibly separate from sourced text.
5. Chapter titles read as a sequence in the table of contents.
6. Each section ends with a verdict, and the guide ends with actions.
7. AI-writing review run; every flag decided by the author.
8. Checked at 390px and 1440px: no horizontal overflow, no clipped SVG text, no overlaps in sketches.
9. Both scripts parse; no console errors; every local asset and internal anchor resolves.
10. Light and dark checked. Reduced motion checked.
11. README updated. Footer links here.

## Guides built on these principles

- [Agent 365 for security and compliance engineers](https://rodneymhungu.github.io/agent-365-guide/), September 2026. Field guide 01.
