# AI Skills Library

![GitHub stars](https://img.shields.io/github/stars/ahjimomo/ai-skills-library?style=social)
![GitHub forks](https://img.shields.io/github/forks/ahjimomo/ai-skills-library?style=social)

A curated library of prompts and workflows designed for non-technical users — structured to be dropped into any AI tool and used immediately, without prompt engineering knowledge.

Each entry is built around a specific use case, includes plain-English guidance on when and how to use it, and comes with guardrails to help users catch mistakes before they act on the output.

---

## How to Use

**Option A — Claude users (via Skills)**
Download the `SKILL.md` file from the skill folder and place it in your Claude skills directory:
- Personal use: `~/.claude/skills/<skill-name>/SKILL.md`
- Project use: `.claude/skills/<skill-name>/SKILL.md` inside your project directory

**Option B — Any AI tool**
Open the `SKILL.md` file, copy the instruction block under **The Instruction**, and paste it into a new conversation in your preferred AI tool.

---

## Skills & Workflows

### Available Now

| Name | Category | Type | Description | Link |
|------|----------|------|-------------|------|
| Context Translator | Writing & Communication | Prompt | Translate any text into English and get a plain explanation of what it actually means — the words, the tone, and the intent behind them. | [View →](skills/context-translator/SKILL.md) |
| Meeting Notes Summariser | Synthesis & Insights | Prompt | Turn raw meeting notes or transcripts into a clean summary with decisions made, action items, owners, and a proposed agenda for the next meeting. | [View →](skills/meeting-notes-summariser/SKILL.md) |
| Project Kickoff Planner | Strategy & Planning | Prompt | Turn a project brief or rough idea into a structured kickoff plan covering objectives, scope, roles, milestones, risks, and domain-specific context. | [View →](skills/project-kickoff-planner/SKILL.md) |
| Research Briefing Generator | Inquiry & Research | Prompt | Get a structured briefing on any topic before starting a project — covering what is established, what is contested, open questions, risks, and a short reading list. | [View →](skills/research-briefing-generator/SKILL.md) |
| Data Interpretation Assistant | Technical Execution | Prompt | Describe a dataset or report in plain language and get a clear breakdown of what it shows, what it cannot tell you, and what questions to bring to your analyst. | [View →](skills/data-interpretation-assistant/SKILL.md) |
| SOP Builder | Interpersonal & Ops | Workflow | Build a structured, role-assigned standard operating procedure from a process description or reference materials — with gaps flagged and improvements suggested. | [View →](skills/sop-builder/SKILL.md) |

### In the Pipeline

| Name | Category | Type | Description |
|------|----------|------|-------------|
| Explain It Simply | Writing & Communication | Prompt | Break down any topic, concept, or document into a plain explanation suitable for a child or complete newcomer — no jargon, no assumed knowledge. |
| Travel Planner | Strategy & Planning | Workflow | Plan a trip end-to-end — itinerary, logistics, budget, and packing considerations — through a guided conversation that adapts to your travel style and constraints. |

---

## Structure

```
ai-skills-library/
└── skills/
    └── <skill-name>/
        └── SKILL.md    ← instruction, guidance, guardrails, and example output
```

Each `SKILL.md` follows a consistent format:

| Section | Purpose |
|---------|---------|
| When to Activate | Trigger phrases and conditions for Claude users |
| When to Use It | User-facing situations where the skill is relevant |
| What It Does | Plain-English description of the output |
| How to Use It | Step-by-step usage for Claude Skills and other AI tools |
| The Instruction | The full copy-paste prompt |
| Guardrails & Accuracy Checks | Built-in safeguards and a pre-action checklist |
| Example Output | A realistic worked example |

---

## About

Built and maintained by [Nicky Ng](https://github.com/ahjimomo). Part of a broader personal project exploring how non-technical users can get consistent, reliable results from AI tools without needing to understand prompt engineering.

Skills are designed to work with Claude but are tested to be tool-agnostic where possible.

---

## Licence

[MIT](LICENSE)