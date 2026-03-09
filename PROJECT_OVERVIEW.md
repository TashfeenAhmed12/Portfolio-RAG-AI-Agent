# Project Overview

## Summary

Portfolio RAG Assistant is a public-facing AI feature built for a technical portfolio website. A visitor can describe a project or problem, and the assistant returns a short fit assessment based on relevant portfolio context.

The project is designed to answer one narrow question well:

`Does this project look like a fit, and what portfolio work best supports that answer?`

## Problem

Traditional portfolio sites often require a recruiter or hiring manager to manually browse projects and infer relevance. That is slow, especially when the visitor has a specific problem in mind but does not know which project best represents the required skill set.

## Solution

This assistant adds a retrieval-based layer on top of portfolio content:

1. The visitor describes a project brief.
2. The system retrieves the closest relevant portfolio entries.
3. The model generates a concise answer grounded in that retrieved context.
4. The interface surfaces the most relevant GitHub work when appropriate.

## Design Goals

- keep answers concise
- make results useful for recruiters
- avoid generic chatbot behavior
- avoid exposing personal information
- support semantic matching rather than exact keyword-only matching
- handle vague, mixed, or imperfect user prompts gracefully

## What Makes It Interesting

- practical RAG use case tied to a real website
- vector retrieval over portfolio experience and project summaries
- hybrid reranking rather than naive top-k retrieval alone
- safety and privacy constraints designed for a public portfolio
- clear user value: faster project discovery and relevance matching

## Outcome

The project turns a static portfolio into an interactive discovery experience. Instead of forcing users to guess which project matters, the assistant helps connect project intent to relevant work in a controlled way.
