
# ProblemFinder v1.1

Evidence-first problem discovery tool.
Sources:
- Hacker News (live, no keys)
- Reddit search by keyword + subreddit (via Cloudflare Worker)
- Paste / CSV imports
- Google Trends velocity (via same Worker)

No API keys required.

---

## QUICK START

### 1. Deploy the Worker (required for Reddit + Trends)

```bash
npm install -g wrangler
cd worker
wrangler login
wrangler deploy
```

Copy the Worker URL (example):
https://problemfinder-worker.yourname.workers.dev

---

### 2. Deploy the Site (Cloudflare Pages)

Upload the `site/` folder to a GitHub repo.

Cloudflare Pages settings:
- Framework preset: None
- Build command: (empty)
- Output directory: site

---

### 3. First Run

1. Open the site URL
2. Go to the app
3. Paste your Worker URL into **Trends proxy URL**
4. Enable **Reddit search**
5. Enter a keyword + optional subreddit
6. Run scan

---

## WHAT v1.1 ADDS

- Reddit keyword + subreddit search
- Reddit comment extraction
- Shared Worker for Reddit + Trends
- Monthly briefs stored locally
- Markdown export

---

## NO API KEYS

This version uses:
- Public APIs
- Public JSON endpoints
- User-provided inputs

LLMs are optional and not required for v1.

---

## STRUCTURE

/worker  -> Cloudflare Worker (Reddit + Trends)
/site    -> Static PWA frontend

---

## NEXT

- LLM idea generation (BYO key)
- Saved Reddit profiles
- Paid tiers & licensing

