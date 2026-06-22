# Product Requirements Document (PRD): BenefitBridge AI

**Project Name:** BenefitBridge AI  
**Tagline:** Autonomous Government Benefits Navigator for Citizens  
**Status:** Draft / Hackathon Proposal  
**Target Event:** HiDevs × Mastra Hackathon  

---

## 1. Executive Summary
BenefitBridge AI is an autonomous, multi-agent platform designed to bridge the gap between citizens and the government benefits they are entitled to. Unlike traditional search-based portals, BenefitBridge AI utilizes a sophisticated agent swarm (powered by **Mastra**), a high-performance vector memory (powered by **Qdrant**), and a robust safety and compliance layer (powered by **Enkrypt AI**). The system proactively identifies eligibility, detects missed historical benefits, and guides users through complex application processes, ensuring that no citizen is left behind due to information fragmentation or administrative complexity.

## 2. Problem Statement
Millions of citizens fail to access government benefits, scholarships, welfare programs, and healthcare assistance because information is fragmented across thousands of disconnected portals. Eligibility rules are often written in dense legal language, and application processes are notoriously complex. Consequently, eligible individuals either never discover relevant schemes or abandon applications due to document errors and a lack of personalized guidance.

## 3. Existing Challenges
*   **Information Fragmentation:** Data is scattered across local, state, and federal websites.
*   **Cognitive Overload:** Complex eligibility criteria are difficult for the average citizen to interpret.
*   **Reactive Nature:** Current systems require the user to know what they are looking for before they start searching.
*   **High Friction:** Missing documentation and lack of step-by-step guidance lead to high application abandonment rates.
*   **Trust & Accuracy:** Concerns over data privacy and the risk of misinformation in automated systems.

## 4. Why Existing Solutions Fall Short

| Feature | Traditional Government Portals | BenefitBridge AI |
| :--- | :--- | :--- |
| **Discovery** | Users must manually search across multiple websites | Unified intelligent discovery across all schemes |
| **Eligibility** | Citizens must interpret complex rules themselves | AI-powered autonomous eligibility analysis |
| **Personalization** | No personalized recommendations | Tailored benefit matching based on profile |
| **Memory** | No long-term memory of citizen history | Persistent citizen memory using Qdrant |
| **Proactivity** | No proactive notifications | Life-event triggered recommendations |
| **Guidance** | Limited guidance during application process | Step-by-step application roadmap |
| **Recovery** | No identification of missed opportunities | Missed Benefits Detection Engine |
| **Reasoning** | Static information retrieval | Autonomous multi-agent reasoning |
| **Safety** | No safety validation of recommendations | Enkrypt AI validation and compliance checks |

**Analysis:** Existing systems are primarily search-based and reactive, placing the burden of discovery on the citizen. BenefitBridge AI shifts this paradigm by acting as a proactive, agent-driven advocate that continuously monitors opportunities and manages the lifecycle of benefit acquisition on behalf of the citizen.

## 5. Proposed Solution
BenefitBridge AI is an autonomous multi-agent system that helps citizens discover, understand, qualify for, and successfully apply to government schemes. By integrating **Mastra** for orchestration, **Qdrant** for semantic memory, and **Enkrypt AI** for safety, the platform provides a "set-and-forget" experience where the system works in the background to maximize a citizen's social and financial well-being.

## 6. Target Users / Stakeholders
*   **General Citizens:** Individuals seeking healthcare, education, or housing subsidies.
*   **Underserved Populations:** Low-income families and elderly citizens who may lack the digital literacy to navigate complex portals.
*   **Students:** Individuals looking for scholarships and educational grants.
*   **Government Agencies:** Stakeholders interested in increasing the utilization of social programs.

## 7. Functional Requirements

### 7.1 Core Features
*   **Personalized Discovery:** Matches citizen profiles against a global repository of schemes.
*   **Eligibility Analysis:** Deep-dives into legal requirements to determine qualification status.
*   **Missed Benefits Detection:** Scans historical data to find unclaimed past benefits.
*   **Document Readiness Verification:** Uses OCR and agents to check if uploaded documents meet scheme requirements.
*   **Application Roadmap Generation:** Provides a chronological checklist for the application process.
*   **Life-Event Triggers:** Automatically re-evaluates eligibility when a user’s status changes (e.g., marriage, relocation).
*   **Impact Analytics:** Reports on the total financial value secured for the user.

### 7.2 Mastra Agent Swarm (Detailed Agent Architecture)
The system utilizes a specialized swarm of agents orchestrated by Mastra:
1.  **Citizen Profile Agent:** Manages and updates the user's digital twin.
2.  **Eligibility Analysis Agent:** Interprets complex policy text.
3.  **Missed Benefits Detection Agent:** Analyzes historical eligibility gaps.
4.  **Benefit Discovery Agent:** Scours the Knowledge Graph for new opportunities.
5.  **Document Verification Agent:** Validates the presence and accuracy of required files.
6.  **Application Roadmap Agent:** Generates step-by-step execution plans.
7.  **Life Event Trigger Agent:** Monitors profile changes for new eligibility windows.
8.  **Notification Agent:** Handles multi-channel alerts and follow-ups.
9.  **Impact Analytics Agent:** Calculates and visualizes the social/economic benefit.
10. **Agent Workflow Orchestrator:** The master agent managing inter-agent communication.

## 8. Non-Functional Requirements
*   **Performance:** Agent reasoning and RAG retrieval should occur in under 3 seconds.
*   **Scalability:** Support for millions of citizen profiles and scheme documents.
*   **Reliability:** 99.9% uptime for the monitoring and notification engine.
*   **Security:** End-to-end encryption for sensitive citizen documents (PII).
*   **Compliance:** Adherence to GDPR/CCPA and government data handling standards.

## 9. System Architecture Overview
The architecture is built on a three-pillar foundation:
1.  **Orchestration (Mastra):** Manages the logic, state, and communication between the 10 specialized agents.
2.  **Memory & Knowledge (Qdrant):** Stores the Government Knowledge Graph and long-term citizen memory using vector embeddings for semantic retrieval (RAG).
3.  **Safety & Trust (Enkrypt AI):** Acts as a firewall for the LLM, detecting hallucinations, bias, and ensuring all recommendations are compliant with current laws.

## 10. Tech Stack
*   **Agent Framework:** Mastra (Workflow orchestration, agent state management).
*   **Vector Database:** Qdrant (Knowledge Graph, Citizen Memory, Semantic Search).
*   **Safety Layer:** Enkrypt AI (Hallucination detection, Risk scoring, Compliance).
*   **LLMs:** GPT-4o or Claude 3.5 Sonnet (Reasoning engines).
*   **Backend:** Node.js / Python.
*   **Frontend:** React / Next.js.

## 11. Data Requirements
*   **Government Scheme Repository:** Ingested and embedded into Qdrant.
*   **Citizen Profiles:** Structured data (income, age, location) and unstructured data (history).
*   **Document Store:** Secure storage for identity and eligibility documents.
*   **Embedding Pipeline:** Continuous ingestion of new government circulars and policy updates.

## 12. Innovation and Differentiators

### 12.1 Proactive Citizen Opportunity Intelligence
Unlike traditional portals that require active searching, BenefitBridge AI continuously monitors citizen profiles and policy updates.
*   **Turning 18:** Automatically identifies new voting rights, adult education grants, and independent welfare.
*   **Higher Education:** Triggers scholarship discovery the moment a student is accepted.
*   **Employment Changes:** Detects job loss or income drops to immediately suggest unemployment benefits or food assistance.
*   **Relocation:** Instantly maps the user to state-specific benefits in their new location.

### 12.2 Missed Benefits Recovery Engine
The system analyzes historical eligibility to identify "lost" money.
*   **Unclaimed Credits:** Detects tax credits or rebates the user qualified for but didn't claim.
*   **Retroactive Benefits:** Identifies schemes that allow for back-dated applications.
*   **Financial Impact Estimation:** Provides a dollar value of missed opportunities to motivate user action.

**Summary:** The combination of **Mastra’s** multi-agent orchestration, **Qdrant’s** long-term memory, and **Enkrypt AI’s** safety validation creates a next-generation platform that functions as an autonomous advocate rather than a simple chatbot.

## 13. Success Metrics (KPIs)
*   **Utilization Rate:** Percentage of eligible benefits successfully claimed by users.
*   **Application Completion Rate:** Reduction in abandoned applications.
*   **Accuracy Score:** Percentage of recommendations validated as correct by Enkrypt AI.
*   **Financial Impact:** Total currency value of benefits secured for the citizen population.
*   **Time-to-Discovery:** Reduction in time between a life event and benefit discovery.

## 14. Timeline & Milestones
*   **Phase 1 (Week 1):** Knowledge Graph ingestion into Qdrant and Mastra agent setup.
*   **Phase 2 (Week 2):** Integration of Enkrypt AI for safety and hallucination testing.
*   **Phase 3 (Week 3):** Development of the Life-Event Trigger and Missed Benefits engines.
*   **Phase 4 (Week 4):** UI/UX development and end-to-end workflow testing.

## 15. Open Questions & Risks
*   **Data Access:** How to maintain a real-time feed of government policy changes?
*   **Privacy:** Ensuring PII is never used for training and is handled according to strict security protocols.
*   **Hallucination Risk:** While Enkrypt AI mitigates this, legal disclaimers are still necessary for AI-generated advice.