# Physics ArXiv Daily Summaries

Daily blog posts explaining cutting-edge physics papers in layman's terms.

**Author:** Francesco (Theoretical Physicist)  
**Purpose:** Make frontier physics research accessible to curious people who want real understanding  
**Cadence:** Daily (Mon-Fri, typically; optional weekends)

---

## Repository Structure

```
physics-arxiv-repo/
├── README.md (this file)
├── CLOSING_PARAGRAPH.md (standard closing paragraph template)
├── drafts/
│   ├── 2026-02-22/
│   │   ├── paper.md (ArXiv link + metadata)
│   │   ├── blog-post.md (full blog post draft)
│   │   ├── twitter-thread.md (Twitter thread)
│   │   ├── reddit-post.md (Reddit post)
│   │   └── status.md (review status: PENDING / APPROVED / PUBLISHED)
│   ├── 2026-02-23/
│   └── ...
├── published/
│   ├── 2026-02-22-dark-matter-lensing.md
│   ├── 2026-02-23-higgs-discovery.md
│   └── ...
└── archive/
    └── (old summaries, organized by month)
```

---

## Workflow

### 1. **Draft Creation (Chiara, daily ~8 AM UTC)**
- Pull 2-3 interesting papers from ArXiv (astro-ph.CO, hep-th, hep-ph, gr-qc, quant-ph)
- Write blog post (800-1200 words, conversational, math-light, catchy)
- Generate Twitter thread + Reddit post
- Push to `drafts/YYYY-MM-DD/` folder
- Send Telegram notification with link

### 2. **Review & Approval (Francesco, ~9 AM UTC, 15-20 mins)**
- Review blog post draft in GitHub
- Check for accuracy, tone, clarity
- Make edits or approve as-is
- Update `status.md` to APPROVED

### 3. **Publishing (Francesco, ~9:30 AM UTC, 10-15 mins)**
- Copy blog post to Substack
- Cross-post to Medium
- Post Twitter thread
- Post to Reddit (r/physics, r/cosmology, etc.)
- Move final version to `published/` folder in GitHub
- Update `status.md` to PUBLISHED

---

## File Templates

### `paper.md`
```
# Paper Metadata

**Title:** [Paper title]
**Authors:** [First author et al.]
**ArXiv ID:** [e.g., 2405.12345]
**Category:** [e.g., astro-ph.CO]
**Date:** [Publication date]
**Link:** https://arxiv.org/abs/[ID]

## Key Concepts
- [Concept 1]
- [Concept 2]
- [Concept 3]

## Why It Matters
[1-2 sentence summary of significance]

## Difficulty Level
Easy / Medium / Hard (for reader)
```

### `blog-post.md`
```
# [Title - Catchy and Direct]

**Date:** YYYY-MM-DD

[Opening paragraph: hook + why it matters + what you'll learn]

## Background: [Key Concept 1]
[Explanation in layman's terms with analogy]

## Background: [Key Concept 2]
[Explanation in layman's terms]

## The Research
[What did they do? What did they find? How does it differ from before?]

## Why It Matters
[Real-world implications and open questions]

## Connection to the Bigger Picture
[How this relates to other areas of physics]

---

[CLOSING PARAGRAPH - use template from CLOSING_PARAGRAPH.md]
```

### `twitter-thread.md`
```
# Twitter Thread

**Thread starter (hook):**
🧵 Scientists just discovered [surprising result]. If confirmed, it changes everything we thought about [topic]. Here's what it means:

**Tweet 1:**
[Point 1 in 280 chars max, with visual if possible]

**Tweet 2:**
[Point 2]

**Tweet 3 (finale):**
[Conclusion + link to blog post]

---
Learn more: [link to Substack/Medium]
```

### `reddit-post.md`
```
# Reddit Post

**Subreddit:** r/physics (or r/cosmology, r/Futurology, etc.)
**Title:** [Title - should spark curiosity]

**Body:**
[Opening hook + 2-3 paragraphs explaining the paper]

[Link to full blog post]

---

Questions? Ask in comments!
```

### `status.md`
```
# Status Tracking

| Field | Value |
|-------|-------|
| Date | 2026-02-22 |
| Paper | [ArXiv ID] |
| Status | PENDING / APPROVED / PUBLISHED |
| Chiara Draft | ✓ Complete |
| Francesco Review | [ ] Complete |
| Substack | [ ] Published |
| Medium | [ ] Published |
| Twitter | [ ] Posted |
| Reddit | [ ] Posted |
| Notes | [Any issues, iterations, etc.] |
```

---

## Git Workflow (for Francesco)

### Review & Approve
```bash
cd physics-arxiv-repo
git pull origin main
# Open drafts/YYYY-MM-DD/ in editor
# Make edits
git add .
git commit -m "Review: approve draft for YYYY-MM-DD"
git push origin main
```

### Move to Published
```bash
# After publishing to Substack/Medium/Twitter/Reddit:
mv drafts/YYYY-MM-DD/blog-post.md published/YYYY-MM-DD-[slug].md
rm -rf drafts/YYYY-MM-DD/
git add .
git commit -m "Publish: [Date] - [Title]"
git push origin main
```

---

## Cadence

- **Mon-Fri:** Daily post (standard)
- **Sat-Sun:** Optional (post if interesting paper found, or skip)
- **Reserve drafts:** Keep 2-3 extra drafts pre-written for backup (holiday, busy day, etc.)

---

## Metrics & Feedback

Track engagement externally:
- Substack: Views, opens, signups
- Medium: Views, reads, followers
- Twitter: Impressions, engagements
- Reddit: Upvotes, comments

Update progress in this repo as a log (see `PROGRESS.md` below).

---

## Archive & Organization

**Monthly:** Move old drafts to `archive/YYYY-MM/`

**Quarterly:** Review engagement data, identify top-performing topics

---

## Questions?

- Issues with drafts? Ping Chiara in Telegram
- Need to adjust tone/style? Update `CLOSING_PARAGRAPH.md` and let me know
- Want to change cadence or structure? Edit this README

---

**Last Updated:** 2026-02-21  
**Repo Owner:** Francesco  
**Automated by:** Chiara
