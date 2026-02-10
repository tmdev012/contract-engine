# Contract Engine

> AI-powered document generation — contracts, proposals, NDAs, invoices, SLAs. Jinja2 templates + AI clause enhancement + PII anonymization + PDF export.

[![Python](https://img.shields.io/badge/python-3.10+-blue)]()
[![Jinja2](https://img.shields.io/badge/Jinja2-templates-green)]()
[![WeasyPrint](https://img.shields.io/badge/PDF-WeasyPrint-orange)]()

## Pipeline

```
Template (Jinja2)     Variables (JSON)     AI Enhancement (Ollama)
      │                    │                      │
      └────────────┬───────┘                      │
                   ▼                               │
            ┌─────────────┐                        │
            │   Renderer  │◀───────────────────────┘
            └──────┬──────┘
                   ▼
            ┌─────────────┐
            │ Anonymizer  │  ← PII detection + redaction
            └──────┬──────┘
                   ▼
            ┌─────────────┐
            │  PDF Export  │  ← WeasyPrint HTML→PDF
            └──────┬──────┘
                   ▼
            ┌─────────────┐
            │ Audit Trail  │  ← SQLite: who, when, what, version
            └─────────────┘
```

## Template Library

| Template | Use Case | Variables |
|----------|----------|-----------|
| NDA | Non-disclosure agreement | parties, date, duration, jurisdiction |
| Consulting Agreement | Service contracts | scope, rate, payment terms, deliverables |
| Invoice | Billing | line items, tax, payment details |
| Proposal | Project proposals | scope, timeline, budget, team |
| SLA | Service level agreements | uptime %, response times, penalties |

## Revenue

Legal/medical/finance clients pay **R2,500-5,000 per template set** + **R1,000/month support**. White-label for law firms at R10,000 setup.

---
*MIT License*
