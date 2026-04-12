# Blog Content Strategy

**Last updated:** 2026-04-12

## What Works

The winning blog pattern for podcastalarm.app is **"Best [genre] Podcasts 2026"** list posts. Posts that perform well share these traits:

1. **"2026" in the title** — captures seasonal search intent
2. **Mid-size genre niche** — niche enough to avoid Google SERP features eating clicks, broad enough for volume
3. **Distributed query spread** — traffic comes from many query variations, not one dominant term
4. **Position 1-3 on the "2026" variant** — low-competition queries where we rank easily

### Top Performers (as of April 2026)

| Post | Clicks/28d | Real Impressions | CTR | Healthy? |
|------|-----------|-----------------|-----|----------|
| True crime | 164 | 10,779 | 1.5% | Yes — many "2026" variations |
| UK podcasts (top 100) | 64 | 1,563 | 4.1% | Yes — broad UK query spread |
| Investigative | 54 | 1,329 | 4.1% | Yes — top queries 8-18% CTR |
| Documentary | 16 | 485 | 3.3% | Yes — smaller niche |
| Mystery | 12 | 372 | 3.2% | Yes — "2026" queries doing well |
| Fiction | 11 | 193 | 5.7% | Yes — best CTR, tiny but growing |
| Short podcasts | 10 | 248 | 4.0% | Yes — interesting long-tail |

## What Doesn't Work

### Ghost Queries

Some pages show massive impression counts but near-zero clicks. This is caused by a single high-volume query where Google's SERP features (AI overviews, carousels, featured snippets) eat all the clicks. Meta title/description rewrites will NOT fix these.

**How to detect:** Run `get_search_by_page_query` in GSC. If 80%+ of impressions come from 1-2 queries with 0 clicks, it's a ghost query page.

| Post | Ghost Query | Impressions | Clicks | Real Traffic |
|------|------------|-------------|--------|-------------|
| Celebrity | "best interview podcasts with celebrities" | 48,263 | 0 | ~600 imp |
| Science | "best science podcasts for curious minds" | 21,856 | 1 | ~2,500 imp |

**Action:** Don't waste time optimising these. The page-level CTR looks terrible but there's nothing to fix.

### Broad Topics

Topics that are too broad (celebrity, science) trigger Google's own SERP features and content farm competition. Stick to mid-size niches.

### CTR Expectations (Realistic, 2025+)

Don't use the classic "position 1 = 30% CTR" figures. With AI overviews and SERP features:

| Position | Realistic CTR |
|----------|--------------|
| 1 | 8-15% |
| 2 | 5-8% |
| 3 | 3-5% |
| 4 | 2-4% |
| 5 | 1.5-3% |
| 6-10 | 0.5-1.5% |

For "best X" listicle queries, expect even lower due to featured snippets.

## Meta Title/Description Lessons

### What helped
- Adding "2026" to titles captures seasonal intent and new query clusters
- Name-dropping popular podcasts (Serial, Crime Junkie) in descriptions may improve CTR

### What hurt
- Science post: changing "That Will Blow Your Mind" to "for Curious Minds (2026)" caused 90% click drop. Emotional titles outperform generic ones.
- Reverted to original on 2026-04-12.

### Rules
- Emotional/curiosity hooks beat descriptive titles
- Include 2-3 podcast names in descriptions
- Never mention "Podcast Alarm" in meta — searchers don't know the brand
- Titles under 60 chars, descriptions 150-160 chars
- Always check query breakdown before rewriting — don't optimise ghost query pages

## Next Batch — Content Ideas

Based on spin-offs from winners + gaps in coverage. Prioritised by evidence.

### Batch 2 — Next posts to write

New genre posts (Approach B) plus select spin-offs and a timely space post. No tiered rollout — write all of these.

| # | Topic | Rationale |
|---|-------|-----------|
| 1 | Best Cold Case Podcasts 2026 | Spin-off — queries already on true crime + mystery pages |
| 2 | Best Paranormal Podcasts 2026 | Spin-off — 69 impressions already on horror page |
| 3 | Best Storytelling/Narrative Podcasts 2026 | Spin-off — queries on fiction page |
| 4 | Best Conspiracy Podcasts 2026 | New genre — adjacent to true crime audience, niche enough |
| 5 | Best Political Podcasts 2026 | New genre — high volume, seasonal |
| 6 | Best Psychological Thriller Podcasts 2026 | New genre — true crime/fiction crossover |
| 7 | Best Space & Astronomy Podcasts 2026 | Timely — Artemis program just happened, search interest spike |
| 8 | Best War & Military History Podcasts 2026 | New genre — sub-niche of history |
| 9 | Best British Comedy Podcasts 2026 | New genre — UK traffic is strong, narrows broad "comedy" |
| 10 | Best Serial Killer Podcasts 2026 | Spin-off — huge search interest from true crime |
| 11 | Best Unsolved Mystery Podcasts 2026 | Spin-off — tighter niche from mystery |
| 12 | Best Relationship Podcasts 2026 | New genre — gap in coverage, distinct audience |
| 13 | Best Nature & Wildlife Podcasts 2026 | New genre — pairs with space/science angle |
| 14 | Best Productivity Podcasts 2026 | New genre — adjacent to self-improvement |
| 15 | Best Geopolitics Podcasts 2026 | Timely — Iran/Trump situation driving search interest |
| 16 | Best Real Estate Podcasts 2026 | New genre — high commercial intent |
| 17 | Best Survival & Outdoor Podcasts 2026 | New genre — niche enthusiast audience |
| 18 | Best Music History Podcasts 2026 | New genre — narrower than broad "music" |
| 19 | Best Legal/Law Podcasts 2026 | New genre — professional audience |
| 20 | Best Investing Podcasts 2026 | New genre — high commercial intent |

### Process

Use the podcast-blog-seo skill for production workflow (image fetching, formatting, verification). After all posts are live, check GSC after 3-4 weeks to evaluate.

## Previous Batches

- **Batch 1 (March 2026):** 25 posts. Spec at `docs/superpowers/specs/2026-03-13-blog-content-plan-design.md`. All 25 published. Took total from 28 to 74 posts (some additional posts were added outside the batch).
