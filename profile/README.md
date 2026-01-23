# ReviewScope – AI-Powered Code Review Automation

ReviewScope is an intelligent PR review platform that combines **static analysis**, **semantic context**, and **AI reasoning** to provide comprehensive, fast code reviews on GitHub.

<img width="1884" height="855" alt="Screenshot 2026-01-18 231855" src="https://github.com/user-attachments/assets/7734e009-b8de-48c6-94e7-3d9565c3c023" />


## Overview

ReviewScope analyzes pull requests end-to-end, evaluating code quality, security, performance, and maintainability. It runs directly on your own API keys, so you control costs and data.

**Key Capabilities:**
- 🔍 **Static Analysis** – AST-based rule detection (no LLM required, always free)
- 🧠 **AI-Powered Reviews** – Complexity-aware routing between fast (Gemini) and accurate (GPT-4) models
- 📚 **Semantic RAG** – Retrieves relevant code context from your repository's history
- ⚡ **Smart Batching** – Handles large PRs by intelligently chunking files
- 🎯 **Rule Validation** – LLM classifies static findings (valid/false-positive/contextual)
- 💰 **BYO API Keys** – Transparent pricing, you pay only for what you use

## Technology Stack

**Frontend & Dashboard:**
- Next.js 16 (Turbopack)
- TailwindCSS + shadcn/ui
- NextAuth (GitHub OAuth)

**Backend & Processing:**
- Node.js Worker (background review jobs)
- Drizzle ORM + PostgreSQL
- Redis (caching & rate limiting)

**AI & LLM:**
- Gemini 2.5 (fast, low-cost reviews)
- GPT-4 (complex PRs, high accuracy)
- Context Engine (RAG + chunking)

**Integration:**
- GitHub Webhooks (real-time PR events)
- DODO Payments (billing integration)
- GitHub API (PR data, code retrieval)
