# Sales Call Intelligence

A conversation intelligence platform that records, transcribes, and analyzes sales calls with AI-driven coaching, MEDDIC/SPICED methodology auto-scoring, and deal risk detection—positioned as a best-value alternative to Gong for mid-market teams.

## Problem Statement

Conversation intelligence is expensive and hard to justify:
- **Gong** sets the gold standard ($1,200–$1,600/seat/year + $5,000–$15,000 platform fee; 15-seat minimum) but ROI is hard to prove for smaller teams
- **Mid-market alternatives** (Avoma, Fireflies.ai) offer better pricing but lack deal intelligence and coaching infrastructure
- **Transcription quality** varies: Whisper-based systems exhibit documented hallucination and bias issues (Koenecke et al., 2024)
- **No open-source option** exists combining call recording, transcription, and methodology auto-scoring

## Key Differentiators

### MEDDIC/SPICED Auto-Scoring
- Automatically score deals against enterprise qualification frameworks from call transcripts
- Surface missing signals (Budget, Authority, Need, Timeline) for reps in real-time
- No manual review required; reduces deal slippage by identifying stalled conversations

### Lightweight Pricing
- Mid-market sweet spot: $50–$77/seat/month fully loaded vs. Gong's $100–$130/seat/month
- No 15-seat minimum; suitable for 5–50 person sales teams
- Transparent per-seat model vs. Gong's opaque platform fee + seat cost structure

### Deal Risk Detection
- Real-time risk alerts for single-threaded relationships, reduced engagement, pricing objections, ghosting post-proposal
- Coaches surface coaching moments (specific call transcripts + timestamps for manager review)
- Win/loss analysis: identify patterns in closed-won vs. closed-lost communication

### Meeting Lifecycle Management
- Full journey: pre-meeting brief generation, during-call transcription and guidance, post-meeting summary and follow-up drafts
- CRM sync: call recordings, transcripts, and action items written back to opportunity records
- Async sharing: team members can watch call replays with comments and coaching notes

## Market Context

- **Market size**: Conversation intelligence market $32.25B in 2026, projected to reach $55.7B by 2035 at 23.5% CAGR
- **Adoption**: 46% of US sales teams now use AI call recording (up from 38% in 2023); expected to reach 57% by end-2025
- **Key competitors**: Gong ($1,200–$1,600/seat/year), Chorus.ai/ZoomInfo ($1,000–$1,400/seat/year), Avoma ($77/seat/month fully loaded)
- **Positioning**: Best-value conversation intelligence for mid-market teams needing deal intelligence without enterprise pricing

## Recommended MVP Scope

- Call recording across Zoom, Teams, Google Meet, and telephony platforms (Dialpad, RingCentral)
- AI transcription with documented accuracy benchmarks (vs. Whisper baseline)
- MEDDIC/SPICED methodology auto-scoring from transcripts
- Real-time coaching moments identification: flag specific call segments for manager review
- Deal risk alerts: single-threading, ghosting, reduced engagement, pricing objections
- CRM bi-directional sync (Salesforce, HubSpot native)
- Win/loss analysis dashboard: close rates by qualification signal, rep, segment
- Manager coaching dashboard with rep-level benchmarking and performance trends

## Resources

**Research Materials**: [research.md](research.md) | **Feature Analysis**: [features.md](features.md)

## Target Users

- Sales managers at mid-market B2B SaaS companies (25–150 rep teams) seeking deal intelligence and coaching
- Sales enablement leaders responsible for rep coaching and onboarding acceleration
- RevOps managers building deal health dashboards and pipeline governance
- Enterprise sales teams needing cost-effective conversation intelligence alternative to Gong
