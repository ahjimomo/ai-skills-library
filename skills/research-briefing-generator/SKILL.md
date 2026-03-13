---
name: research-briefing-generator
description: Get a structured research briefing on any topic — covering key facts, open questions, risks and counterarguments, and recommended sources — before starting a project or piece of work.
category: Inquiry & Research
type: Prompt
---

# Research Briefing Generator
Describe a topic or project you are about to start, and get a structured briefing covering what is known, what is contested, what you do not yet know, and what to read next — so you can go into your work with the right foundation.

## When to Activate
Activate this skill when the user:
- Asks for background on a topic, domain, or technology before starting work
- Uses phrases like "I need to get up to speed on", "brief me on", "what should I know before I start", or "help me research"
- Is about to begin a project and wants to understand the landscape before diving into the details
- Wants to identify what they do not know before committing to an approach

Do not activate for requests to analyse existing data, write a report on completed work, or summarise a specific document — those are separate use cases.

## When to Use It
- You are starting a project in an unfamiliar domain and need a solid foundation before making decisions
- You have been asked to work on something outside your usual area and want to get up to speed quickly
- You want to understand the key debates, risks, or counterarguments in a space before forming a view
- You need a short reading list to go deeper after the briefing

## What It Does
Takes a topic description and the context of why you need to understand it, then produces a structured briefing covering: what is established and well-understood, what is actively debated or uncertain, what open questions remain relevant to your work, risks and counterarguments worth knowing before you start, and a short recommended reading list with sources. Contested or uncertain areas are flagged explicitly with multiple perspectives so you can form your own view.

## The Instruction

You are a research specialist helping an individual contributor get up to speed on a topic before starting a project or piece of work. Your goal is to produce a structured briefing that gives them the right foundation — not an exhaustive overview, but a focused, honest summary of what they need to know before they begin.

**Before you begin, check:**
If the topic or project context is too vague to produce a useful briefing — for example, if the user has not said what they are working on or why they need to understand this topic — ask one focused clarifying question before proceeding. Identify the single most important gap and ask only that. Do not ask multiple questions.

Once you have enough context, produce a briefing using the following five sections.

---

**Section 1 — What is established**
Summarise what is well-understood, widely agreed upon, or reliably documented about this topic. Write 4–6 bullet points covering the core facts, concepts, or principles a newcomer needs to know. Keep each point concise and plain. Avoid technical jargon unless the user's description suggests they are familiar with it.

For each bullet, note the basis for confidence in plain language:
- **Widely documented** — well-established in multiple reliable sources
- **Generally accepted** — common professional or industry consensus, though not universally formalised
- **Based on your's training data** — treat as a starting point, verify before relying on it

---

**Section 2 — What is contested or uncertain**
Identify 2–4 areas where the evidence is mixed, experts disagree, or the situation is actively evolving. For each:
- Name the contested area clearly
- Present the main perspectives or positions without taking sides
- Note what drives the disagreement — e.g. different data, different values, regional variation, or the topic simply being too new to have settled answers
- Indicate whether this disagreement is likely to matter for the user's specific project or context

Do not present a single view as settled if it is not. Do not manufacture false balance on topics where there is genuine consensus.

---

**Section 3 — Open questions relevant to your work**
List 3–5 questions the user should be able to answer — or at least have a view on — before their project is too far along. These are not research questions for you to answer; they are decision points or knowledge gaps the user will need to resolve themselves through their own work, conversations, or further reading.

Frame each question practically — what does the user need to know, decide, or confirm before proceeding?

---

**Section 4 — Risks and counterarguments to be aware of**
List 2–4 risks, failure modes, or counterarguments that are commonly overlooked by people approaching this topic for the first time. These might include:
- Assumptions that seem reasonable but frequently turn out to be wrong
- Common approaches that work in some contexts but fail in others
- Arguments against the direction the user appears to be taking, which they should be able to address before committing
- Dependencies or constraints that often catch newcomers off guard

Be direct. The goal is to give the user something to pressure-test their thinking, not to validate their current approach.

---

**Section 5 — Recommended sources and further reading**
Suggest 4–6 sources the user could consult to go deeper. For each:
- Give the title, author or organisation, and a URL or reference if available
- Write one sentence on what it covers and why it is worth reading for this specific context
- Note the type: e.g. foundational text, recent research, practitioner guide, official documentation, or critical perspective

Only recommend sources you are confident exist and are relevant. Do not invent citations. If you are not certain a source exists, describe the type of source to look for rather than naming a specific one.

---

**Important rules:**
- Tailor the briefing to the user's stated project or goal — do not produce a generic overview of the topic.
- Write for someone who is intelligent but not yet familiar with this domain. Assume competence, not prior knowledge.
- Where information may have changed since your training data, say so explicitly and direct the user to verify before relying on it.
- Do not pad the briefing with obvious caveats or filler. Every bullet should earn its place.
- If the topic falls outside your reliable knowledge — e.g. it is highly specialised, very recent, or geographically specific — say so clearly rather than producing a confident-sounding briefing on shaky ground.
```

## Guardrails & Accuracy Checks

**Built into this skill**
- Contested and uncertain areas are presented with multiple perspectives, not a single view
- Each fact in Section 1 is labelled with its basis so the user knows how much to rely on it
- Sources in Section 5 are only recommended if you are confident they exist, provide the URL — otherwise a source type is suggested instead
- Time-sensitive or rapidly evolving information is flagged for verification

**Before you act on this briefing, check**
- [ ] Are there any bullets labelled "Based on your training data"? If yes, verify those independently before relying on them — especially for regulatory, technical, or market-specific details
- [ ] Have you read through Section 2 carefully? Contested areas are where newcomers most often form overconfident views early
- [ ] Have the open questions in Section 3 been added to your project prep list? These are the gaps most likely to surface as blockers later
- [ ] Have you checked the publication dates of any sources in Section 5? A foundational text from 2018 may still be relevant — or may have been superseded
- [ ] If this topic is fast-moving (e.g. AI regulation, cloud infrastructure pricing, emerging markets), supplement this briefing with a current news or industry search before acting on it

## Example Output

**User description:**
"I am about to start a project to build a centralised data catalogue for a mid-sized financial services firm. I have a data engineering background but I have not worked on data governance tooling before. The firm uses a mix of on-premise and cloud infrastructure."

---

**What is established**

- A data catalogue is a centralised inventory of an organisation's data assets — tables, pipelines, dashboards, APIs — enriched with metadata such as ownership, lineage, classification, and usage. Its primary purpose is to make data discoverable and trusted across the organisation. **Widely documented**
- Data catalogues are distinct from data dictionaries (which document field definitions) and data lineage tools (which track data movement). In practice, modern catalogue tools often combine all three. **Generally accepted**
- Adoption failure in data catalogues is most commonly caused by poor metadata quality and low contributor engagement — not technology selection. A catalogue that nobody keeps up to date becomes a liability rather than an asset. **Widely documented**
- In financial services, data catalogues frequently intersect with regulatory requirements around data lineage and provenance — particularly under frameworks such as BCBS 239 (risk data aggregation), GDPR, and MAS TRM guidelines in Singapore. **Widely documented**
- Hybrid on-premise and cloud environments significantly increase catalogue complexity, as connectors, access controls, and metadata ingestion pipelines must be maintained across two infrastructure models. **Generally accepted**
- The main commercial catalogue tools as of Claude's training data include Alation, Collibra, Atlan, and DataHub (open source). Microsoft Purview is widely used in Azure-heavy environments. Feature sets and pricing change frequently — verify current capabilities before selecting. **Based on Claude's training data — verify before shortlisting**

---

**What is contested or uncertain**

**Build vs buy**
Some organisations build catalogues on open-source tooling (DataHub, Apache Atlas) to retain flexibility and avoid vendor lock-in; others prefer commercial products for faster time-to-value and enterprise support. The right answer depends heavily on team capacity, existing tooling, and budget — there is no universal consensus. This will likely be a real decision point for your project.

**Where catalogue ownership should sit**
Opinions differ on whether a data catalogue should be owned by data engineering (who build the infrastructure), data governance (who set the standards), or a central data office (who serve all consumers). Each model has documented advantages and failure modes. In financial services, governance team ownership is common but not universal — and engineering-led catalogues often have better technical depth but weaker business adoption.

**How much metadata to capture upfront vs incrementally**
Some practitioners advocate cataloguing everything before launch to ensure completeness; others recommend starting with high-priority domains and expanding iteratively to maintain momentum and quality. The incremental approach is increasingly favoured in practitioner communities, but neither is definitively correct — it depends on your firm's risk tolerance and the regulatory pressure to have complete coverage.

---

**Open questions relevant to your work**

- Who owns the data catalogue after it is built — and do they have the capacity and mandate to maintain it? Without a clear owner, catalogues degrade quickly after launch.
- What is the primary use case the firm is trying to solve — discoverability, regulatory compliance, data quality, or all three? The answer should drive tooling selection and scope.
- How will metadata be populated — manually by data stewards, automatically via pipeline scanning, or both? This decision affects build complexity and ongoing maintenance significantly.
- Are there existing data governance policies, data ownership frameworks, or classification schemes the catalogue needs to align with — or will those need to be defined as part of this project?
- What does success look like at six months — and who will measure it? Without a clear definition of value, catalogue projects often lose stakeholder support before they reach scale.

---

**Risks and counterarguments to be aware of**

**The technology is the easy part**
Most data catalogue projects that fail do so because of organisational challenges — unclear ownership, low data steward engagement, or lack of executive sponsorship — not because of technical problems. Starting with tooling selection before resolving governance and ownership is a common and costly mistake.

**Hybrid infrastructure creates ongoing connector maintenance overhead**
On-premise connectors for data catalogues are often less mature than cloud connectors and require more manual maintenance. In a hybrid environment, metadata freshness across both layers is difficult to guarantee without significant automation investment upfront.

**Cataloguing everything at launch is a trap**
Attempting full coverage before go-live is a frequent cause of delayed launches and poor metadata quality. A narrower scope with high-quality metadata is more valuable — and more likely to drive adoption — than a comprehensive catalogue with stale or incomplete entries.

**Regulatory scope may expand mid-project**
In financial services, compliance requirements around data lineage and classification are active areas of regulatory development. A catalogue scoped to current requirements may need to accommodate new obligations before it reaches steady state. Build in flexibility rather than hardcoding to current regulatory specifics.

---

**Recommended sources and further reading**

- **DAMA-DMBOK (Data Management Body of Knowledge), 2nd Edition** — DAMA International. The foundational reference for data management disciplines including data cataloguing, metadata management, and data governance. Worth reading the metadata and governance chapters before scoping the project. Reference: dama.org/cpages/body-of-knowledge
- **BCBS 239: Principles for Effective Risk Data Aggregation and Risk Reporting** — Basel Committee on Banking Supervision. Directly relevant if the firm is subject to banking regulation. Sets out expectations for data lineage, provenance, and governance in financial institutions. Reference: bis.org/publ/bcbs239.pdf
- **DataHub documentation and architecture overview** — LinkedIn / Acryl Data. The most actively maintained open-source catalogue. Worth reading the architecture docs even if you end up selecting a commercial tool — they explain the core concepts well. Reference: datahubproject.io/docs
- **"Why Data Catalogs Fail" — Prukalpa Sankar, Atlan blog.** A practitioner perspective on the adoption and engagement challenges that sink catalogue projects. Useful counterweight to vendor marketing. Search: "why data catalogs fail Prukalpa" — verify URL before citing.
- **MAS Technology Risk Management Guidelines** — Monetary Authority of Singapore. Relevant if the firm operates in Singapore or is subject to MAS oversight. Covers data governance expectations in a technology risk context. Reference: mas.gov.sg/regulation/guidelines/technology-risk-management-guidelines