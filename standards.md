# Standards & API Reference

> Project: Sales Call Intelligence · Generated: 2026-05-06

## Industry Standards & Specifications

### ISO Standards

**ISO/IEC 27001:2022 — Information Security Management Systems**
- URL: https://www.iso.org/standard/27001
- The baseline security certification required by enterprise B2B buyers before onboarding any vendor that processes recorded audio or call transcripts. Governs policies, access controls, supplier management, and incident handling for the full call-data lifecycle.

**ISO/IEC 42001:2023 — AI Management Systems**
- URL: https://www.iso.org/standard/81230.html
- Emerging alongside ISO 27001 as a baseline requirement for 2026 AI product procurement. Addresses AI-specific risks including model bias, data poisoning, and algorithmic governance — directly applicable to LLM-based coaching and deal-scoring features.

---

### W3C & IETF Standards

**W3C WebVTT — Web Video Text Tracks Format**
- URL: https://www.w3.org/TR/webvtt1/
- The W3C standard for timed text in web video, using MIME type `text/vtt`. This is the native transcript format produced by Zoom Cloud Recording, Microsoft Teams, and AssemblyAI. All transcript storage, search indexing, and export pipelines should support ingestion and emission of WebVTT alongside SRT.

**RFC 8825 — Overview: Real-Time Protocols for Browser-Based Applications (WebRTC)**
- URL: https://datatracker.ietf.org/doc/html/rfc8825
- Top-level overview of the WebRTC protocol suite. Relevant for any real-time call capture architecture, in-browser recording bots, or live transcription features that operate within a web client context.

**RFC 8826 — Security Considerations for WebRTC**
- URL: https://www.rfc-editor.org/rfc/rfc8826.html
- Defines the WebRTC threat model and mandates DTLS-SRTP encryption for all media streams. Required reading for any live-call audio capture implementation to ensure encrypted transmission of sensitive sales conversations.

**RFC 8827 — WebRTC Security Architecture**
- URL: https://datatracker.ietf.org/doc/html/rfc8827
- Specifies the security architecture for WebRTC deployments, covering identity verification and browser-based media security. Relevant for building in-browser meeting bots that capture audio without a server-side proxy.

**RFC 7478 — Web Real-Time Communication Use Cases and Requirements**
- URL: https://www.rfc-editor.org/rfc/rfc7478
- Defines the canonical use cases and functional requirements that underpin the WebRTC protocol suite. Useful for aligning real-time call capture design to the intended scope of the standards.

**RFC 6749 — The OAuth 2.0 Authorization Framework**
- URL: https://www.rfc-editor.org/rfc/rfc6749
- Foundation for all delegated-access integrations: CRM write-back (Salesforce, HubSpot), calendar-based bot scheduling, and conferencing platform API access. Every integration in a sales call intelligence platform requires OAuth 2.0 flows.

**RFC 6750 — The OAuth 2.0 Authorization Framework: Bearer Token Usage**
- URL: https://www.ietf.org/rfc/rfc6750.txt
- Specifies how Bearer tokens are transmitted in HTTP Authorization headers. Standard mechanism used by Salesforce, HubSpot, Zoom, and Microsoft Graph APIs for authenticated API requests.

---

### Data Model & API Specifications

**OpenAPI Specification 3.1 / 3.2**
- URL: https://spec.openapis.org/oas/v3.2.0.html · https://www.openapis.org/
- Industry-standard format for describing REST APIs in YAML or JSON, with full JSON Schema Draft 2020-12 compatibility. All public-facing REST endpoints (transcript retrieval, call metadata, coaching scorecard export) should be documented in OpenAPI 3.1+.

**WebVTT (MIME: text/vtt) and SRT (SubRip Text)**
- URL: https://www.w3.org/TR/webvtt1/ · https://matroska.org/technical/specs/subtitles/srt.html
- The two universal transcript interchange formats. WebVTT is the W3C standard preferred for web-native playback; SRT is the de facto standard for broad tool compatibility. Any transcript export pipeline should support both formats.

**JSON-LD / Schema.org — Structured Data for Conversational AI Metadata**
- URL: https://schema.org/ · https://json-ld.org/
- Emerging practice for encoding structured call metadata (participants, topics, action items, entities) in machine-readable linked-data format, enabling downstream integration with knowledge graphs, CRM systems, and RAG pipelines.

---

### Security & Authentication Standards

**OAuth 2.0 (RFC 6749 / RFC 6750)**
- URL: https://oauth.net/2/
- See entries above. Mandatory for all CRM, calendar, and conferencing API integrations.

**OpenID Connect Core 1.0**
- URL: https://openid.net/specs/openid-connect-core-1_0.html
- Authentication identity layer built on OAuth 2.0. Required for any multi-tenant SaaS deployment where users authenticate via Google Workspace, Microsoft Entra ID (formerly Azure AD), or other SSO providers — which is standard in enterprise sales tooling procurement.

**GDPR (EU) 2016/679 — General Data Protection Regulation**
- URL: https://gdpr-info.eu/
- Governs recording consent for calls involving EU-based participants. Requires: informing all parties that the call is being recorded, specifying the legal basis and purpose, defining retention periods, and honouring right-to-erasure requests for call recordings and transcripts. Violations carry fines up to €20 million or 4% of global annual revenue.

**CCPA — California Consumer Privacy Act (as amended by CPRA)**
- URL: https://oag.ca.gov/privacy/ccpa
- US state-level equivalent for California residents. Requires transparency about data collection and opt-out rights. Emphasizes opt-out (vs. GDPR's opt-in consent model). Stricter CCPA enforcement and new requirements have been enforced through 2025–2026.

**Two-Party Consent / All-Party Consent Call Recording Laws**
- Multiple US states (California, Florida, Illinois, Maryland, etc.) and many non-US jurisdictions require all parties to consent before a call is recorded. AI-native tools must implement geographic consent routing: detecting call-participant jurisdictions and triggering the appropriate consent disclosure before recording begins.

**OWASP LLM Top 10 (v2.0, 2025) — AI Security for LLM Applications**
- URL: https://genai.owasp.org/llm-top-10/ · https://owasp.org/www-project-top-10-for-large-language-model-applications/
- Industry reference for LLM-specific security vulnerabilities. Key risks for a sales call intelligence platform: (1) Prompt Injection — adversarial instructions embedded in call transcripts could manipulate summarisation or CRM write-back agents; (2) Sensitive Information Disclosure — transcripts contain PII, contract terms, and pricing that must not leak across tenant boundaries; (3) Excessive Agency — automated CRM write-back agents must have scoped, auditable permissions.

**OWASP Top 10 for Agentic Applications (2026)**
- URL: https://www.trydeepteam.com/docs/frameworks-owasp-top-10-for-agentic-applications · https://genai.owasp.org/
- Companion framework to the LLM Top 10, focusing on autonomous AI systems. Directly relevant to CRM write-back agents, live whisper-coaching agents, and any tool that takes action (email follow-ups, CRM updates) based on AI inference from call content.

**SOC 2 Type II**
- URL: https://www.aicpa-cima.com/topic/audit-assurance/audit-and-assurance-tools-and-aids/soc-2
- Enterprise B2B buyers evaluating call recording vendors consistently request SOC 2 Type II audit reports alongside ISO 27001 certificates before technical evaluation begins. Any open-source tool seeking enterprise adoption should provide a clear path to SOC 2 compliance for self-hosted deployments.

---

### MCP Server Specifications

**Model Context Protocol (MCP)**
- URL: https://modelcontextprotocol.io/ · https://github.com/modelcontextprotocol/specification
- An emerging open protocol for connecting LLM agents to data sources and tools. A sales call intelligence platform could expose an MCP server interface so that AI assistants (Claude, Copilot, etc.) can query call transcripts, deal signals, and coaching notes in real time — enabling conversational access to call library and pipeline data without requiring a bespoke integration per AI platform.

---

## Similar Products — Developer Documentation & APIs

### Gong

- **Description:** Market-leading revenue intelligence platform. Provides programmatic access to call recordings, transcripts, conversation analytics, deal boards, and user activity data.
- **API Documentation:** https://help.gong.io/docs/what-the-gong-api-provides
- **SDKs/Libraries:** Unofficial Ruby gem (https://github.com/matteeyah/gong-api); Python data loader via dltHub (https://dlthub.com/context/source/gong); Postman collection (https://www.postman.com/growment/gong-meetup/collection/yuikwaq/gong-api-beginners-guide)
- **Developer Guide:** https://help.gong.io/docs/receive-access-to-the-api
- **Standards:** REST/JSON; no public OpenAPI document available
- **Authentication:** Access Key + Access Key Secret (HTTP Basic Auth–style credential pair); requires Gong admin role to generate credentials

---

### Fireflies.ai

- **Description:** AI meeting recorder and note-taker with GraphQL API for querying transcripts, summaries, and meeting metadata. Widely used by SMB and mid-market sales teams.
- **API Documentation:** https://docs.fireflies.ai/getting-started/introduction
- **SDKs/Libraries:** No official SDK; GraphQL endpoint consumed directly or via REST wrappers
- **Developer Guide:** https://docs.fireflies.ai/getting-started/introduction
- **Standards:** GraphQL (not REST); queries return JSON
- **Authentication:** API Key passed as Bearer token in Authorization header

---

### AssemblyAI

- **Description:** Developer-first speech-to-text and audio intelligence API. Provides transcription, speaker diarization, sentiment analysis, auto-chapters, and entity detection — the building-block APIs for a custom sales call intelligence pipeline.
- **API Documentation:** https://www.assemblyai.com/docs/api-reference/overview
- **SDKs/Libraries:** Python (https://github.com/AssemblyAI/assemblyai-python-sdk · PyPI: `assemblyai`); JavaScript/Node.js (https://assemblyai.github.io/assemblyai-node-sdk/); LangFlow integration (https://docs.langflow.org/bundles-assemblyai)
- **Developer Guide:** https://www.assemblyai.com/docs/api-reference/transcripts/submit
- **Standards:** REST/JSON; no published OpenAPI document but well-structured endpoint reference
- **Authentication:** API Key via `Authorization` header

---

### OpenAI Whisper (Open Source + Managed API)

- **Description:** The de facto open-source ASR baseline (MIT licence). Available as a self-hosted Python package or via the OpenAI managed API (whisper-1, gpt-4o-transcribe, gpt-4o-mini-transcribe models).
- **API Documentation:** https://developers.openai.com/api/docs/guides/speech-to-text
- **SDKs/Libraries:** GitHub (https://github.com/openai/whisper); whisper.cpp C/C++ port (https://github.com/ggml-org/whisper.cpp); Hugging Face model hub (https://huggingface.co/openai/whisper-large-v3)
- **Developer Guide:** https://developers.openai.com/api/docs/guides/speech-to-text
- **Standards:** REST/JSON for managed API; Python library for self-hosted; supports mp3, mp4, mpeg, mpga, m4a, wav, webm input; outputs json, text, srt, vtt
- **Authentication:** OpenAI API Key (Bearer token)
- **Note:** File uploads capped at 25 MB via the managed API. Known hallucination risk in long-form audio (Koenecke et al., 2024) — validate output quality before deploying in production sales coaching contexts.

---

### pyannote.audio / pyannoteAI

- **Description:** Leading open-source speaker diarization toolkit (MIT/commercial). The OSS model (`pyannote/speaker-diarization-3.1`) achieves ~10% DER on standard benchmarks. pyannoteAI offers a managed Precision-2 API with significantly higher accuracy.
- **API Documentation:** https://www.pyannote.ai/ · https://huggingface.co/pyannote/speaker-diarization-3.1
- **SDKs/Libraries:** `pip install pyannote.audio` (Hugging Face model hub); pyannoteAI managed API (REST)
- **Developer Guide:** https://docs.vast.ai/examples/transcription/speaker-diarization-pyannote
- **Standards:** Python library; Hugging Face model hub format; pyannoteAI REST API
- **Authentication:** Hugging Face token (OSS); pyannoteAI API key (managed)

---

### Recall.ai

- **Description:** Infrastructure-layer API for deploying meeting bots across Zoom, Google Meet, Microsoft Teams, and Webex. Handles bot lifecycle management, real-time and post-meeting transcription, and metadata capture — the lowest-friction path to multi-platform recording without platform-specific bot development.
- **API Documentation:** https://docs.recall.ai/docs/getting-started
- **SDKs/Libraries:** REST API; no official SDK; integrates with AssemblyAI transcription (https://www.assemblyai.com/docs/integrations/recall)
- **Developer Guide:** https://docs.recall.ai/docs/quickstart · https://docs.recall.ai/docs/bot-real-time-transcription
- **Standards:** REST/JSON; webhook-based event delivery for real-time transcript events
- **Authentication:** API Key

---

### Zoom Meetings & Recording API

- **Description:** Zoom's REST API for managing meetings, retrieving cloud recordings, and accessing transcripts. The primary conferencing integration target for sales call intelligence pipelines (Zoom is the dominant platform for B2B sales calls in North America).
- **API Documentation:** https://developers.zoom.us/docs/api/meetings/ · https://developers.zoom.us/docs/api/
- **SDKs/Libraries:** Zoom Meeting SDK (https://developers.zoom.us/docs/meeting-sdk/); Zoom API methods reference (https://developers.zoom.us/docs/api/rest/reference/zoom-api/methods/)
- **Developer Guide:** https://developers.zoom.us/docs/api/using-zoom-apis/
- **Standards:** REST/JSON; OpenAPI-documented endpoints
- **Authentication:** OAuth 2.0 (recommended) or JWT (deprecated); Server-to-Server OAuth for backend access to cloud recordings
- **Note:** Cloud Recording transcripts are produced only when the host explicitly enables Zoom Cloud Recording (not local recording). Transcripts delivered in VTT format.

---

### Microsoft Graph API — Teams Transcripts & Recordings

- **Description:** Microsoft Graph provides REST APIs to access Teams meeting recordings and transcripts post-meeting. Key for enterprises running on Microsoft 365 / Teams as their primary conferencing stack.
- **API Documentation:** https://learn.microsoft.com/en-us/microsoftteams/platform/graph-api/meeting-transcripts/overview-transcripts
- **SDKs/Libraries:** Microsoft Graph SDKs for Python, JavaScript, Java, Go, .NET (https://learn.microsoft.com/en-us/graph/sdks/sdks-overview)
- **Developer Guide:** https://learn.microsoft.com/en-us/graph/api/calltranscript-get?view=graph-rest-1.0
- **Standards:** REST/JSON; OpenAPI-documented via Graph Explorer; transcript content delivered as `.vtt` files; recordings as `.mp4`
- **Authentication:** OAuth 2.0 via Microsoft Entra ID (Azure AD); requires either organisation-wide application permissions or RSC (Resource-Specific Consent) per meeting
- **Note:** Transcript and recording APIs are metered (pay-per-use for high volume). Transcription must be enabled by the meeting organiser.

---

### Salesforce REST API

- **Description:** The primary CRM target for automated call data write-back. Supports reading and writing to Contacts, Leads, Opportunities, Tasks, and custom objects — enabling zero-touch CRM hygiene from call transcripts.
- **API Documentation:** https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/ · https://resources.docs.salesforce.com/latest/latest/en-us/sfdc/pdf/api_rest.pdf (v66.0, Spring '26)
- **SDKs/Libraries:** Salesforce DX CLI; simple-salesforce (Python); jsforce (Node.js); official Java, .NET SDKs
- **Developer Guide:** https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/quickstart_oauth.htm
- **Standards:** REST/JSON; OpenAPI 3.0 descriptions available via Salesforce API Explorer
- **Authentication:** OAuth 2.0 via Connected Apps or External Client Apps (Spring '26+). Supports Authorization Code, Client Credentials, and JWT Bearer flows. My Domain–specific OAuth endpoints required (`https://<myorg>.my.salesforce.com/services/oauth2/...`).

---

### HubSpot CRM API

- **Description:** CRM write-back target for mid-market and SMB teams. Supports Contacts, Companies, Deals, Engagements (calls, notes, emails), and custom properties — all writable via REST.
- **API Documentation:** https://developers.hubspot.com/docs
- **SDKs/Libraries:** Official Python, Node.js, PHP, Ruby, Java SDKs (https://developers.hubspot.com/); Postman collection (https://www.postman.com/hubspot/)
- **Developer Guide:** https://developers.hubspot.com/docs/getting-started/overview
- **Standards:** REST/JSON; OpenAPI specifications available per API category; Engagement APIs allow logging calls with transcript text, duration, and participants
- **Authentication:** OAuth 2.0 or Private App tokens (API key authentication deprecated in 2022–2023; all integrations should use OAuth 2.0 or Private Apps)

---

## Notes

**Emerging: Real-Time AI Overlay Standards**
No established standard yet governs "live whisper coaching" overlays — the in-call AI suggestions market is pre-standard. Implementations currently rely on platform-specific SDKs (Zoom Meeting SDK, Teams Meeting Apps) combined with WebSocket-based LLM streaming. Watch for emerging W3C or IETF activity in the real-time AI overlay space.

**Consent Routing Complexity**
Call recording consent laws vary by jurisdiction at the state, national, and regional level. As of 2026, no single international standard governs multi-party consent for AI-processed call recordings. Products operating globally must maintain a jurisdiction lookup table and dynamically trigger the appropriate disclosure flow before recording begins.

**Transcript Format Fragmentation**
The transcript ecosystem remains fragmented: Zoom delivers VTT, Teams delivers VTT, AssemblyAI delivers JSON/SRT/VTT, Whisper delivers JSON/SRT/VTT/text. Any internal data model should normalise all sources into a canonical format (recommended: JSON with per-utterance speaker labels and timestamps) before processing, then emit VTT and SRT as export formats.

**SOC 2 and ISO 27001 as GTM Gates**
Enterprise sales deals consistently require SOC 2 Type II reports and ISO 27001 certificates at the security review stage, before the product reaches technical evaluation. An open-source tool targeting enterprise adoption should ship deployment documentation that maps to SOC 2 control categories and ISO 27001 Annex A controls.
