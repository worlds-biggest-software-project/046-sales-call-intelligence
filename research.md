# Sales Call Intelligence

> Candidate #46 · Researched: 2026-05-01

## Existing Products and Software Packages

| Tool | Type | Pricing | Notes |
|------|------|---------|-------|
| **Gong** | Commercial | $1,200–$1,600/seat/year + $5,000–$15,000 platform fee; 15-seat minimum | Market leader in revenue intelligence; strongest standalone forecasting and deal analytics; expensive for SMBs; occasional transcription redaction issues |
| **Chorus.ai (ZoomInfo)** | Commercial | ~$1,000–$1,400/seat/year; usually bundled with ZoomInfo at $15,000–$40,000+/year | Strong sentiment analysis; deep Salesforce integration; transcription accuracy described as "hit or miss" by users; ZoomInfo bundle dependency is costly |
| **Clari Copilot** (formerly Wingman) | Commercial | $60–$100/user/month ($720–$1,200/year); full Clari stack $200–$310/user/month | Conversation intelligence module of the broader Clari revenue platform; merged with Salesloft in Dec 2025 for full RevOps stack |
| **Avoma** | Commercial | $19/seat/month base; with Conversation Intelligence +$29 and Revenue Intelligence +$29 = $77/seat/month fully loaded | Full meeting lifecycle management; CRM sync; mid-market sweet spot; pricing complexity as add-ons required |
| **Fireflies.ai** | Commercial | Free tier (800 min/seat); Pro $10/user/month; Business $19; Enterprise $39 (annual) | Clean pricing; excellent for transcription/search; lacks deal intelligence, pipeline forecasting, and sales methodology scoring |
| **tl;dv** | Commercial (Freemium) | Free tier unlimited recordings; paid plans from ~$29/user/month | Strong async sharing and CRM-linked follow-ups; better as a notes/workflow tool than coaching infrastructure |
| **Salesloft** (formerly with standalone CI) | Commercial | Bundled into Clari post-Dec 2025 merger; previously ~$75–$125/user/month | Sales engagement + conversation intelligence combined; enterprise-oriented; now absorbed into Clari platform |
| **Jiminny** | Commercial | ~$85/user/month | MEDDIC/SPICED scoring; strong UK/EU presence; smaller market footprint than Gong/Chorus |
| **Oliv AI** | Commercial | Modular pricing; starter plans ~$50/user/month | Agentic execution; auto-scores MEDDIC, BANT, SPICED from call transcripts; newer entrant with fast-growing adoption |
| **Fathom** | Commercial (Freemium) | Free for individuals; team plans ~$19–$29/user/month | Lightweight note-taker; 80% of value at 10–20% of Gong's price; limited enterprise coaching features |

## Relevant Industry Standards or Protocols

- **MEDDIC / MEDDPICC** — de facto enterprise deal qualification framework; leading CI platforms auto-score it from call transcripts
- **SPICED** (Winning by Design) — B2B SaaS recurring revenue qualification standard; AI platforms increasingly auto-enforce it
- **BANT** — legacy qualification framework (Budget, Authority, Need, Timeline); still widely tracked by SMB-oriented tools
- **WebRTC / SIP / VoIP integration standards** — required for real-time call capture across telephony stacks (Zoom, Teams, Dialpad, RingCentral)
- **GDPR / CCPA call recording compliance** — two-party consent requirements govern recording legality; all enterprise tools must handle geographic consent workflows
- **OpenAI Whisper** — de facto open-source ASR baseline (note: documented hallucination risk in long-form audio per Koenecke et al., 2024)

## Available Research Materials

1. Koenecke, A. et al. (2024). "Errors in Speech-to-Text Can Be Harmful and Offensive." *arXiv preprint*. https://arxiv.org/abs/ — flags systematic bias and hallucination in Whisper-based transcription. (Preprint)
2. Coffee AI Research. (2026). "Best Conversation Intelligence Software for Sales Teams 2026." *coffee.ai*. https://www.coffee.ai/articles/conversation-intelligence-software-guide-2026/ — practitioner buyer's guide with pricing comparisons. (Industry report)
3. Clari Labs. (2026). "87% of Enterprises Missed Revenue Targets in 2025 Despite Record AI Investment." *Clari Press*. https://www.clari.com/press/new-clari-labs-research-reveals-enterprises-missed-revenue-targets-in-2025/ — market research on AI adoption gaps. (Vendor research)
4. Oliv AI Blog. (2026). "Sales Methodology Automation: Auto-Score MEDDIC, BANT & SPICED from Calls." *oliv.ai*. https://www.oliv.ai/blog/sales-methodology-automation-auto-score-meddic-bant-spiced-from-calls — technical overview of methodology automation via NLP. (Vendor white paper)
5. Claap Research. (2026). "Gong vs. Chorus (2026): The Honest Comparison for Sales Teams." *claap.io*. https://www.claap.io/blog/gong-vs-chorus-which-is-better-and-why — detailed feature/pricing comparison. (Industry analysis)
6. Outdoo AI. (2026). "Gong.io Pricing 2026: Costs vs 4 Revenue Intelligence Alternatives." *outdoo.ai*. https://www.outdoo.ai/blog/gong-io-pricing-vs-4-others — pricing breakdown with procurement data. (Industry analysis)
7. MarketResearchFuture. (2025). "Conversation Intelligence Market — Global Forecast 2025–2033." — market projects $23.4B (2024) to $55.7B (2035) at ~23.5% CAGR. (Market research report)

## Market Research

**Market Size:** The conversation intelligence software market was valued at ~$23.4B in 2024, projected to reach $55.7B by 2035 at a 23.5% CAGR. The 2026 figure is estimated at $32.25B (MarketResearchFuture, 2025).

**Adoption:** 46% of US sales teams now use AI call recording (up from 38% in 2023), expected to reach 57% by end of 2025.

**Pricing Landscape:**

| Tier | Example | Annual Cost (10-rep team) |
|------|---------|--------------------------|
| Enterprise | Gong | $21,000–$36,000+/year (incl. platform fee) |
| Mid-market | Avoma (full stack) | ~$9,240/year |
| SMB/Prosumer | Fireflies Business | ~$2,280/year |
| Freemium | Fathom / tl;dv | $0–$3,480/year |

**Key Buyer Personas:**
- VP of Sales / CRO: wants deal risk visibility and forecasting accuracy
- Sales Enablement Manager: wants rep coaching and methodology adherence scoring
- Revenue Operations: needs CRM hygiene automation and call data for analytics
- Sales Rep: wants auto-generated notes and follow-up drafts

**Notable M&A / Funding:**
- Gong raised $250M Series E (2021) at $7.25B valuation; remains private as of 2026
- Chorus.ai acquired by ZoomInfo for $575M (2021); now bundled with ZoomInfo data subscriptions
- Clari merged with Salesloft (December 2025), creating a combined revenue platform
- Wingman (CI tool) acquired by Clari (2022), now marketed as Clari Copilot

## AI-Native Opportunity

- **Methodology enforcement is still manual in most tools:** Gong surfaces insights but relies on managers to act; an AI-native tool could auto-coach reps in real time during calls (live whisper coaching) without requiring post-call review workflows
- **No open-source alternative exists at feature parity:** Whisper handles transcription, but there is no open-source pipeline covering diarization → transcript → NLP → CRM write-back → coaching scorecard; an OSS stack would unlock this for teams priced out of Gong
- **CRM data hygiene is still a manual tax:** tools transcribe but require reps to trigger syncs; an AI-native agent could listen, extract structured deal data (MEDDIC fields, next steps, stakeholders), and write directly to CRM fields with zero rep action
- **Coaching personalization is shallow:** current platforms show aggregate talk-time ratios; AI could deliver individualized coaching paths per rep based on longitudinal behavioral patterns and deal outcomes
- **Multilingual and accent coverage is poor:** Gong and Chorus are optimized for North American English; an open-source model fine-tuned on global accents and languages would serve underserved markets (LATAM, SEA, MENA) where enterprise SaaS penetration is growing fastest
