# Physics ArXiv Daily Blog

Daily breakdowns of cutting-edge physics papers. Layman's language, catchy explanations, connected to core concepts.

**Author:** Francesco (Theoretical Physicist, 12+ years research)  
**Schedule:** Daily at 5 AM UTC  
**Output:** Substack + Medium + Twitter + Reddit

---

## Repository Structure

```
physics-arxiv-daily/
├── README.md                          # This file
├── CLOSING_PARAGRAPH.md               # Template footer for all blog posts
├── PROGRESS.md                        # Metrics & engagement tracking
│
├── drafts/
│   ├── YYYY-MM-DD/                   # Daily draft papers (pre-publication)
│   │   ├── paper-option-1.md         # ArXiv paper metadata + abstract
│   │   ├── paper-option-2.md
│   │   ├── paper-option-3.md
│   │   ├── SUMMARY.md                # Quick overview of all 3 options
│   │   └── SELECT_PAPER.md           # Selection workflow
│   │
│   └── 2026-03-04/
│       ├── paper-option-1.md
│       ├── paper-option-2.md
│       ├── paper-option-3.md
│       ├── SUMMARY.md
│       └── SELECT_PAPER.md
│
├── published/
│   ├── 2026-02-24-dark-matter-evidence.md      # Full blog post (after publication)
│   ├── 2026-02-25-gravitational-waves.md
│   └── ...
│
└── archive/
    └── 2026-02/                      # Monthly archives (deprecated drafts)
```

---

## Workflow

### 1. **Daily Paper Selection (5 AM UTC)**
- **What:** Automated cron job fetches 2-3 interesting ArXiv papers
- **Where:** Papers land in `drafts/YYYY-MM-DD/`
- **Files created:**
  - `paper-option-{1,2,3}.md` — metadata, authors, abstract, link
  - `SUMMARY.md` — quick overview of all 3
  - `SELECT_PAPER.md` — selection form

### 2. **Your Review (Morning, ~15 mins)**
- Read the 3 options in GitHub
- Pick your favorite
- Reply in Telegram: "option-1" (or 2, or 3)

### 3. **Blog Post Generation (After your pick)**
- I write full blog post (800-1200 words)
- Generate Twitter thread + Reddit post
- Push to `drafts/YYYY-MM-DD/blog-post.md`
- Send you Telegram link for final review

### 4. **Publishing (Your call, ~15 mins)**
- You review blog post
- Copy-paste to Substack
- Cross-post to Medium
- Share Twitter thread
- Post to Reddit (r/physics, r/cosmology, etc.)
- Move post to `published/YYYY-MM-DD-{slug}.md`

### 5. **Archive (Monthly)**
- At month-end, move completed `drafts/` to `archive/YYYY-MM/`
- Keep active month in `drafts/`

---

## File Templates

### `paper-option-X.md`
```
# Paper Metadata

**Title:** [Paper title]
**Authors:** [First author et al.]
**ArXiv ID:** [2603.02177]
**Category:** [astro-ph.CO]
**Date:** [2026-03-04]
**Link:** https://arxiv.org/abs/2603.02177

## Abstract
[Full abstract from ArXiv]

## Key Concepts
- [Concept 1]
- [Concept 2]
- [Concept 3]

## Why It Matters
[Brief significance]

## Difficulty Level
Easy / Medium / Hard
```

### `SUMMARY.md`
```
# Daily ArXiv Summary — YYYY-MM-DD

**Status:** ✅ Papers fetched and ready for review
**Generated at:** [timestamp]

## Papers Found (3 Options)

### Option 1: [Title]
- ArXiv ID: [ID]
- Category: [Category]
- Key insight: [One sentence]
- Difficulty: [Level]

[Repeat for options 2 and 3]

## Next Steps
1. Review all three papers above
2. Pick your favorite and reply in Telegram: "option-1" (or 2, or 3)
3. I'll generate full blog post + Twitter + Reddit
4. You review and publish

## Publishing Timeline
- 5 AM UTC: New papers fetched
- Morning (your timezone): You review + pick
- Afternoon: I write blog post
- Evening: You review + publish
```

### `blog-post.md` (After you select)
```
# [Catchy Title - Direct and Intriguing]

[Opening paragraph: Hook + why it matters + what you'll learn]

## Background: [Key Concept 1]
[Explanation in layman's terms with analogy]

## Background: [Key Concept 2]
[Explanation]

## The Research
[What they did, what they found, how it differs from before]

## Why It Matters
[Real-world implications and open questions]

## Connection to the Bigger Picture
[How this relates to other physics]

---

[CLOSING PARAGRAPH — use template from CLOSING_PARAGRAPH.md]
```

---

## Metrics & Tracking

Track in `PROGRESS.md`:
- **Daily:** Views, email signups, engagement per platform
- **Weekly:** Aggregated metrics, top-performing topics
- **Monthly:** Trends, audience growth, key signals

---

## Git Workflow (For You)

### Review & Pick Paper
```bash
cd physics-arxiv-repo
git pull origin main
# Read drafts/YYYY-MM-DD/SUMMARY.md
# Reply in Telegram: "option-X"
```

### After Blog Post Is Written
```bash
# Review draft
git pull origin main
# Read drafts/YYYY-MM-DD/blog-post.md
# Make edits if needed
git add .
git commit -m "Review: blog post for YYYY-MM-DD approved"
git push origin main
```

### After Publishing
```bash
# Move to published + archive
mv drafts/YYYY-MM-DD/blog-post.md published/YYYY-MM-DD-{slug}.md
git add .
git commit -m "Publish: YYYY-MM-DD - [Title]"
git push origin main
```

---

## Monthly Cleanup

**End of month:**
```bash
# Archive old drafts
mkdir -p archive/YYYY-MM
mv drafts/YYYY-MM-* archive/YYYY-MM/
git add .
git commit -m "Archive: YYYY-MM drafts"
git push origin main
```

---

## Publishing Checklist

Before copying to Substack/Medium/Twitter:

- [ ] Blog post is clear and accessible (no jargon without explanation)
- [ ] At least 1 analogy per concept
- [ ] Links to related concepts embedded
- [ ] Closing paragraph included
- [ ] Twitter thread drafted (5-7 tweets max)
- [ ] Reddit post drafted (platform-specific subreddit)
- [ ] All links are working (ArXiv, related concepts, etc.)

---

## Questions?

- Issues with the workflow? Ping in Telegram
- Need to adjust structure? Edit this README
- Want to change publishing times or platforms? Update schedule above

---

**Repo Owner:** Francesco  
**Automated by:** Chiara (daily paper fetch + blog generation)  
**Last Updated:** 2026-03-04
