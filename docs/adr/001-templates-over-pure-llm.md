# ADR-001: Templates with AI Enhancement vs Pure LLM Generation

## Status: Accepted | Date: 2026-02-10

## Decision
Use Jinja2 templates as the base, with AI enhancing specific clauses — NOT pure LLM-generated documents.

## Why
- Templates are reproducible and auditable (legal requirement)
- AI hallucination in legal docs = liability
- Templates + AI = best of both: structure + intelligence
- Version-controlled templates = full audit trail
