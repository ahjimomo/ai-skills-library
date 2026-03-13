---
name: context-translator
description: Translate any text or document into English, then explain what it actually means in context — including tone, intent, and cultural nuance.
category: Writing & Communication
type: Reusable Instruction
---

# Context Translator
Translate any text or document into English, then explain what it actually means — not just the words, but the intent behind them.

## When to Activate
- You have received an email, message, or document from an overseas colleague or partner and need to understand the full intent, not just the literal words
- You are reading foreign news, articles, or reports and want to understand the cultural or political context behind the story
- You are working across multilingual teams and need to quickly get up to speed on communications in another language
- You want a second opinion on a translation you have already received to check for accuracy or missed nuance
- You are preparing for a meeting or negotiation with counterparts from another country and want to understand the tone of prior communications

## What It Does
Takes any text or uploaded document in a foreign language and works through it in two steps. First, it produces a clean, natural English translation — faithful to the original without being robotic. Then it explains what the content actually means in context: the tone, the intent, any cultural references or assumptions, and anything that could easily be misread across cultures.

## How to Use It
1. Open a new Claude conversation at claude.ai
2. Paste the full instruction from the section below into the chat
3. Paste the text you want translated directly into the chat, or upload the file (Claude accepts PDFs, Word documents, and plain text)
4. If you need the output in a language other than English, say so at the start — for example: "Please translate into French instead"
5. Claude will return the translation first, followed by the contextual explanation

## The Instruction
Copy the full text below and paste it into a new Claude conversation.

```
You are a professional translator and cultural interpreter.

When I give you a text or upload a file, work through it in two steps:

**Step 1 — Translation**
Translate the full content into English. The translation should be accurate and natural — faithful to the original meaning, not a word-for-word literal conversion. Preserve the tone of the original where possible (formal, casual, urgent, diplomatic, and so on).

**Step 2 — Contextual Explanation**
After the translation, provide a structured explanation covering:

- **Tone and intent** — What is the author trying to communicate or achieve? What is the underlying message beyond the literal words?
- **Cultural context** — Are there references, expressions, idioms, or assumptions in the original that may not be obvious to an English-speaking reader? Explain them plainly.
- **What to watch out for** — Is there anything in this text that could easily be misread or misunderstood across cultures? Flag it clearly.

**Important rules:**
- If anything in the text is ambiguous or unclear even in the original language, flag it explicitly rather than guessing. Use the phrase "Flagged for review:" so it stands out.
- Do not invent cultural context that cannot be reasonably inferred from the text itself.
- If the text contains technical, legal, or regulatory language, note this and recommend that a subject matter expert reviews the translation before it is acted upon.
- If I specify a different target language at the start of our conversation, translate into that language instead of English and apply the same contextual explanation in that language.
```

## Guardrails & Accuracy Checks

**Built into this skill:**
- Claude will flag ambiguous or unclear parts explicitly using "Flagged for review:" rather than guessing
- Claude will not invent cultural context it cannot reasonably infer from the text provided
- Claude will flag technical, legal, or regulatory language and recommend expert review

**Before you act on the output, check:**
- [ ] Does the translation read naturally, or does it feel robotic or word-for-word?
- [ ] Are the cultural explanations grounded in the actual text, or do they feel like general assumptions?
- [ ] Did Claude flag anything as ambiguous? If yes, resolve those points before using the output
- [ ] Does the tone described in Step 2 match your instinct about the communication?
- [ ] If the content is formal — a contract, policy, legal notice, or regulatory document — has a native speaker or subject matter expert reviewed it before you act on it?

## Example Output

**Translation**

Thank you for your continued support of our partnership. We hope this message finds you well. We would like to take this opportunity to revisit the terms discussed at our last meeting, as some points require further alignment before we can proceed.

---

**Contextual Explanation**

- **Tone and intent:** The message is polite but carries an implicit signal of concern. The phrase "require further alignment" is diplomatic language for disagreement or unresolved issues. The author is raising a problem without stating it directly, which is common in formal business communications in many East Asian and Southeast Asian contexts.
- **Cultural context:** Opening with gratitude and a wellbeing check before raising an issue is a face-saving convention — it softens what follows and signals that the relationship is valued even though a concern is being raised.
- **What to watch out for:** Do not read this as a routine check-in. The intent is to reopen negotiation on specific terms. Responding without acknowledging the underlying concern may be read as dismissive.
