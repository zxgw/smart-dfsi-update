# Smart Tier Update

**AI-Built Interactive App for Sales Account Data Governance**

> Designed and delivered a production-grade data collection platform serving 60+ users across 8 teams — built through AI-assisted development in 3 days.

---

## Overview

At a global tech company, every customer account's investment tier needs periodic re-evaluation based on up-to-date financial metrics. The operations team is responsible for collecting these updates from sales representatives across multiple regional teams.

The previous workflow was entirely manual: download account lists → split into spreadsheets by team → email to reps → chase non-responders → manually consolidate → repeat. This took 2+ weeks per cycle, with constant version conflicts, no audit trail, and zero real-time visibility for leadership.

I designed and delivered an interactive web application that replaced this entire workflow. The app was built through iterative conversations with generative AI over 3 days.

---

## Demo

🎬 [Watch the 3-minute demo video](./demo_video.mp4.mp4)

---

## Key Features

### For Sales Representatives
- Log in and immediately see assigned accounts with current system values as reference
- Update financial metrics directly in-app with justification fields
- Search and add unlisted accounts from a pre-loaded master list (no Ops bottleneck)
- Clear instructions embedded in the interface explaining business rules

### For Managers
- Dedicated view to review and sign off on their team's submissions
- Before/after comparison for every data point changed
- Track exactly who has submitted and who hasn't
- Deep dive into individual team or account-level details

### For Operations
- Real-time aggregated dashboard — total submissions, delta summaries, progress by team
- Automated anomaly flagging (e.g., logically inconsistent inputs trigger visual alerts)
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
│                  Interactive App                     │
├─────────────┬──────────────┬────────────────────────┤
│  Rep View   │ Manager View │     Ops Dashboard      │
│  (Input)    │  (Review)    │    (Aggregate)         │
├─────────────┴──────────────┴────────────────────────┤
│              Role-Based Access Control               │
├─────────────────────────────────────────────────────┤
│         Data Layer (System Records + User Input)     │
└─────────────────────────────────────────────────────┘
```

**Permission Model:** Each user sees only their relevant scope — reps see their accounts, managers see their team, Ops sees everything. All controlled through a single unified app.

---

## Results

| Metric | Before | After |
|--------|--------|-------|
| Collection cycle time | 2+ weeks | 3 days |
| Version conflicts | Frequent | Zero |
| Real-time visibility | None | Full |
| Manual consolidation | Hours per cycle | Automated |
| Active users | — | 60+ |
| Accounts served | — | Thousands |

---

## AI-Assisted Development Process

This project was built entirely through conversational AI — leveraging generative AI as both a design partner and implementation tool.

**How I used AI at each stage:**

| Phase | What AI Did |
|-------|-------------|
| Requirements | Broke down the business problem into data model and user flows |
| Design | Iterated on permission architecture, input validation rules, and UX layout through dialogue |
| Implementation | Generated the application logic, formulas, and configurations based on my descriptions |
| Edge Cases | Identified and solved scenarios I hadn't considered (e.g., "what happens when a rep needs an account not in the list?") |
| Testing | Helped reason through anomaly detection logic and verify business rules |
| Presentation | Generated the slide deck and video voiceover narration via AI tools |

**Key insight:** AI wasn't just a code generator — it was a design partner. The most valuable interactions were structuring complex multi-stakeholder requirements into clean architecture decisions, and rapidly iterating on edge-case handling that would normally take weeks of development cycles.

---

## Tech Stack

- **Application Platform:** BI application framework
- **AI Development Partner:** Generative AI assistant
- **Presentation:** AI-assisted slide generation
- **Narration:** Neural text-to-speech with SSML pacing
- **Data Source:** System firmographic records (financial metrics, territory mappings)

---

## What I Learned

1. **AI accelerates the full product lifecycle.** The hardest parts of this project were design decisions — permission models, team-specific logic, validation rules. AI enabled rapid exploration of architectural tradeoffs and immediate prototyping.

2. **Anticipate edge cases upfront.** When I imported a new data source, previously entered user data disappeared. Working with AI requires being explicit about constraints and invariants, not just desired features.

3. **Build for different users, not just one workflow.** The team-specific features were the most impactful part — and the most challenging to design. A generic tool wouldn't have achieved the same adoption.

4. **Ship fast, iterate based on feedback.** Each version was tested by real users who told me what was confusing or missing. AI made the iteration loop fast enough to respond same-day.

---

## License

This repository contains project documentation and desensitized materials only. No proprietary data, customer information, or internal system access is included.
