# Portfolio RAG Assistant

Cloudflare-based retrieval-augmented assistant that matches project briefs to relevant portfolio work and anonymized experience.

## Overview

Portfolio RAG Assistant is a focused AI assistant designed for a technical portfolio website. Instead of acting like a general chatbot, it evaluates whether a project brief aligns with relevant experience, surfaces the closest GitHub work, and responds with short, privacy-safe answers.

This repository is intentionally documentation-only. It describes the project without exposing implementation code, deployment secrets, or personal information.

## What It Does

- accepts a project brief from a website visitor
- retrieves the closest relevant portfolio context
- maps the request to experience areas and GitHub projects
- returns a concise fit assessment
- keeps responses controlled, recruiter-friendly, and privacy-safe
- handles vague prompts, mixed greeting-plus-project prompts, and unrelated requests

## Why This Project Matters

This project shows applied GenAI in a practical setting:

- retrieval-augmented generation for a real user workflow
- semantic matching between user intent and portfolio content
- production-minded prompt design and response constraints
- privacy guardrails for public-facing AI experiences
- Cloudflare-native deployment design using managed AI and vector search

## Core Features

### RAG-based retrieval

User prompts are matched against a structured portfolio knowledge base rather than answered from model memory alone.

### Hybrid ranking

Semantic retrieval is supported by lexical ranking and service-area signals to improve performance on short prompts, synonyms, and mixed phrasing.

### Guardrails

The assistant is constrained to portfolio-relevant questions and avoids exposing private details or responding to harmful requests.

### Concise response design

Answers are intentionally short so they work well inside a recruiter-facing website section.

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
- Retrieval-Augmented Generation
- Prompt guardrails and response normalization

## Repository Contents

- [PROJECT_OVERVIEW.md](./PROJECT_OVERVIEW.md)
- [ARCHITECTURE.md](./ARCHITECTURE.md)
- [SCREENSHOT_NOTES.md](./SCREENSHOT_NOTES.md)
- [WEBSITE_COPY.md](./WEBSITE_COPY.md)

## Notes

- This repo intentionally excludes implementation code.
- This repo intentionally excludes personal contact details, employer details, and deployment secrets.
- The goal is to present the project clearly to recruiters and reviewers.
