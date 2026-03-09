# Portfolio AI Agent

Live website: [tashfeenahmed.org](https://tashfeenahmed.org)

RAG-based AI agent for a portfolio website that reads a project brief, checks whether it is a fit, and points to the most relevant work.

## Overview

Portfolio AI Agent is a focused AI feature built for a portfolio website. Instead of acting like a general chatbot, it looks at a user's project brief, checks whether the work is a fit, surfaces the closest GitHub projects, and replies with a short, privacy-safe answer.

This repository is intentionally documentation-only. It describes the project without exposing implementation code, deployment secrets, or personal information.

## What It Does

- accepts a project brief from a website visitor
- retrieves the closest relevant portfolio context
- maps the request to experience areas and GitHub projects
- returns a concise fit assessment
- keeps responses controlled, recruiter-friendly, and privacy-safe
- handles vague prompts, mixed greeting-plus-project prompts, and unrelated requests

## Why This Project Matters

This project shows how AI can make a portfolio more useful:

- it helps recruiters and hiring managers find relevant work faster
- it connects vague project briefs to concrete portfolio examples
- it keeps answers short, controlled, and easy to read
- it avoids exposing personal information
- it is built for a real website, not just a demo

## Core Features

### RAG-based retrieval

The assistant looks up relevant portfolio context before answering, so the response is grounded in real project and experience summaries.

### Hybrid ranking

The matching logic is designed to work even when the user writes a short prompt, uses different wording, or mixes a greeting with a project request.

### Guardrails

The assistant stays focused on portfolio-related questions and avoids exposing private details or answering harmful requests.

### Concise response design

Answers are intentionally short so they are easy to read inside a recruiter-facing website.

## Example Use Cases

- `I need a Power BI dashboard for KPI reporting`
- `We need causal inference for campaign impact`
- `I want to build data engineering pipelines`
- `We want a healthcare chatbot`
- `I need an NLP model for text classification`

## Stack

- Cloudflare Pages Functions
- Cloudflare Workers AI
- Cloudflare Vectorize
- JavaScript
- Retrieval-Augmented Generation (RAG)
- Prompt guardrails and response cleanup

## Repository Contents

- [PROJECT_OVERVIEW.md](./PROJECT_OVERVIEW.md)
- [ARCHITECTURE.md](./ARCHITECTURE.md)
- [SCREENSHOT_NOTES.md](./SCREENSHOT_NOTES.md)
- [WEBSITE_COPY.md](./WEBSITE_COPY.md)

## Notes

- This repo intentionally excludes implementation code.
- This repo intentionally excludes personal contact details, employer details, and deployment secrets.
- The goal is to explain the project clearly to recruiters, hiring managers, and non-technical readers.
