# Neomage Architecture

## Multimodal Clinical Intelligence Platform

This document provides a high-level overview of Neomage's public system architecture.

Neomage is designed as a modular Clinical AI platform that integrates fragmented healthcare data into a unified intelligence layer for clinician-in-the-loop decision support.

> **Note**
>
> This repository intentionally presents the public architecture only.
> Proprietary algorithms, production models, clinical datasets and commercial infrastructure are not included.

---

# System Overview

```
                      Physicians
                           │
                           ▼
               Clinical Dashboard / APIs
                           │
                      FastAPI Backend
                           │
      ┌──────────────┬──────────────┬──────────────┐
      ▼              ▼              ▼
 Clinical Data   Medical Imaging   Physiological Data
 EHR • FHIR      MRI • CT • US     Biomarkers • Vitals
      └──────────────┬──────────────┘
                     ▼
         Clinical Intelligence Layer
                     │
                     ▼
 Patient Risk Intelligence & Decision Support
                     │
                     ▼
             PostgreSQL Database
```

---

# Platform Components

| Layer | Purpose |
|--------|---------|
| Clinical Data | Integrates structured healthcare information from multiple clinical sources. |
| AI Platform | Data engineering, feature generation, model training, validation and inference. |
| API Layer | FastAPI services exposing platform capabilities through REST APIs. |
| Clinical Intelligence | Patient risk intelligence and clinician decision support. |

---

# Engineering Principles

| Principle | Description |
|-----------|-------------|
| Modular | Independent components designed for scalability and maintainability. |
| Explainable | Supports clinicians rather than replacing clinical judgement. |
| Interoperable | Designed for FHIR-ready healthcare environments. |
| Reproducible | Engineering and ML workflows emphasise reproducibility. |
| Privacy-first | Designed with secure healthcare deployment in mind. |

---

# Technology Stack

| Layer | Technology |
|--------|------------|
| Language | Python 3.11 |
| Backend | FastAPI |
| AI / ML | PyTorch · Scikit-learn |
| Database | PostgreSQL · SQLAlchemy |
| APIs | REST |
| Infrastructure | Docker |
| Healthcare | FHIR-ready architecture |

---

# Repository Scope

| Included | Not Included |
|----------|--------------|
| Public architecture | Proprietary source code |
| Engineering approach | Production machine learning models |
| Technology stack | Clinical datasets |
| Public documentation | Commercial integrations |
| Product direction | Internal infrastructure |

---

© Neomage Ltd.