# B2B SaaS Cold Outreach Pipeline — 10 Expert Sources Dashboard

Cold outreach pipeline — B2B SaaS  
10 high-signal expert sources · content collection architecture · repository structure

---

## Dashboard summary

- **Expert sources**: 10 (practitioners, not pundits)
- **Channels covered**: 4 (YouTube · LinkedIn · Podcast · Blog)
- **Content pieces**: 200+ (collectible via APIs)
- **Collection method**: 3 (API · Scrape · Manual)

---

## Collection pipeline

01. **Expert curation** — Manual selection by signal quality  
→ 02. **Content discovery** — Channel IDs, post URLs, RSS feeds  
→ 03. **API extraction** — Supadata · YouTube Data API  
→ 04. **Normalization** — JSON schema per expert  
→ 05. **Playbook synthesis** — Pattern extraction + tagging

---

## 10 expert sources — ranked by practitioner signal

### JB — Josh Braun
- **Role**: Founder, Sales DNA · “Badass B2B Growth” podcast
- **Why high-signal**: The anti-pitch philosopher of cold outreach. Built a career teaching reps to lead with insight, not asks. His “giving” email model (teach before you pitch) is one of the most referenced cold email frameworks in SaaS.
- **Topics**: cold email · podcast · LinkedIn
- **Channels**: Podcast · LinkedIn · `joshbraun.com`
- **Signal**: Practitioner · Originality

### WA — Will Aitken
- **Role**: Founder, Sales Feed · Author, *Gap Prospecting*
- **Why high-signal**: One of the most tactically sharp voices on cold email (2025). Known for deconstructing what makes prospects ignore or engage; co-authored *Gap Prospecting* with Keenan. Hosts a daily B2B sales show.
- **Topics**: cold email · YouTube · LinkedIn
- **Channels**: YouTube · LinkedIn · `willaitken.com`
- **Signal**: Practitioner · Originality

### TB — Tito Bohrt
- **Role**: Founder, AltiSales · “The Sales Mad Scientist”
- **Why high-signal**: SDR lab at scale: teams have run 1M+ cold calls, achieving a 55% connect-to-meeting rate. One of the only people publishing reproducible outbound experiments with real numbers. Category creator in GTM playbook development.
- **Topics**: cold calling · cold email · GTM playbook
- **Channels**: YouTube · LinkedIn · podcast guest
- **Signal**: Practitioner · Originality

### JR — Jack Reamer
- **Role**: CEO, SalesBread · Co-host, Cold Outreach Podcast
- **Why high-signal**: Delivers 1 qualified lead per day via ultra-personalized LinkedIn + email combos. 14 years of B2B outreach; every message built around specific prospect context. Real teardowns of live campaigns on his podcast.
- **Topics**: LinkedIn · cold email · podcast
- **Channels**: Cold Outreach Podcast · LinkedIn · `salesbread.com`
- **Signal**: Practitioner · Originality

### JL — Jason Lemkin
- **Role**: Founder, SaaStr · 2× Founder · SaaStr Fund GP
- **Why high-signal**: The CEO’s lens on cold outreach—what actually works on decision-makers, from the buyer’s chair. His LinkedIn posts on cold email psychology (subject lines, first lines) are ruthlessly practical from lived experience as a $100M+ ARR founder.
- **Topics**: founder · GTM · LinkedIn · SaaStr podcast
- **Channels**: SaaStr Podcast · LinkedIn · YouTube
- **Signal**: Practitioner · Originality

### CW — Chris Walker
- **Role**: Founder, Refine Labs · “State of Demand Gen” podcast
- **Why high-signal**: The counterpoint voice: built a demand-gen agency that challenges cold outreach assumptions with data. His analysis of what signals actually drive pipeline—buyer intent vs. spray-and-pray—is essential context for any outbound playbook.
- **Topics**: demand gen · signal-based · podcast
- **Channels**: State of Demand Gen · LinkedIn · YouTube
- **Signal**: Practitioner · Originality

### SE — Steli Efti
- **Role**: CEO, Close CRM · Author, “The Ultimate Startup Guide to Outbound Sales”
- **Why high-signal**: Built Close.io on the back of brutal outbound. His follow-up frameworks and “always be closing” sequences are field-tested across thousands of SaaS startups. Publishes some of the most granular breakdowns of sales cadence online.
- **Topics**: cadence · follow-up · YouTube
- **Channels**: YouTube · Podcast · `close.com/blog`
- **Signal**: Practitioner · Originality

### MM — Michael Maximoff
- **Role**: Co-founder, Belkins · Guest, Marketing Spark Podcast
- **Why high-signal**: Scaled Belkins into a global cold outreach powerhouse. His thesis—relevance beats personalization—is a useful reframe for teams over-indexing on {first_name} tactics. Created $244M in pipeline for a single client.
- **Topics**: cold email · AI outreach · agency ops
- **Channels**: Podcast guest · LinkedIn · `belkins.io/blog`
- **Signal**: Practitioner · Originality

### CC — Collin Cadmus
- **Role**: Revenue Coach · Advisor · Podcast host
- **Why high-signal**: Helped 300+ B2B sales reps generate $100M+ in recurring revenue. Specializes in outbound systems for scaling from founder-led to team-led sales—the exact gap many B2B SaaS companies fail to cross. Detailed LinkedIn content on sequences and SDR ops.
- **Topics**: outbound systems · SDR ops · LinkedIn
- **Channels**: Podcast · LinkedIn · Blog
- **Signal**: Practitioner · Originality

### SP — Sujan Patel
- **Role**: Co-founder, Mailshake · Growth marketer
- **Why high-signal**: Built the tool tens of thousands of SDRs use daily—then documented every playbook he ran to grow it. Uniquely positioned as both toolmaker and practitioner. Content spans deliverability, sequence architecture, and multichannel plays at scale.
- **Topics**: deliverability · automation · YouTube
- **Channels**: YouTube · LinkedIn · `mailshake.com/blog`
- **Signal**: Practitioner · Originality

---

## Content collection — API & tooling plan

### Supadata API
YouTube transcript extraction. Pass video ID, get full timestamped transcript. Works without official API quota limits for most use cases.  
Cost: free tier

### YouTube Data API v3
Channel videos list, metadata, view counts, publish dates. 10,000 units/day free. Use to build video inventory before fetching transcripts.  
Cost: free (Google)

### LinkedIn (manual)
No public scraping API. Best approach: browser export of creator posts, or use PhantomBuster (paid) for automated collection within ToS limits.  
Cost: manual / tool

### RSS / Podcast feeds
All podcasts expose RSS. Pull episode descriptions, show notes, and transcripts (if available) via feedparser. Zero cost, high reliability.  
Cost: free

### Whisper (OpenAI)
Transcribe podcast audio when show notes lack transcripts. Download MP3 from RSS enclosure URL, run through Whisper API. ~ $0.006/min.  
Cost: low cost

### Apify / ScrapingBee
For blog content (`joshbraun.com`, `mailshake.com/blog`, etc.). Structured web scraper with JS rendering. Free tiers sufficient for ~200 pages.  
Cost: free tier

---

## Repository structure (target)

```text
cold-outreach-pipeline-b2b-saas/
  ├── README.md ← expert rationale, scoring criteria, collection log
  ├── experts/
  │   ├── josh-braun/
  │   │   ├── profile.json ← name, channels, signal score, why selected
  │   │   ├── linkedin_posts.json ← post text, date, engagement
  │   │   ├── youtube_transcripts/ ← one .txt per video
  │   │   └── podcast_episodes.json ← title, date, show notes, transcript
  │   └── ... (×10 experts, same structure)
  ├── scripts/
  │   ├── fetch_youtube.py ← YouTube Data API + Supadata transcripts
  │   ├── fetch_podcasts.py ← RSS feed parser + Whisper fallback
  │   ├── fetch_blogs.py ← Apify/ScrapingBee wrapper
  │   └── normalize.py ← unified JSON schema enforcer
  ├── synthesis/
  │   ├── themes.md ← cross-expert pattern extraction
  │   ├── frameworks.md ← named models (giving email, gap prospecting…)
  │   └── playbook_draft.md ← living outreach playbook
  └── data/
      └── master_index.json ← all content indexed, tagged, searchable
```

---

## Why these 10 and not the top Google results

Every expert on this list has either run real outbound campaigns at scale (example: Tito Bohrt: 1M+ calls), built the product SDRs use (example: Sujan Patel: Mailshake), or consistently receives cold emails themselves and documents what works from the buyer side (example: Jason Lemkin). Generic “top 20 cold email influencers” lists recycle the same faces who write about outreach—not those who do it. The selection prioritizes verifiable practitioner signal: named client results, reproducible frameworks, and content grounded in live campaigns rather than theory.

---

## Correction Plane

01. **Expert curation** — Manual selection by signal quality  
→ 02. **Content discovery** — Channel IDs, post URLs, RSS feeds  
→ 03. **API extraction** — Supadata · YouTube Data API  
→ 04. **Normalization** — JSON schema per expert  
→ 05. **Playbook synthesis** — Pattern extraction + tagging
