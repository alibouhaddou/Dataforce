<div align="center">

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f9/Salesforce.com_logo.svg/320px-Salesforce.com_logo.svg.png" alt="Salesforce" width="160"/>

# Dataforce — Capability Registry

![Framework](https://img.shields.io/badge/Framework-Dataforce-00A1E0?style=flat-square&logo=salesforce&logoColor=white)
![Maintained by](https://img.shields.io/badge/Maintained%20by-alibouhaddou-032D60?style=flat-square)
![Capabilities](https://img.shields.io/badge/Capabilities-1%20Complete-1B96FF?style=flat-square)

> Customer-facing, multi-persona enablement content for Salesforce Data Cloud capabilities.
> Each capability is a self-contained repository: cloneable, lab-ready, and independently deliverable.

</div>

---

## 📦 Capability Registry

| Capability | Repo | Status | Personas | Iterations |
|---|---|---|---|---|
| **Zero-Copy Databricks v1** | [DATAFORCE-Zero-Copy-Databricks-v1](https://github.com/alibouhaddou/DATAFORCE-Zero-Copy-Databricks-v1) | ✅ Complete | Engineers · Scientists · Marketers | ✅✅✅✅ |

---

## 🏗️ Framework

Each capability repo follows the same 4-iteration, 2-hour delivery structure:

| Iteration | Content | Files |
|---|---|---|
| **1 — Strategic Framing** | Business value, architecture overview | `docs/00–02`, `README.md`, `INSTRUCTOR.md` skeleton, `labs/00-lab-index.md`, `environments/` |
| **2 — Technical Blueprinting** | Topic deep-dives, hands-on labs, scripts | `docs/03–07`, `labs/lab-01–05` + solutions, `scripts/participant/` |
| **3 — Well-Architected Review** | Guardrails, ADRs, pitfall synthesis | `docs/08-well-architected.md`, `scripts/instructor/` |
| **4 — Asset Delivery** | Checklist, Drive upload, Slack, GitHub tag | `docs/09-delivery-checklist.md`, registry update |

### Repository Structure (per capability)

```
DATAFORCE-{CapabilityName}-{Version}/
├── CLAUDE.md              ← capability state machine + iteration tracking
├── README.md              ← session agenda, prerequisites, persona map
├── INSTRUCTOR.md          ← facilitator guide, timing, troubleshooting
├── SELF_PACED.md          ← async entry point for solo learners
├── docs/                  ← 10 concept files (00–09)
├── labs/                  ← 5 hands-on labs + solutions/
├── environments/          ← shared Databricks config + per-participant templates
├── scripts/instructor/    ← provision, seed, validate, teardown
└── scripts/participant/   ← pre-flight, deploy, validate
```

---

## 🛠️ Global Tooling

| Tool | Purpose |
|---|---|
| `scripts/setup_mcp.sh` | Register all 4 MCP servers (`google-drive`, `salesforce-data-cloud`, `salesforce-sobject`, `lucidchart`) |
| `scripts/create_sf_external_client_app.sh` | Deploy Salesforce External Client App and store consumer key in macOS Keychain |

---

## 🔐 Security Baseline

- All secrets stored in **macOS Keychain** under service `dataforce`
- No credentials ever hardcoded in scripts, configs, or markdown
- PII never crosses Databricks → Data Cloud boundary in raw form (SHA256 tokens only)
- Consent enforced at the Databricks Dynamic View layer, not downstream

---

*Part of the [Dataforce](https://github.com/alibouhaddou/Dataforce) enablement framework · maintained by [@alibouhaddou](https://github.com/alibouhaddou)*
