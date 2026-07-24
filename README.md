

# AI Portfolio Assistant

An AI-powered assistant for my personal portfolio website that answers questions **only** using my professional knowledge base.

Unlike a generic chatbot, this assistant is designed to retrieve information from a curated collection of documents—including resumes, project documentation, certifications, blogs, notes, and screenshots—and answer only from those sources.

If the requested information is not available in the knowledge base, the assistant explicitly states that it does not know instead of generating an answer.

---

## Why I Built This

Traditional portfolio websites are static.

Recruiters can read my experience but cannot interact with it.

This project transforms a portfolio into an AI-powered knowledge assistant that can answer questions like:

- What AI projects has Ankit built?
- What product domains has he worked in?
- Which technologies does he know?
- What certifications does he have?
- What was his role at Bajaj Finserv?

while refusing questions outside its knowledge.

Example:

**Q:** What is Ankit currently working on?

✅ Answers from portfolio.

**Q:** Who is the Prime Minister of India?

❌ "I couldn't find that information in Ankit's knowledge base."

---

## Features

- AI-powered conversational interface
- Knowledge-grounded responses
- Hallucination control
- Portfolio-specific assistant
- Markdown knowledge base
- Extensible architecture
- Cloudflare Worker backend
- Google Gemini integration
- Responsive web interface

---

## Architecture

```
                Portfolio Website
                       │
                       ▼
             Cloudflare Worker API
                       │
                       ▼
             Knowledge Base Loader
                       │
        ┌──────────────┼──────────────┐
        │              │              │
        ▼              ▼              ▼
   Resume.md     Projects.md     About.md
        │              │              │
        └──────────────┼──────────────┘
                       ▼
              Prompt Construction
                       ▼
                   Gemini API
                       ▼
                  AI Response
```

---

## Technology Stack

- HTML
- CSS
- JavaScript
- Cloudflare Workers
- Google Gemini API
- Markdown Knowledge Base

---

## Repository Structure

```
.
├── index.html
├── worker.js
├── knowledge/
│   ├── about.md
│   ├── experience.md
│   ├── projects.md
│   ├── skills.md
│   ├── certifications.md
│   └── blogs/
└── README.md
```

---

## Design Principles

This assistant follows four important rules.

### 1. Knowledge Grounding

Every answer must originate from the supplied knowledge base.

---

### 2. No Hallucinations

If information is unavailable, the assistant responds:

> I couldn't find that information in Ankit's knowledge base.

instead of making assumptions.

---

### 3. Portfolio Only

The assistant is intentionally restricted.

It does not answer general-purpose questions.

---

### 4. Expandable

The knowledge base can be extended by simply adding new files.

No prompt modification is required.

---

## Future Roadmap

### Phase 1

- Markdown knowledge base

### Phase 2

- PDF ingestion

### Phase 3

- DOCX support

### Phase 4

- Image & screenshot understanding

### Phase 5

- Semantic search using embeddings

### Phase 6

- Vector database powered Retrieval-Augmented Generation (RAG)

### Phase 7

- Multi-agent architecture

---

## Example Questions

- Tell me about Ankit.
- What AI projects has he built?
- What domains has he worked in?
- Which programming languages does he know?
- What certifications does he have?
- Summarize his experience.

---

## Disclaimer

This assistant is intentionally constrained to answer only from its knowledge base.

It is designed to demonstrate responsible AI practices, retrieval-based reasoning, and hallucination reduction rather than serve as a general-purpose chatbot.
