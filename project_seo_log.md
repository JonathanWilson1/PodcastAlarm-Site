# Podcast Alarm — SEO Change Log

A running record of SEO changes to podcastalarm.app: what changed, why, and the
GSC signal that motivated it. Newest entries at the top.

---

## 2026-09-26 — Ranking push on the 3 worst-converting high-impression pages

**Branch:** `seo-refresh/2026-09-ranking-push`

Three pages were pulling good impression volume at terrible CTR from **position
24-28** — too deep to fix with a meta rewrite. Per-page GSC query breakdowns were
checked first: all three show the *healthy* pattern (25-30 distinct queries, no
single query hoarding impressions), so this is a ranking problem, not a SERP-feature
mirage. The work is therefore content depth + intent coverage, not just metadata.

| Page | GSC signal (28d) | Diagnosis from the query data |
|------|------------------|-------------------------------|
| `/blog/best-horror-podcasts` | 729 impr, 0.96% CTR, pos 28.6 | `best horror podcast 2026` already ranks pos 9.4, but `best scary podcast(s)` (~138 impr) sits at pos 44-51 with no on-page targeting. Worse: the **paranormal page outranked this one for "best horror podcasts"** (pos 8.0 vs 44.9) — straight cannibalisation. |
| `/blog/best-celebrity-podcasts` | 674 impr, 0.30% CTR, pos 24.2 | `best celebrity podcasts 2026` ranks pos 9.7, but the whole `best interview podcasts` cluster (~80 impr) is stranded at pos 47-62. |
| `/blog/best-paranormal-podcasts` | 618 impr, 0.49% CTR, pos 24.6 | `best paranormal podcasts 2026` ranks pos 9.6; `best supernatural podcast(s)` (~100 impr) stranded at pos 40-43. |

**What changed:**

1. **De-cannibalised horror vs paranormal.** Horror is now scripted fiction, audio
   drama and anthology only; the real-encounter shows (Spooked, Uncanny, Radio
   Rental, Astonishing Legends) moved to the paranormal post. Both intros state
   their scope and link to the other.
2. **Expanded and restructured** into H2 sections named for the stranded query
   clusters — horror 10→15 shows, celebrity 10→15, paranormal 15→18.
3. **Episode-level detail: a "Start with:" starter episode on all 48 entries**,
   plus a 3-question FAQ block per post. This is the main depth play against the
   current top 10.
4. **New titles + descriptions** leading with the money query (titles 51-54 chars,
   descriptions 151-158 chars), `date-modified`, a visible "Last updated September
   2026" line, a "What's new for 2026" block, and `podcasts:` ItemList resized to
   match the new counts.
5. **App Store CTA rebuilt for conversion.** The site took 1,050 new visitors in 28
   days but only 12 `app_store_click` events (1.1%). Added
   `_includes/appStoreCta.html` — a styled card with a real button — placed above
   the fold right after the intro and repeated mid-post. It keeps a plain
   `apps.apple.com` href so the existing delegated click listener in
   `_layouts/default.html` still fires `app_store_click` and the conversion stays
   measurable.
6. **Internal links** between all three posts and the unsolved-mystery,
   psychological-thriller, conspiracy, comedy, movie and best-of-2026 lists —
   including inbound links added to five posts that had none.

**Artwork:** 19 new covers fetched via `scripts/fetch-podcast-images.py` (Listen
Notes) with zero not-found and zero wrong-match, each one eyeballed individually.
Collage cover banners regenerated for all three posts.

**Verification:** `jekyll build` clean; rendered output confirms one inline artwork
per entry (16/15/18), 48 "Start with" lines, no `/gb/` links, no missing or
undersized images, CTA CSS compiled, `app_store_click` listener intact.

**Expect no CTR movement for 4-8 weeks** while Google recrawls and re-ranks. Don't
re-flag these pages as "low CTR, needs a meta rewrite" before November 2026.

---

## 2026-08-02 — CTR harvest: meta/title rewrites on 5 high-impression pages

**Branch:** `seo-refresh/2026-08-ctr-harvest`

Five blog posts were bleeding impressions at very low CTR (~0.1–0.9%) despite
ranking. Diagnosed from GSC last-28-days query/page data. All changes are
meta/title/intro/internal-link refreshes plus artwork where entries were missing
it — no new pages, no permalink changes, so no redirects needed.

| Page | GSC signal (28d) | Change |
|------|------------------|--------|
| `/blog/best-celebrity-podcasts` | 1,569 impr, 0.89% CTR, pos 16.8. Query "celebrity interview podcasts" ranked pos 8.7 (317 impr, 0.32% CTR) but the page didn't target it. | Rewrote `<title>` to lead with **Best Celebrity Interview Podcasts (2026)** and led the meta description with "celebrity interview podcasts". Bumped `date-modified` + "Last updated" to Aug 2026. |
| `/blog/best-paranormal-podcasts` | 685 impr, 0.15% CTR, pos 21. Money query "best paranormal podcasts 2026" ranked pos 10.2 (323 impr). | Retitled to the un-parenthesised money query **Best Paranormal Podcasts 2026: 15 Ghost & UFO Shows**; led meta description with the same phrase. Added `date-modified` + "Last updated Aug 2026" freshness line. |
| `/blog/best-podcasts-to-fall-asleep-to` | 968 impr, 0.10% CTR, pos 47.5. Thematically ideal for a sleep/alarm app. | Refreshed title/meta to Aug 2026; added a strong CTA linking the App Store listing (sleep-timer angle) high in the post; added Apple Podcasts links + fetched cover art for all 7 shows (post was previously imageless, off-convention). |
| `/blog/7-best-podcasts-hosted-by-women` | 1,179 impr, 0.08% CTR, pos 53.7. | Title/meta refreshed to Aug 2026; fixed a copy-paste content bug (the "History Chicks" entry described "Science VS") with an accurate description; freshened "What's new". |
| `/blog/best-podcasts-for-road-trips` | Current winner — 1,060 impr, 21 clicks; "best road trip podcasts 2026" ranked pos 7.1. | Retitled to lead with the money query **Best Road Trip Podcasts 2026**; led meta description with it; refreshed "What's new" + `date-modified` to Aug 2026; fetched cover art for the 5 core entries that were missing it. |

**Artwork:** 12 podcast covers fetched via `scripts/fetch-podcast-images.py`
(Listen Notes) and eyeballed individually — 7 for the sleep post, 5 for road trips.

**Verification:** `bundle exec jekyll build` clean; rendered titles/descriptions/
images confirmed in `_site/`.
