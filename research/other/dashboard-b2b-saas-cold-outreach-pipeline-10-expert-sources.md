# B2B SaaS Cold Outreach Pipeline — 10 Expert Sources Dashboard (summary)

Source: condensed summary of `research/sources.md`  
Added: 2026-04-14

## What this is

A high-signal dashboard for building a **cold outreach pipeline** in B2B SaaS using **10 practitioner sources** and a repeatable collection + synthesis workflow.

## Dashboard snapshot

- **Expert sources**: 10 (practitioners, not pundits)
- **Channels covered**: 4 (YouTube · LinkedIn · Podcast · Blog)
- **Content target**: 200+ pieces (collectible via APIs)
- **Collection methods**: API · Scrape · Manual

## Collection pipeline (end-to-end)

01. **Expert curation** — manual selection by signal quality  
→ 02. **Content discovery** — channel IDs, post URLs, RSS feeds  
→ 03. **API extraction** — Supadata · YouTube Data API  
→ 04. **Normalization** — JSON schema per expert  
→ 05. **Playbook synthesis** — pattern extraction + tagging

## The 10 expert sources (codes)

- **JB** Josh Braun — anti-pitch, “giving email” model  
- **WA** Will Aitken — tactical cold email + Gap Prospecting  
- **TB** Tito Bohrt — outbound experiments + cold calling at scale  
- **JR** Jack Reamer — ultra-personalized LinkedIn + email combos  
- **JL** Jason Lemkin — buyer/CEO lens; cold email psychology  
- **CW** Chris Walker — signal-based counterpoint; what actually drives pipeline  
- **SE** Steli Efti — cadence + follow-up frameworks (Close)  
- **MM** Michael Maximoff — relevance > personalization; outreach ops + deliverability  
- **CC** Collin Cadmus — outbound systems + SDR ops; authenticity  
- **SP** Sujan Patel — deliverability + sequencing; practitioner + toolmaker (Mailshake)

## Where this lives in the repo (current)

- **Full dashboard**: `research/sources.md`
- **LinkedIn posts by expert**: `research/linkedin-posts/`
  - `josh-braun.md`, `will-aitken.md`, `tito-bohrt.md`, `jack-reamer.md`, `jason-lemkin.md`, `chris-walker.md`, `steli-efti.md`, `michael-maximoff.md`, `collin-cadmus.md`, `sujan-patel.md`
- **YouTube transcript indexes / video notes**: `research/youtube-transcripts/`
  - `josh-braun-youtube-channel-index.md`, `tito-bohrt-youtube-channel-index.md`, `saastr-youtube-channel-index.md`, `steli-efti-youtube-channel-index.md`, plus example video files

## Tooling plan (high level)

- **Supadata**: transcript extraction by video ID
- **YouTube Data API v3**: list videos + metadata inventory
- **LinkedIn**: manual capture (or tools within ToS limits)
- **Podcasts**: RSS feeds → show notes/transcripts; Whisper fallback for audio
- **Blogs**: Apify / ScrapingBee for structured extraction

## Why these 10 (selection logic)

Prioritizes **verifiable practitioner signal** (scaled outbound, built the tools, or lived buyer perspective) over generic influencer lists.

