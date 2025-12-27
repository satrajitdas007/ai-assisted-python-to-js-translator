# AI-Assisted Python to JavaScript Translator

This repository demonstrates an AI-assisted workflow for translating production-style Python business logic to clean, testable JavaScript. The project focuses on preserving behavior, edge cases, and readability while using LLMs as a translation and refactoring engine.

## Tech Stack

- Python (source language)
- Node.js / JavaScript (target language)
- Jest for unit testing
- GitHub Actions for CI

## Problem

Engineering teams often maintain similar logic in multiple languages (for example, a Python backend and a JavaScript frontend), which leads to duplication and drift. Manually keeping these implementations aligned is slow and error-prone.

## Solution

This project showcases how an AI-orchestrator can:

- Ingest existing Python code and docstrings.
- Generate equivalent JavaScript implementations.
- Automatically scaffold tests to validate behavioral parity.
- Iterate on translations based on failing tests and code review comments.

## AI-Assisted Workflow

1. **Code intake**
   - Paste the Python function and docstring into an LLM (ChatGPT / Gemini / Perplexity) with a structured system prompt.

2. **First-pass translation**
   - Ask the LLM to produce one JavaScript version as close as possible to the original behavior.

3. **Test generation**
   - Provide the original Python examples and ask the LLM to generate Jest tests.

4. **Automated feedback loop**
   - Run Jest tests locally or via GitHub Actions.
   - If tests fail, share the stack traces back to the LLM for patching.

5. **Documentation**
   - Ask the LLM to produce human-readable documentation.

## How to Run

```
npm install
npm test
node src/javascript_translated/calculator.js
```

## Role in My Portfolio

This project demonstrates my capability as an AI-assisted multi-language software integrator: I design the prompts and constraints, validate translation quality through tests, and manage the repository and documentation. AI tools handle the repetitive translation work under my supervision.
