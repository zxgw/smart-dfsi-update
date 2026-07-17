# Smart DFSI Update

**AI-Built Interactive App for Sales Account Data Governance**

> Designed and delivered a production-grade data collection platform serving users across teams — built through AI-assisted development in 3 days.

---

## Overview

During Annual Planning at AWS, every customer account needs its investment tier re-evaluated based on up-to-date financial data. Sales Ops is responsible for collecting this from sales representatives across regional teams — covering thousands of accounts.

I designed and delivered an interactive web application that replaced this entire workflow — with no prior coding or software development experience. The app was built through iterative conversations with generative AI over 3 days.

---

## Demo

🎬 [Watch the 3-minute demo video](./demo/video.mp4)

---

## Key Features

### For Sales Representatives (BDs)
- Log in and immediately see their assigned accounts with current system values as reference
- Update Turnover and TAS data directly in-app with justification fields
- Search and add unlisted accounts from a pre-loaded master list (no Ops bottleneck)
- Clear instructions embedded in the interface explaining business rules

### For Managers
- Dedicated view to review and sign off on their team's submissions
- Before/after comparison for every data point changed
- Track exactly who has submitted and who hasn't
- Deep dive into individual team or account-level details

### For Sales Ops
- Real-time aggregated dashboard — total submissions, delta summaries, progress by team
- Automated anomaly flagging (e.g., TAS > Turnover triggers a visual alert)
- One-click export of all submissions for reporting
- Full audit trail of every change made

### Team-Specific Adaptations
Different teams have different data situations. Rather than forcing a one-size-fits-all approach:
- **Team A**: Can self-service add accounts not in the default list, matching against a pre-loaded master table
- **Team B**: Sees system-flagged exceptions with annotated reasons, choosing to update or acknowledge
- **Team C**: Views non-exception accounts separately, with clear notes on what proceeds automatically

---

## Architecture

```
┌─────────────────────────────────────────────────────┐
│                   QuickSight App                     │
├─────────────┬──────────────┬────────────────────────┤
│  BD View    │ Manager View │     Ops Dashboard      │
│  (Input)    │  (Review)    │    (Aggregate)         │
├─────────────┴──────────────┴────────────────────────┤
│              Role-Based Access Control               │
├─────────────────────────────────────────────────────┤
│         Data Layer (System Records + BD Input)       │
└─────────────────────────────────────────────────────┘
```

**Permission Model:** Each user sees only their relevant scope — BDs see their accounts, Managers see their team, Ops sees everything. All controlled through a single unified app.

---

## Results

| Metric | Before | After |
|--------|--------|-------|
| Collection cycle time | 2+ weeks | 3 days |
| Version conflicts | Frequent | Zero |
| Real-time visibility | None | Full |
| Manual consolidation | Hours per cycle | Automated |
| Active users | — | 68 |
| Accounts served | — | 3,189 |

---

## AI-Assisted Development Process

This project was built entirely through conversational AI — no traditional coding involved.

**How I used AI at each stage:**

| Phase | What AI Did |
|-------|-------------|
| Requirements | Helped me break down the business problem into data model and user flows |
| Design | Iterated on permission architecture, input validation rules, and UX layout through dialogue |
| Implementation | Generated the application logic, formulas, and configurations based on my descriptions |
| Edge Cases | Identified and solved scenarios I hadn't considered (e.g., "what happens when a BD needs an account not in the list?") |
| Testing | Helped me reason through anomaly detection logic and verify business rules |
| Presentation | Generated the slide deck (Kiro) and video voiceover narration (Amazon Polly) |

**Key insight:** AI wasn't just a code generator — it was a design partner. The most valuable interactions were structuring complex multi-stakeholder requirements into clean architecture decisions, and rapidly iterating on edge-case handling that would normally take weeks of development cycles.

---

## Tech Stack

- **Application Platform:** Amazon QuickSight (App feature)
- **AI Development Partner:** Amazon Q (generative AI assistant)
- **Presentation:** Kiro (AI slide generation)
- **Narration:** Amazon Polly (Neural TTS, SSML)
- **Data Source:** System firmographic records (Turnover, TAS, territory mappings)

---

## What I Learned

1. **AI accelerates the full product lifecycle.** The hardest parts of this project were design decisions — permission models, team-specific logic, validation rules. AI enabled rapid exploration of architectural tradeoffs and immediate prototyping.

2. **Anticipate edge cases upfront.** When I imported a new data source, previously entered BD data disappeared. Working with AI requires being explicit about constraints and invariants, not just desired features.

3. **Build for different users, not just one workflow.** The team-specific features were the most impactful part — and the most challenging to design. A generic tool wouldn't have achieved the same adoption.

4. **Ship fast, iterate based on feedback.** Three days, multiple versions. Each version was tested by real users who told me what was confusing or missing. AI made the iteration loop fast enough to respond same-day.

---

## About Me

**Jiaqian Geng**
Sales Operations Analyst | AWS Global Commerce & Revenue (GCR)

- Built production-grade internal tools using AI-assisted development
- Experienced in cross-team data governance, pipeline management, and sales operations
- Skilled at leveraging generative AI for rapid prototyping, system design, and end-to-end project delivery

📧 gjiaqian@amazon.com
🔗 [LinkedIn](https://linkedin.com/in/yourprofile)

---

## License

This repository contains project documentation and desensitized materials only. No proprietary data, customer information, or internal system access is included.
````
