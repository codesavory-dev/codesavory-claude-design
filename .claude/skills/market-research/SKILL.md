---
name: market-research
description: Sourced market and competitor research on companies, products, links or a category, written to a dated markdown file with a short summary in chat. Use when the user says "market research", "competitor research", "who else does this", "thoughts on these companies", or pastes product, funding or launch links and asks how they relate to their own product.
---

# Market research

Produce research a founder can trust in a pitch or a decision. Every claim is sourced, opinions are labelled, and the output ends in what it means for the user's product.

## Inputs

- The subjects: links, company names, a category, or a question ("who else does X").
- The user's product: read the project's CLAUDE.md, README or strategy doc first so the "what it means for us" sections are concrete. If there is no project context, ask one line: "Which product should I compare this against?"
- Video links: follow the global video rule. Download with `yt-dlp` (or `uvx yt-dlp`) into the scratchpad, pull frames with `ffmpeg` and read them. Fall back to browser screenshots if that fails. Use downloads only for analysis, and never republish them.

## Method

1. **Fetch each source directly.** Use WebFetch for pages and WebSearch for funding, pricing and dates. Prefer primary sources: the company's own site, docs, pricing page, blog, changelog, filings or press release. Use news and third-party blogs only to fill gaps, and say so.
2. **Run independent lookups in parallel.** For a broad sweep (five or more companies, or a whole category), you may hand each company to a subagent with a tight brief, then verify anything surprising yourself.
3. **Record facts per subject.** Not every field applies; write "Not stated" when the source doesn't say. The fields:
   - what it is
   - who it's for
   - how it works (the rendering, model or stack, if relevant)
   - pricing, with the exact tiers and numbers
   - funding: amount, round, lead investors, date
   - team size
   - launch dates
   - distribution
   - notable customers
4. **Quote numbers exactly** with their unit and date. Never round a price or a funding figure into something the source didn't say.
5. **Label your own reading.** Anything that is your interpretation gets "(inferred)" or sits in an "Inferred" or "What it means" paragraph, never mixed into a fact bullet.
6. **When sources disagree,** give both, with links, and say which is better supported and why.
7. **Never invent** a statistic, quote, customer, price or funding round. If you can't find it, say so.

## Output file

Write one markdown file. Use the project's research or design folder if it has one (check CLAUDE.md), else `research/` at the project root, else the scratchpad. Name it for its content plus the date, for example `market-research-creative-ai-2026-10-28.md`. Never use a generic name.

Structure:

```markdown
# <Topic> market and competitor research

Date: <D Mon YYYY>. Scope: <subjects>. Every claim has a URL. "Not stated" means the source did not say. "Inferred" marks my own reading.

## 1. <Company or product>

Source: <link the user gave, and what loaded>

- What it is: ... (URL)
- Pricing: ... (URL)
- Funding: ... (URL)
- ...

What it means for <user's product> (inferred): <two to four sentences: threat, opening, or something to copy or avoid>

## N. Comparison

| Company | What it does | Price | Funding | Overlap with us |
|---|---|---|---|---|

## Risk check (if the project uses one)

For each idea the research suggests, give:

- Value (1 to 10)
- R-agent: could a coding agent just build this?
- R-model: could a generative model just output this?
- R-incumbent: who already ships it?
- a kill signal

## What to do

<3 to 6 concrete actions, ordered, each tied to a finding above>

## Sources

<every URL used, as a list>
```

## Chat reply

Keep it short.

- Link the file.
- Give 4 to 8 colour-coded points on what matters for the user's product. Use the project's severity convention if it has one (for example 🔴 threat, 🟠 watch, 🟡 note, 🟢 opening).
- Give one recommended next step.
- End with a "Sources:" list of the main URLs as markdown links.

Don't paste the whole document into chat.

## Rules

- **Writing style:**
  - No em dashes, en dashes or double hyphens anywhere, in the file or in chat. Split the sentence instead.
  - Plain, direct sentences.
  - None of "delve", "leverage" (as a verb), "robust", "seamless", "comprehensive" or "game-changer".
- **Copyrighted material:** don't reproduce long passages. Summarise and link.
- **Logged-in and paywalled sources:** never log in, pay, or bypass a paywall. Note "paywalled" and move on.
- **Simulated or synthetic feedback** (persona simulations, AI focus groups) is never evidence of demand or traction. Label it as simulated if it appears at all.
- **Committing:** if the project requires a verification step before a commit (check CLAUDE.md), run it before committing the research file. Never commit third-party images or downloaded videos.
