# Uditha Manohara Prasad

**Software Engineer (BSc Hons, UG) · AI Engineering · Founder & CEO, [Neziora](https://neziora.com)**
Colombo, Sri Lanka · [ORCID 0009-0003-1178-5309](https://orcid.org/0009-0003-1178-5309) · [udithamanohara.dev](https://udithamanohara.dev)

I build reliable software and AI systems that run where the data lives. My research and engineering focus is **making small, locally deployed language models dependable enough for production data workflows**, using deterministic constraints rather than larger models or cloud APIs.

---

## Research

### EDIP: Edge Deterministic Ingestion Protocol

*Closed-Loop Relational Constraint Reflection for Autonomous Document Ingestion on Quantized Edge Models*

[![Whitepaper DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23995414.svg)](https://doi.org/10.5281/zenodo.23995414)
[![Software DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23995358.svg)](https://doi.org/10.5281/zenodo.23995358)

Organizations under data-residency rules cannot send documents to commercial cloud AI, and the 1B–3B parameter models that run on a standard workstation frequently emit invalid foreign keys, malformed numerics and missing fields. EDIP treats the relational database as the supervisor. A rejected write is caught as a native `IntegrityError`, rolled back, and the exact error plus the valid candidate keys are fed back to the model in a bounded retry loop. Records that cannot be resolved go to a dead-letter queue for human review.

**Design**
- Fully offline, CPU-only, no cloud calls
- SQLite constraints (PK, FK, CHECK, UNIQUE) as the validation gate
- Write-Ahead Logging for concurrent read/write
- Dynamic schema introspection, so no hardcoded prompts
- Atomic multi-table transactions with a three-folder quarantine routing and audit table

**Evaluation** (Intel Core i3-10100, 12 GB RAM, Llama-3.2-1B 4-bit via Ollama): five adversarial conditions: deprecated keys, unstructured prose amounts, prompt injection, duplicate filings and unregistered entities. Invalid records were contained in every case; recoverable failures self-corrected within two attempts; unresolvable ones were quarantined with a full audit trail.

**Stated limits:** constraints guarantee structural validity, not factual truth; a CPU-only retry sequence costs roughly 8–10 s per document; the reference schema is two levels deep.

| Artifact | Link |
|---|---|
| White paper | [doi.org/10.5281/zenodo.23995414](https://doi.org/10.5281/zenodo.23995414) |
| Engine (software, MIT) | [doi.org/10.5281/zenodo.23995358](https://doi.org/10.5281/zenodo.23995358) |
| Package | `pip install edip` ([PyPI](https://pypi.org/project/edip/)) |
| Source | [github.com/uditha-manohara/edip](https://github.com/uditha-manohara/edip) |

<details>
<summary>Cite</summary>

```bibtex
@misc{prasad2026edip,
  author    = {Prasad, Uditha Manohara},
  title     = {Edge Deterministic Ingestion Protocol (EDIP): Closed-Loop Relational
               Constraint Reflection for Autonomous Document Ingestion on Quantized Edge Models},
  year      = {2026},
  publisher = {Zenodo},
  doi       = {10.5281/zenodo.23995414}
}
```

</details>

---

## Engineering Focus

| Area | Work |
|---|---|
| **Applied AI** | Constraint-supervised small-model pipelines, error-feedback loops, LLM-assisted features (AI quiz generation), agent-callable tool design |
| **Local-first & privacy** | Client-side processing with WebAssembly and Web Crypto, zero-retention architectures, offline computation |
| **Architecture** | Row Level Security, zero-database edge control planes, HMAC-signed administration, idempotent and transactional workflows |
| **Full-stack delivery** | Dashboards, portals, authentication, PDF and document engines, deployment |

**Stack:** Python · JavaScript · TypeScript · Java · PHP · SQL (SQLite, MySQL) · React · Node.js · Electron · Tailwind · Supabase · Firebase · Netlify · Vercel · Ollama · Linux

---

## Neziora

[Neziora](https://neziora.com) is an AI-engineering technology brand building dependable software, automated intelligence pipelines and private client-native computing.

- **[Tools Hub](https://neziora.com/tools):** 31 free utilities that run entirely in the browser (documents, PDF, data, security, regional tools)
- **Ceylon GridPulse:** 2026 CEB/LECO tariff and solar net-metering engine, fully offline
- **Ceylon PayGuard & LankaQR:** CBSL EMVCo-compliant LankaQR, cheque writer and in-memory invoicing
- **Edge Control Deck:** zero-database administration layer with signed controls
- **[Research Forum](https://neziora.com/forum)**

## Selected Products

| Product | Description |
|---|---|
| [Neziora LeadFlow](https://neziora-leadflow.netlify.app/) | Lead, quotation and job management with private workspaces and Supabase RLS |
| [SecureShield](https://shield-platform.web.app/) | Privacy and digital-safety platform *(in development)* |
| [MindSprint](https://mindsprintlk.vercel.app/) | Study-focus platform with AI quiz generation |
| [Crestline Graphics](https://crestlinegraphics.com/) | Agency web system with client portal |
| [UMP Singlish](https://github.com/uditha-manohara/ump-singlish) | Singlish → Sinhala Unicode converter |
| [JustReceipt Pro](https://github.com/uditha-manohara/invoice-generator) | Secure receipt generator |

## Education

- **BSc (Hons) Software Engineering**, Birmingham City University, delivered by the Java Institute for Advanced Technology
- Harvard **CS50x** · University of Helsinki **Java Programming I & II**

---

## Contact

For software engineering, AI systems and research collaboration.

| | Personal | Neziora |
|---|---|---|
| **Email** | [udithamprasad@gmail.com](mailto:udithamprasad@gmail.com) | via [neziora.com](https://neziora.com) |
| **WhatsApp** | [+94 76 182 3815](https://wa.me/94761823815) | [+94 72 654 5635](https://wa.me/94726545635) |
| **LinkedIn** | [uditha-manohara](https://www.linkedin.com/in/uditha-manohara/) | [company/neziora](https://www.linkedin.com/company/neziora) |
| **X** | [@uditha_manohara](https://x.com/uditha_manohara) | [@Neziora](https://x.com/Neziora) |
| **Instagram** | [@uditha.manohara](https://www.instagram.com/uditha.manohara/) | [@nezioraofficial](https://www.instagram.com/nezioraofficial/) |
| **Facebook** | [udithamprasad](https://www.facebook.com/udithamprasad/) | [neziora](https://www.facebook.com/neziora/) |
| **TikTok** | [@udithamprasad](https://www.tiktok.com/@udithamprasad) | [@neziora](https://www.tiktok.com/@neziora) |
