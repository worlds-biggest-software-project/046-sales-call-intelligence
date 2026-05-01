# Sales Call Intelligence — Feature & Functionality Survey

> Candidate #46 · Researched: 2026-05-01

## Solutions Analysed

| Tool | Type | Licence / Model | URL |
|------|------|-----------------|-----|
| Gong | Commercial SaaS | Proprietary; $1,200–$1,600/seat/yr + platform fee | https://gong.io |
| Chorus.ai (ZoomInfo) | Commercial SaaS | Proprietary; ~$1,000–$1,400/seat/yr | https://zoominfo.com/products/chorus |
| Clari Copilot (+ Salesloft) | Commercial SaaS | Proprietary; $60–$310/user/mo | https://clari.com |
| Avoma | Commercial SaaS | Proprietary; $19–$77/seat/mo | https://avoma.com |
| Fireflies.ai | Commercial SaaS | Proprietary; free–$39/user/mo | https://fireflies.ai |
| tl;dv | Commercial SaaS (Freemium) | Proprietary; free–$29/user/mo | https://tldv.io |
| Jiminny | Commercial SaaS | Proprietary; ~$85/user/mo | https://jiminny.com |
| Oliv AI | Commercial SaaS | Proprietary; from ~$50/user/mo | https://oliv.ai |
| Fathom | Commercial SaaS (Freemium) | Proprietary; free–$29/user/mo | https://fathom.video |
| OpenAI Whisper | Open Source | MIT licence | https://github.com/openai/whisper |

## Feature Analysis by Solution

### Gong

**Core features**
- Automatic call recording and transcription across Zoom, Teams, Google Meet, Dialpad, RingCentral, and telephony integrations
- AI-powered transcript analysis: talk-time ratios, question frequency, monologue detection, competitor mention tracking, and next-step clarity scoring
- Deal boards: aggregates conversation signals with CRM data to score deal health and surface at-risk opportunities
- Coaching scorecards: identify specific call moments (failed discovery question, missed objection response) for manager review and rep training
- Win/loss analytics: correlates conversation patterns (topics discussed, questions asked) with closed-won and closed-lost outcomes across cohorts

**Differentiating features**
- Market-defining depth: analyses 100+ conversation signals per call including filler word frequency, patience (silence handling), energy level, and empathy markers
- Deal likelihood scoring: 50% weighted on conversation intelligence, 50% on activity, contacts, timing, and CRM history; most comprehensive multi-signal model in category
- Call library: fully searchable transcript repository with topic filters, enabling reps to find examples of successful objection handling across the team's call history
- Revenue forecasting integration: conversation signals feed into pipeline health and forecast confidence scores

**UX patterns**
- Call recording card: per-call view with waveform, transcript, AI summary, and tagged moments for coaching
- Deal timeline: engagement activity chart showing interaction frequency and recency across all deal stakeholders
- Coaching dashboard: manager view of rep scorecards with comparative benchmarks against team average

**Integration points**
- Native: Salesforce, HubSpot, Microsoft Dynamics
- Conferencing: Zoom, Teams, Google Meet, Webex
- Telephony: Dialpad, RingCentral, Outreach, Salesloft
- Slack for call summary and deal alert delivery
- REST API for data export

**Known gaps**
- Very expensive; 15-seat minimum plus $5,000–$15,000 platform fee; ROI hard to prove for teams under 30 reps
- Transcription quality inconsistent for non-North-American English accents
- Coaching recommendations are pattern-matched to population averages, not personalised to individual rep development stage
- Win/loss analysis requires manual interview programs for the qualitative narrative layer; automated synthesis is limited
- No open-source or self-hosted option for regulated industries

**Licence / IP notes**
- Fully proprietary; Gong reportedly holds patents on aspects of its conversation intelligence methodology; specific patent claims were not verified in this research

---

### Chorus.ai (ZoomInfo)

**Core features**
- Call recording, transcription, and AI-powered conversation analysis
- Sentiment analysis: tracks buyer sentiment trajectory across the call timeline
- Deal intelligence: aggregates call signals with email and CRM activity for deal health view
- Deep Salesforce integration: activity data and conversation summaries written to opportunity records automatically
- Coaching workflow: call snippets shareable with reps for review; custom scoring rubric builder

**Differentiating features**
- Sentiment analysis trajectory is more granular than Gong's equivalent; tracks per-speaker sentiment across the call timeline rather than only aggregate sentiment
- Deep Salesforce native experience; often evaluated as the Salesforce-committed team's alternative to Gong
- ZoomInfo bundle: teams already paying for ZoomInfo can add Chorus at reduced marginal cost vs. standalone Gong

**UX patterns**
- Call review interface with sentiment timeline overlaid on waveform
- Coaching playlist: curated collections of call snippets for onboarding and methodology training

**Integration points**
- Native: Salesforce (primary), HubSpot (secondary)
- Zoom, Teams, Google Meet
- ZoomInfo data platform (native bundle)
- REST API

**Known gaps**
- Transcription accuracy described by users as inconsistent ("hit or miss") compared to Gong
- ZoomInfo bundle dependency; standalone pricing is less competitive than Gong
- Product investment slower since ZoomInfo acquisition; feature parity with Gong has widened in Gong's favour

**Licence / IP notes**
- Fully proprietary; acquired by ZoomInfo for $575M (2021)

---

### Clari Copilot (formerly Wingman, merged with Salesloft December 2025)

**Core features**
- Real-time whisper coaching during live calls: AI surfaced suggestions triggered by conversation events (competitor mention detected → show battlecard; pricing objection → show ROI calculator)
- Post-call summary: automatic meeting notes with action item extraction and CRM field population
- Deal intelligence: conversation signals feeding into the broader Clari forecasting and pipeline model
- Sales methodology adherence scoring: tracks whether reps asked discovery questions, covered required topics, and proposed clear next steps
- Combined with Salesloft (Dec 2025): sequencing, engagement, and conversation intelligence now in one platform

**Differentiating features**
- Most developed real-time whisper coaching of any commercial tool; live battlecard surfacing during calls is a genuine differentiator
- Clari platform integration: conversation signals directly feed deal health scores and revenue forecasts without a separate integration step
- Salesloft merger creates the most complete sequence-to-call-to-forecast pipeline under one subscription

**UX patterns**
- Copilot call overlay: side panel showing AI suggestions, battlecards, and talk track prompts in real time during the call
- Post-call workspace: structured meeting summary with action items, follow-up draft, and CRM sync confirmation

**Integration points**
- Native: Salesforce, HubSpot
- Zoom, Teams (via bot join)
- Salesloft (native, post-merger)
- Slack for summary and alert delivery

**Known gaps**
- Full Clari stack ($200–$310/user/mo) is expensive; Copilot standalone pricing more accessible ($60–$100/user/mo) but loses forecasting integration benefit
- Integration complexity post-Salesloft merger still stabilising as of 2026
- Real-time coaching quality depends on low-latency transcription; VoIP quality issues can degrade suggestion timing

**Licence / IP notes**
- Fully proprietary; Wingman acquired by Clari 2022; merged into Salesloft platform December 2025

---

### Avoma

**Core features**
- Full meeting lifecycle platform: pre-meeting agenda templates, live note-taking, post-call AI summary, and CRM sync
- AI scorecards: tracks adherence to sales methodology (MEDDIC, SPICED, BANT) with per-call scoring
- Talk pattern analysis: talk-time ratio, monologue detection, and question-asking frequency for coaching
- CRM field auto-update: writes meeting notes, action items, and deal fields to Salesforce/HubSpot
- Revenue intelligence tier: deal risk assessment and pipeline health scoring (add-on tier)

**Differentiating features**
- Best value full-stack meeting intelligence tool; $77/user/mo fully loaded vs. $1,400–$2,000/seat/yr for Gong
- Pre-meeting agenda templates linked to CRM opportunity context; unique structured meeting preparation layer
- Methodology scorecards (MEDDIC, SPICED, BANT) built into core product, not a separate add-on

**UX patterns**
- Meeting dashboard: pre-meeting → in-meeting → post-meeting workflow in a single continuous view
- AI summary: structured sections (summary, key points, action items, next steps) auto-generated per call

**Integration points**
- Native: Salesforce, HubSpot
- Zoom, Teams, Google Meet
- Slack for summary delivery
- Calendar: Google Calendar, Outlook for meeting detection

**Known gaps**
- Pricing complexity: $19 base + $29 CI add-on + $29 RI add-on = $77/user/mo fully loaded; not immediately obvious
- Revenue intelligence features (deal risk) less mature than Gong/Clari
- Smaller coaching dataset than Gong; population benchmarks less statistically reliable

**Licence / IP notes**
- Fully proprietary

---

### Fireflies.ai

**Core features**
- Automatic recording and transcription across 69 languages on Zoom, Teams, Google Meet, Webex, and others
- AI meeting summary with key topics, action items, and sentiment indicators
- Full-text search across all recorded transcripts
- Integration with project management and collaboration tools (Slack, ClickUp, Notion, Asana)
- Free tier: 800 minutes of transcription storage; Pro $10/user/mo; Business $19/user/mo

**Differentiating features**
- Broadest language coverage (69 languages) in the call intelligence category; meaningful for multilingual sales teams
- Most accessible pricing in the category; free tier usable for individuals and small teams
- Integration breadth: connects to project management and note-taking tools beyond CRM, serving non-sales use cases

**UX patterns**
- Notebook-style transcript view with AI-highlighted topics, action items, and custom tracker keywords
- Team dashboard: shared meeting library with search and filter by speaker, topic, and date

**Integration points**
- CRM: Salesforce, HubSpot, Pipedrive, Zoho
- Collaboration: Slack, Notion, ClickUp, Asana, Trello
- Calendar: Google Calendar, Outlook
- REST API; Zapier

**Known gaps**
- Deal intelligence, pipeline forecasting, and sales methodology scoring absent from core product
- Designed for general meeting capture, not specifically for sales coaching or revenue intelligence
- Transcript accuracy lower than Gong for technical or domain-specific sales vocabulary

**Licence / IP notes**
- Fully proprietary

---

### Oliv AI

**Core features**
- Auto-scores MEDDIC, BANT, and SPICED from call transcripts without manual rep input; writes scores directly to CRM fields
- Real-time call coaching: live whisper suggestions during calls triggered by conversation events
- Post-call summary: structured AI notes with action items, deal insights, and CRM sync
- Deal workspace: per-deal view combining methodology scores, activity timeline, and AI recommendations
- Modular pricing: accessible from ~$50/user/mo

**Differentiating features**
- Most automated methodology scoring in the category: MEDDIC/BANT/SPICED extracted from conversation without rep intervention
- Purpose-built AI-first architecture (not a legacy platform with AI added)
- Real-time coaching comparable to Clari Copilot at a lower price point
- Fast-growing adoption among growth-stage B2B companies (50–500 employees) who cannot justify Gong's pricing

**UX patterns**
- Call coaching overlay: live suggestion panel surfacing methodology prompts and competitive context during the call
- Deal workspace: scorecard view with methodology field completion status and gap identification

**Integration points**
- Salesforce, HubSpot
- Zoom, Teams, Google Meet
- Slack for deal alerts

**Known gaps**
- Newer entrant; unproven at large enterprise scale (500+ seat deployments)
- Smaller training dataset than Gong; population benchmarks less statistically reliable
- Forecast integration less developed than Gong/Clari

**Licence / IP notes**
- Fully proprietary

---

### Fathom

**Core features**
- Free automatic recording, transcription, and AI meeting notes for individuals
- Meeting summary: structured output (key topics, decisions, action items) delivered within seconds of call ending
- CRM-linked follow-up: pushes meeting notes and action items to HubSpot/Salesforce with one click
- Async video clip sharing: create timestamped clip from transcript to share specific call moments

**Differentiating features**
- Best individual-use free tier in the category; 80% of core call intelligence value at zero cost for individual reps
- Fastest post-call summary delivery (within ~10 seconds of call ending)
- Minimal onboarding friction: installs as a Chrome extension or Zoom app with no admin configuration required

**UX patterns**
- Minimal, single-call-focused UI; not a team dashboard product
- Post-call summary delivered in-app and via email immediately after call ends

**Integration points**
- Zoom, Teams, Google Meet
- HubSpot, Salesforce (CRM sync with one click)
- Slack (summary sharing)

**Known gaps**
- No team coaching dashboard, methodology scoring, or pipeline intelligence
- Not a revenue intelligence tool; purely a note-taking and summary productivity tool at team scale
- Limited to individual or small team use; no enterprise administration, SSO, or data governance

**Licence / IP notes**
- Fully proprietary

---

### OpenAI Whisper

**Core features**
- Open-source automatic speech recognition (ASR) model trained on 680,000 hours of multilingual audio
- Supports 99 languages with near-human transcription accuracy for common languages
- Available in multiple model sizes (tiny, base, small, medium, large, large-v3) for speed/accuracy tradeoff
- Python library and CLI; can be integrated into any application pipeline

**Differentiating features**
- MIT-licenced: only production-quality open-source ASR model available for commercial use without royalties
- Runs locally: no audio data transmitted to external APIs; critical for regulated industry deployments
- Large-v3 model performance competes with commercial ASR services for standard English transcription

**UX patterns**
- Code-only library; no UI; requires developer integration into a broader pipeline
- Outputs structured JSON with word-level timestamps, enabling precise transcript alignment with audio

**Integration points**
- Any Python/command-line environment
- Commonly integrated with speaker diarisation (pyannote.audio) and NLP pipelines for downstream analysis

**Known gaps**
- Documented hallucination risk in long-form audio: systematic errors in low-audio or noisy segments that produce plausible but incorrect transcription (Koenecke et al., 2024; preprint)
- No speaker diarisation built in; requires separate pyannote.audio or similar library to attribute speech to speakers
- No CRM integration, coaching logic, or deal intelligence; purely a transcription model
- Accuracy degrades for non-North-American English accents, technical jargon, and domain-specific vocabulary

**Licence / IP notes**
- MIT licence: fully permissive; commercial use unrestricted; modifications do not require open-sourcing; note that while the model weights are open-source, the training data methodology is proprietary to OpenAI

---

## Cross-Cutting Feature Themes

### Table-Stakes Features
- Automatic call recording across primary video conferencing platforms (Zoom, Teams, Google Meet)
- Speech-to-text transcription with per-speaker attribution (diarisation)
- AI meeting summary: key topics, decisions, and action items extracted automatically
- CRM sync: meeting notes and action items written to Salesforce/HubSpot opportunity records
- Full-text transcript search across the team's call history
- Basic coaching analytics: talk-time ratio, monologue detection, question frequency per call
- Two-party consent handling: geographic-aware recording consent notifications

### Differentiating Features
- Real-time whisper coaching during live calls: AI surfaces battlecards, talk track prompts, and methodology reminders triggered by conversation events
- Sales methodology auto-scoring (MEDDIC/MEDDPICC, BANT, SPICED) from transcripts without rep input; written directly to CRM fields
- Deal risk detection from conversation patterns: ghosting signals, single-threaded relationships, pricing objection frequency trends
- Revenue forecasting integration: conversation signals feeding pipeline health scores and forecast confidence
- Personalised rep coaching paths based on longitudinal call pattern and deal outcome analysis
- Competitive intelligence integration: real-time competitor mention detection triggering relevant battlecard surfacing
- Win/loss synthesis: automated analysis of closed deal transcripts to surface loss reason patterns at cohort level
- Multilingual transcription with accuracy on non-North-American accents (underserved by current market leaders)

### Underserved Areas / Opportunities
- **No viable open-source call intelligence pipeline**: Whisper handles transcription, but no open-source project combines diarisation → transcript → NLP → CRM write-back → coaching scorecard in a production-ready pipeline; this would unlock the capability for teams priced out of Gong ($1,400–$2,000/seat/yr)
- **Self-hosted regulated industry deployment**: Financial services, healthcare, and defence teams cannot send recordings to Gong's cloud; an open-source or self-hosted pipeline using Whisper and a local LLM would serve this segment with no current competition
- **Personalised longitudinal coaching**: Current tools benchmark reps against team averages and static methodology checklists; a system building a longitudinal model of each rep's individual patterns and connecting them to deal outcomes would be meaningfully more actionable
- **Multilingual and accent coverage**: Gong and Chorus are optimised for North American English; growing B2B SaaS markets in LATAM, SEA, and MENA are systematically underserved; fine-tuned Whisper models for specific languages and accents represent a genuine gap
- **CRM hygiene automation without rep trigger**: Most tools require reps to initiate CRM sync; an autonomous agent that listens, extracts structured deal data, and writes to CRM fields with zero rep action is technically feasible but not fully productised

### AI-Augmentation Candidates
- Transcription: commercial ASR API dependency → open-source Whisper (MIT) running locally, removing data egress and cost
- Speaker attribution: rule-based channel detection → neural diarisation (pyannote.audio) with per-speaker signal extraction
- Meeting summary: template-filled bullet points → LLM-generated contextual summary tailored to deal stage and CRM context
- Methodology scoring: manual rep-entered MEDDIC fields → automatic extraction from call transcript with gap identification
- Real-time coaching: post-call-only analysis → live transcription stream enabling real-time suggestion injection during the call
- Win/loss analysis: periodic manual interview programs → continuous LLM synthesis from closed deal transcript corpus

## Legal & IP Summary

OpenAI Whisper is MIT-licenced: the model weights and code are fully open for commercial use without royalties or share-alike obligations, making it the only viable open-source ASR foundation for a self-hosted pipeline. Pyannote.audio (speaker diarisation) is MIT-licenced for its recent versions; confirm the specific version licence before production use. All commercial platforms (Gong, Chorus, Clari Copilot, Avoma, Fireflies, tl;dv, Jiminny, Oliv AI, Fathom) are fully proprietary. Call recording consent laws apply in all deployments: GDPR (EU), CCPA (California), and US state two-party consent laws (including Illinois, Florida, Pennsylvania, and others) require that all parties consent to recording; geographic-aware consent workflows are legally mandatory for any call intelligence product. Gong reportedly holds patents related to aspects of its conversation intelligence methodology; specific patent numbers were not independently verified, and freedom-to-operate analysis is recommended before implementing similar signal-analysis techniques. Koenecke et al. (2024 preprint) documents systematic Whisper hallucination risk in long-form audio, which must be disclosed to users and mitigated with confidence scoring in any production deployment.

## Recommended Feature Scope

**Must-have (MVP)**:
- Automatic call bot joining and recording across Zoom, Teams, and Google Meet
- Whisper-based (or equivalent) transcription with speaker diarisation
- AI meeting summary: structured output with key topics, decisions, and action items within 60 seconds of call end
- CRM auto-sync: meeting summary, action items, and next steps written to Salesforce/HubSpot opportunity without rep action
- Full-text transcript search across team call history with speaker and date filters
- Two-party consent notifications with geographic awareness (EU, US two-party states)
- Basic coaching analytics per call: talk-time ratio, monologue detection, question frequency

**Should-have (v1.1)**:
- Sales methodology auto-scoring: extract MEDDIC/BANT/SPICED field values from transcript and write to CRM fields automatically
- Keyword and topic tracker: custom tracker terms (competitor names, objection phrases, product names) flagged across all calls with trend reporting
- Deal risk signals from conversation patterns: detect ghosting indicators, single-threaded engagement, and pricing objection frequency trends
- Coaching scorecard: per-rep aggregated scores with comparison to team benchmarks and trend over time
- Win/loss pattern analysis: LLM synthesis of conversation patterns across closed-won vs. closed-lost deals

**Nice-to-have (backlog)**:
- Real-time whisper coaching during live calls: live transcription stream with AI-surfaced battlecards, methodology prompts, and objection responses triggered by conversation events
- Personalised rep coaching paths: longitudinal model of each rep's individual strengths, blindspots, and development trajectory correlated with deal outcomes
- Self-hosted deployment option: full pipeline (recording → transcription via local Whisper → LLM analysis → CRM sync) deployable on-premises for regulated industry use
- Multilingual transcription fine-tuned for non-North-American accents (LATAM Spanish, Southeast Asian English, DACH German)
- Competitive intelligence integration: competitor mention detection triggers relevant battlecard surfacing inline in the call interface
