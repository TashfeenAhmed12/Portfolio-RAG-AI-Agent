# Architecture

This page explains the system in plain language.

## High-Level Flow

1. Portfolio content is turned into a structured library of project and experience summaries.
2. That library is converted into a search-friendly format.
3. The search data is stored in a vector index.
4. A user submits a project brief through the portfolio website.
5. The user brief is converted into the same format.
6. The system finds the closest matching entries.
7. A ranking step improves the match quality.
8. An LLM writes a short final answer using only that retrieved context.
9. The website displays the fit assessment and relevant GitHub links.

## Main Components

### Portfolio context layer

The assistant relies on a curated portfolio library containing:

- project summaries
- subproject descriptions
- anonymized experience statements
- service-area summaries
- tags and skill signals

### Embedding layer

Each portfolio entry is converted into a format that helps the system find similar meaning, even when the user does not use the exact same wording.

### Vector retrieval layer

A vector index stores the portfolio entries and returns the closest matches for a given prompt.

### Reranking layer

The first search results are refined to improve quality for:

- short prompts
- synonym-heavy prompts
- mixed prompts that combine greetings and project requests
- cases where exact repo titles do not mirror the user wording

### Generation layer

The final answer is produced by an LLM that receives:

- the user brief
- the retrieved portfolio context
- fit and privacy instructions

The model is constrained to produce short, professional, portfolio-safe responses.

## Guardrails

The assistant is intentionally narrow in scope.

It is designed to:

- respond to project-fit questions
- handle capability questions briefly
- avoid sharing personal details
- refuse harmful or unrelated prompts
- avoid inventing projects or unsupported claims

## Why RAG Was Chosen

RAG is a better fit than a general chatbot for this use case because:

- it grounds answers in real portfolio evidence
- it reduces made-up claims
- it improves project recommendation quality
- it keeps the assistant aligned with a narrow public-facing purpose

## Platform Choice

The project is designed around Cloudflare-native services:

- serverless request handling
- managed AI inference
- vector search
- lightweight deployment for a portfolio site

This makes it a practical example of deploying an AI assistant for a real web product rather than only building a local demo.
