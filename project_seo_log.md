# Podcast Alarm — SEO Change Log

A running record of SEO changes to podcastalarm.app: what changed, why, and the
GSC signal that motivated it. Newest entries at the top.

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
