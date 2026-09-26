# Search Queries for Job Scraper

<!-- SETUP: Customize these queries based on your skills, target roles, and location -->

## Installed portal CLIs (primary for `/scrape`)

`/scrape` discovers every portal skill under `.agents/skills/*/SKILL.md` and runs its CLI first. Shipped country-agnostic CLIs include `linkedin-search` and `freehire-search`; Danish demos and any skill you add with `/add-portal` are included the same way. You do **not** need a matching `site:` line below for those CLIs to run.

The `site:` query templates in this file are the **WebSearch fallback** — for portals without a CLI, company career pages, or when a CLI fails.

**Language scope:** write every query category in every language listed in your CLAUDE.md Languages table (typically 1-2, sometimes more). A posting requiring a language you have *not* declared, as a job condition, is excluded before scoring; a posting requiring a *higher level* than you declared in a language you *do* work in is flagged for your own judgment, not excluded — see `04-job-evaluation.md`'s Language Gate, the single source of truth for this rule. Translate each category's keywords rather than machine-translating word-for-word (e.g. "Frontend Developer" -> "Desarrollador Frontend", not a literal word-for-word translation) if you work in more than one language.

## Search Sites

Primary (your market's job boards):
- **linkedin.com/jobs** - LinkedIn job listings; also covered by `linkedin-search` CLI
- **github.com/jobs** - GitHub job board (tech-heavy)
- **wellfound.com** - Startup jobs (good for early-stage tech roles)
- **ycombinator.com/jobs** - Y Combinator startup jobs

Secondary (company career pages via Google):
- Direct Google searches with `site:` filters for target tech companies

## Query Categories

Queries are grouped by priority. Write **each category in every language from your Languages table** (see Language scope above). Combine each query with your location terms (e.g. your city, region, or metro area) where the site supports it.

**Organize by function, not job title.** The same underlying work carries different titles across companies and markets (a "Data Scientist" role at one employer may be posted as "Insights Analyst" or "Data Consultant" at another). Name each priority category after the function it covers, and list several plausible job titles as query variants within that category rather than betting an entire priority tier on one exact title string.

### Priority 1: Frontend & Full-Stack Development

These match your strongest and most desired career direction (React, TypeScript, Node.js).

```
site:linkedin.com/jobs "Frontend Developer" remote
site:linkedin.com/jobs "Full-Stack Developer" remote React
site:linkedin.com/jobs "Senior Frontend Engineer" React TypeScript
site:linkedin.com/jobs "Full-Stack Engineer" Node.js PostgreSQL
site:wellfound.com "Frontend Developer" remote
site:wellfound.com "Full-Stack Engineer" React
```

### Priority 2: AI/LLM Integration & Generative AI

These match your growing expertise in Claude and OpenAI integrations.

```
site:linkedin.com/jobs "AI Integration" engineer remote
site:linkedin.com/jobs "LLM" engineer remote TypeScript
site:linkedin.com/jobs "Generative AI" developer
site:linkedin.com/jobs "Claude API" OR "OpenAI API"
site:wellfound.com "AI Engineer" remote
site:github.com/jobs "AI" React Node.js
```

### Priority 3: Citizen-Facing & Government Services

Adjacent roles matching your govtech/public sector experience.

```
site:linkedin.com/jobs "civic tech" OR "govtech" developer
site:linkedin.com/jobs "citizen-facing" platform engineer
site:linkedin.com/jobs "government" digital services React
site:linkedin.com/jobs "public sector" technology remote
```

### Priority 4: Broader Technical & Startup Focus

Wider net for general senior/technical roles in high-growth companies.

```
site:linkedin.com/jobs "Senior Engineer" React remote
site:linkedin.com/jobs "TypeScript" developer remote
site:wellfound.com "Engineer" remote funded
site:ycombinator.com/jobs "engineer" remote React
site:linkedin.com/jobs "technical architect" remote
```

## Location Filter

When evaluating results, verify job location matches remote work requirement:
- **Ideal:** Fully remote, anywhere
- **Acceptable:** Remote-first/remote-friendly with occasional office
- **Borderline:** Remote but requires monthly/quarterly on-site in specific timezone (EST/CST)
- **Too far:** Requires daily commute or strict on-site (Dominican Republic only)

## Language Filter

Your working languages and levels are in CLAUDE.md's Languages table. When filtering scraped results, apply `04-job-evaluation.md`'s Language Gate: a posting requiring a language you haven't declared at all is excluded; a posting requiring a higher level than you declared in a language you do work in is not excluded, flag it clearly instead (see `job-scraper/SKILL.md`'s Step 3 "Quick Fit Assessment" for how the flag surfaces in `/scrape` output). Postings simply *written* in a language you don't work in, that don't require it on the job, are fine.

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus. For example:
- "/scrape [focus_area]" -> relevant category queries + custom focus-specific queries
