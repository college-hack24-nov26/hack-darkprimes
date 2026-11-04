# NTRO Dark Web Threat Actor De-Anonymization & Attribution Intelligence Platform

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Framework-Flask%203.0-lightgrey.svg)](https://flask.palletsprojects.com/)
[![Database](https://img.shields.io/badge/Database-Supabase%20PostgreSQL-green.svg)](https://supabase.com/)
[![Theme](https://img.shields.io/badge/Theme-Blockchain%20%26%20Cybersecurity-red.svg)](#)
[![Status](https://img.shields.io/badge/Status-Hackathon%20Ready-brightgreen.svg)](#)

> **PROBLEM STATEMENT ID:** 26151
> **ORGANIZATION:** National Technical Research Organisation (NTRO)
> **THEME:** Blockchain & Cybersecurity
> **CLASSIFICATION:** Defensive Cybersecurity Intelligence Platform (Probabilistic Attribution)

---

## 1. Project Overview & Objective

The **NTRO Dark Web Threat Actor De-Anonymization and Attribution Intelligence Analysis Platform** is an enterprise-grade cybersecurity intelligence system designed for defensive analysts and national security researchers.

It provides an end-to-end analytical pipeline to **collect, contextualize, correlate, and query threat-intelligence data** spanning darknet forums, cryptocurrency ledgers, PGP keyrings, passive infrastructure indicators, and manually curated criminal suspect registries. All attribution insights are computed as **probabilistic mathematical correlations** rather than unverified identity claims, upholding strict defensive ethics.

---

## 2. Defensive Cybersecurity Safeguards

> [!IMPORTANT]
> **DEFENSIVE COMPLIANCE & SAFETY NOTICE**
> - **No Active Exploitation:** The platform performs zero credential theft, active vulnerability exploitation, unauthorized system access, or Tor network traffic correlation attacks.
> - **Passive & Open Indicators:** Evaluates passive DNS history, Certificate Transparency logs, JA3 TLS hashes, and public darknet forum discussion metadata.
> - **Synthetic Demonstration Dataset:** Preloaded with fictional actor entities (`NIGHTFALCON`, `SHADOWBYTE`, `DARKORBIT`, `CRYPTONOVA`, `VOIDWALKER`, `SPECTRE_GHOST`, `ASTRAL_PHANTOM`, etc.) and mock blockchain wallets to protect operational privacy.
> - **Probabilistic Attribution:** All outputs clearly convey analytical confidence percentages and evidentiary justifications.
> - **Criminal Registry:** Manually added suspect profiles are cross-correlated using alias, date-of-birth, and cryptocurrency wallet fingerprints to detect multi-identity fraud — all on synthetic demonstration data.

---

## 3. Key Capabilities & Analytical Modules

1. **Executive SOC Command Dashboard**: Real-time KPI telemetry, risk distributions, temporal campaign trajectory charts, and highest-risk threat feeds.
2. **Threat Actor Directory**: Searchable, filterable repository of monitored threat clusters with sortable risk tiers, primary handles, and quick action drawers.
3. **11-Tab Deep Dossier**: Complete intelligence packaging across *Overview, Handles, PGP Keys, Wallets, Marketplaces, Infrastructure, Persona, Relationships, Timeline, Evidence, and Sources*.
4. **Interactive Cytoscape.js Relationship Graph**: Force-directed topological network visualization linking threat actors, aliases, PGP fingerprints, cryptocurrency wallets, marketplaces, and infrastructure nodes with click-to-inspect evidence drawer.
5. **Defensive Persona Stylometry Engine (`persona_engine.py`)**: Multi-dimensional Scikit-Learn TF-IDF, N-gram stylometry, Type-Token Ratio (TTR), vocabulary entropy, and operational cadence matching.
6. **4-Pillar Quantitative Risk Engine (`risk_engine.py`)**: Real-time mathematical scoring combining Infrastructure, Behavioural, Network, and Activity risk with automated mitigation recommendations.
7. **Temporal Intelligence Timeline**: Chronological event tracking from first observed forum registration to cryptocurrency transactions and zero-day exploit auctions.
8. **Passive Infrastructure Radar**: Monitoring of Tor v3 hidden services, JA3 fingerprints, SSH banners, and bulletproof ASN colocation.
9. **Automated Export & Printable PDF Dossier**: Instant download in structured CSV, JSON intelligence packages, and print-optimized PDF briefings.
10. **Dual Database Architecture**: Seamless live Supabase PostgreSQL connection with instant graceful fallback to high-fidelity in-memory demonstration mode.
11. **Criminal Registry (`/criminals`)**: Manually curated real-world suspect profiles with automated risk processing. On submission, each criminal record automatically generates a linked Threat Actor entry. A multi-identity attribution alert fires when multiple records share the same alias, date of birth, and cryptocurrency wallet fingerprints — demonstrating that a single suspect is operating under multiple fake identities.

---

## 4. Technology Stack

### Backend
| Library | Version | Purpose |
|:---|:---|:---|
| `Flask` | >= 3.0.0 | Web framework, routing, Jinja2 templates, Blueprint architecture |
| `supabase` | >= 2.0.0 | Supabase PostgreSQL client SDK |
| `numpy` | >= 1.24.0 | Numerical computations, risk score mathematics |
| `pandas` | >= 2.0.0 | Data manipulation, CSV export generation |
| `scikit-learn` | >= 1.3.0 | TF-IDF Vectorizer, Cosine Similarity — Persona Stylometry Engine |
| `networkx` | >= 3.1 | Graph topology analysis, relationship network processing |
| `python-dotenv` | >= 1.0.0 | `.env` file loader for Supabase credentials and config |
| `requests` | >= 2.31.0 | External HTTP calls, intelligence feed fetching |
| `pytest` | >= 7.4.0 | Automated test suite for API, risk engine, and persona engine |

### Built-in Python Libraries (no install required)
| Library | Purpose |
|:---|:---|
| `uuid` | Unique ID generation for criminal records, actors, events |
| `datetime` | Timestamps, event dates, timeline processing |
| `logging` | Server-side structured logging |
| `json` | API request/response encoding and decoding |
| `math` | Risk score calculations |
| `re` | Regex pattern matching in stylometry engine |
| `pathlib` | Cross-platform file path handling |
| `sys` | System-level startup operations |

### Frontend
- **HTML5**, Vanilla **CSS3** — Custom Dark SOC Cyber Design System, Glassmorphism, Neon Glow Accents
- **Vanilla JavaScript ES6+** — No frontend framework dependency
- **Cytoscape.js** — Force-directed Relationship Graph Topology
- **Chart.js** — Doughnut, Line, Horizontal Bar, Radar, Pie charts
- **FontAwesome 6.4** — Icons
- **Google Fonts** — Space Grotesk, Plus Jakarta Sans, JetBrains Mono

---

## 5. Directory Structure

```
darkguard(darkprimes)/
├── app.py                      # Flask application factory, routes & startup banner
├── config.py                   # Environment & Supabase credentials loader
├── requirements.txt            # Python dependencies
├── schema.sql                  # PostgreSQL DDL with indexes & constraints
├── seed.sql                    # SQL seed script for Supabase SQL Editor
├── .env                        # Live Supabase credentials (never commit)
├── .env.example                # Configuration template
├── README.md                   # Complete documentation & demo walkthrough
│
├── core/
│   ├── __init__.py
│   ├── database.py             # Supabase client with graceful offline fallback + Criminal CRUD
│   ├── seed_data.py            # Synthetic dataset (12 actors, 27 handles, 16 wallets, 6 criminals)
│   ├── persona_engine.py       # Scikit-learn TF-IDF & stylometric similarity engine
│   └── risk_engine.py          # 4-factor risk assessment model & mitigation generator
│
├── routes/
│   ├── __init__.py
│   ├── api.py                  # All REST API endpoints including /api/criminals
│   ├── auth.py                 # Authentication routes
│   ├── export.py               # CSV, JSON, and printable HTML/PDF dossier handlers
│   └── views.py                # Web page controllers for all pages including /criminals
│
├── templates/
│   ├── base.html               # Master SOC shell with topbar, glass sidebar & alerts
│   ├── dashboard.html          # Executive SOC Overview
│   ├── actors.html             # Threat Actor Directory
│   ├── actor_detail.html       # 11-Tab Deep Dossier
│   ├── criminals.html          # Criminal Registry — manual entry + multi-identity alert
│   ├── infrastructure.html     # Passive Infrastructure Telemetry
│   ├── relationships.html      # Interactive Cytoscape.js Relationship Graph
│   ├── persona.html            # Stylometric Persona Matcher with Radar Chart
│   ├── timeline.html           # Temporal Attack Trail & Events Feed
│   ├── sources.html            # Intelligence Source Provenance
│   ├── risk.html               # 4-Factor Risk Matrix Simulator
│   ├── reports.html            # Executive Threat Dossier Generator
│   ├── settings.html           # System Diagnostics & Demo Reset
│   ├── login.html              # Analyst authentication
│   ├── register.html           # New analyst registration
│   └── report_print.html       # Print-ready Official Intelligence Dossier
│
├── static/
│   ├── css/
│   │   └── style.css           # Premium Dark SOC design system & animations
│   └── js/
│       ├── main.js             # Global utilities, toast system & search
│       ├── dashboard.js        # Real-time Chart.js KPI analytics
│       ├── actors.js           # Filtering, search & actor table
│       ├── actor_detail.js     # 11-tab asynchronous dossier loader
│       ├── graph.js            # Cytoscape.js network visualizer & inspector
│       ├── persona.js          # Stylometric comparison & radar visualizer
│       ├── timeline.js         # Chronological event explorer
│       ├── risk.js             # Interactive risk recalculation
│       └── reports.js          # Dossier preview & export dispatcher
│
└── tests/
    ├── __init__.py
    ├── test_api.py             # REST API endpoint tests
    ├── test_persona_engine.py  # Stylometry and TF-IDF similarity tests
    └── test_risk_engine.py     # 4-factor risk calculation tests
```

---

## 6. Windows Setup & Installation Guide

Follow these exact steps in **PowerShell** or **Command Prompt**:

### Step 1: Create Virtual Environment
```powershell
python -m venv venv
```

### Step 2: Activate Virtual Environment
```powershell
venv\Scripts\activate
```

### Step 3: Install Required Dependencies
```powershell
pip install -r requirements.txt
```

### Step 4: Configure Supabase (Optional)
The system runs immediately out of the box in **Synthetic In-Memory Mode**. If you want to connect a live Supabase PostgreSQL database:

1. Copy `.env.example` to `.env`:
   ```powershell
   copy .env.example .env
   ```
2. Edit `.env` and set:
   ```ini
   SUPABASE_URL=https://your-project-id.supabase.co
   SUPABASE_KEY=your-supabase-anon-or-publishable-key
   SECRET_KEY=cyber-soc-ntro-secret-key-2026
   ```
3. Open your [Supabase SQL Editor](https://supabase.com/dashboard/project/_/sql) and run `schema.sql` followed by `seed.sql`.

### Step 5: Start the Platform
```powershell
python app.py
```

Open your browser and navigate to:
```
http://127.0.0.1:5000
```

---

## 7. Running Automated Test Suite

```powershell
pytest
```

---

## 8. REST API Reference

### Dashboard & System
| Method | Endpoint | Description |
|:---|:---|:---|
| `GET` | `/api/dashboard/stats` | Executive KPI counts, risk distributions, and category breakdowns |
| `GET` | `/api/system/status` | Database mode, record counts, and system health |
| `POST` | `/api/system/reset-demo` | Resets the in-memory synthetic dataset |

### Threat Actors
| Method | Endpoint | Description |
|:---|:---|:---|
| `GET` | `/api/actors` | Filtered list of threat actors (`search`, `risk`, `category`, `status`) |
| `GET` | `/api/actors/<actor_id>` | Specific threat actor profile |
| `GET` | `/api/actors/<actor_id>/handles` | Observed aliases and forum accounts |
| `GET` | `/api/actors/<actor_id>/pgp` | Cryptographic PGP public keys and fingerprints |
| `GET` | `/api/actors/<actor_id>/wallets` | Cryptocurrency wallets, USD totals, and risk levels |
| `GET` | `/api/actors/<actor_id>/marketplaces` | Underground forum/marketplace memberships and sales |
| `GET` | `/api/actors/<actor_id>/infrastructure` | Passive TLS, JA3, DNS, and IP indicators |
| `GET` | `/api/actors/<actor_id>/relationships` | Direct topological network connections |

### Criminal Registry
| Method | Endpoint | Description |
|:---|:---|:---|
| `GET` | `/api/criminals` | All criminal records (`search`, `status`, `category`) |
| `GET` | `/api/criminals/<criminal_id>` | Single criminal profile |
| `POST` | `/api/criminals` | Add new criminal record — auto-creates linked Threat Actor |
| `DELETE` | `/api/criminals/<criminal_id>` | Delete criminal record |

### Graph, Persona & Risk
| Method | Endpoint | Description |
|:---|:---|:---|
| `GET` | `/api/graph/data` | Complete Cytoscape.js nodes and edges dataset |
| `GET` | `/api/persona-links` | Pairwise stylometric and behavioral similarity links |
| `POST` | `/api/persona/analyze` | Computes live TF-IDF and stylometric similarity between two actors |
| `GET` | `/api/risk/<actor_id>` | Baseline 4-factor risk assessment |
| `POST` | `/api/risk/calculate` | Calculates weighted composite risk from custom parameters |

### Infrastructure, Timeline & Sources
| Method | Endpoint | Description |
|:---|:---|:---|
| `GET` | `/api/infrastructure` | Passive infrastructure observables (`search`, `type`) |
| `GET` | `/api/intelligence-events` | Chronological intelligence events (`actor_id`, `limit`) |
| `GET` | `/api/timeline/<actor_id>` | Actor-specific timeline events |
| `GET` | `/api/sources` | Ingestion pipelines, reliability scores, and provenance |

### Export & Reports
| Method | Endpoint | Description |
|:---|:---|:---|
| `GET` | `/api/export/actor/<actor_id>/json` | Downloads full JSON intelligence package |
| `GET` | `/api/export/actor/<actor_id>/csv` | Downloads structured CSV summary |
| `GET` | `/api/report/actor/<actor_id>` | Renders print-ready HTML/PDF intelligence dossier |

---

## 9. Criminal Registry — Multi-Identity De-Anonymization

The Criminal Registry (`/criminals`) is a manually curated suspect database with automated intelligence processing:

### How It Works
1. Analyst manually adds a criminal suspect with name, alias, DOB, nationality, dark web handles, crypto wallets, and risk score
2. On submission, the system **automatically creates a linked Threat Actor** entry in the Threat Actor Directory
3. The criminal record links directly to the actor dossier via **"View Dossier"** button
4. The system **cross-correlates all records** by alias + date of birth + wallet fingerprint
5. If multiple records match → **Multi-Identity Attribution Alert** fires with orange banner

### Preloaded Demo — 6 Fake IDs of One Person
The platform ships with 6 synthetic criminal records all belonging to the same suspect (`NightFalcon`) operating under different forged identities:

| # | Registered Name | Passport | Status |
|:---|:---|:---|:---|
| 1 | Alexei Nikolaev Volkov | RU-7741882301 | PRIMARY IDENTITY |
| 2 | Andrei Mikhail Sorokin | RU-8812993401 | Fake ID — 99.1% biometric match |
| 3 | Dmitri Oleg Petrov | RU-9934112201 | Fake ID — identical BTC wallet |
| 4 | Viktor Sergei Morozov | RU-7723009812 | Fake ID — XMR wallet cluster match |
| 5 | Pavel Artem Kuznetsov | RU-6612887734 | Fake ID — PGP key signed under alias |
| 6 | Igor Vasily Fedorov | RU-5501774423 | Fake ID — travel record biometric match |

All 6 share: same alias (`NightFalcon`), same DOB (`1991-03-17`), same address, same BTC/XMR wallets, same dark web handles.

---

## 10. Hackathon Jury Demonstration Script (5-Minute Walkthrough)

1. **Dashboard Overview (0:00 – 1:00)**
   - Point out the SOC Command Center styling, glassmorphism cards, glowing neon accents, and live KPI feeds.
   - Explain how passive darknet feeds are aggregated into real-time risk tiers (Critical, High, Medium, Low).
   - Highlight the Defensive Compliance Ribbon emphasizing probabilistic attribution.

2. **Threat Actor Dossier Investigation (1:00 – 2:00)**
   - Navigate to **Threat Actors** (`/actors`), demonstrate dynamic search and multi-criteria filters.
   - Click **Dossier** on `TA-NIGHTFALCON-01`.
   - Walk through the 11-tab layout: forum aliases, 4096-bit RSA PGP fingerprints, Monero/BTC wallet clusters, passive infrastructure nodes.

3. **Interactive Relationship Graph (2:00 – 3:00)**
   - Navigate to **Relationship Graph** (`/relationships`).
   - Demonstrate interactive physics, zoom/pan, and click on nodes/edges.
   - Show the Evidence Inspector Drawer revealing attribution confidence and multi-source corroboration.

4. **Criminal Registry — Multi-Identity Alert (3:00 – 4:00)**
   - Navigate to **Criminal Registry** (`/criminals`).
   - Show the preloaded **orange Multi-Identity Attribution Alert** — 6 fake IDs of the same person detected automatically.
   - Click **View Dossier** on any record to jump directly to the linked Threat Actor profile.
   - Demonstrate adding a new criminal record and watch it auto-appear in Threat Actors.

5. **Risk Calculator & Dossier PDF Export (4:00 – 5:00)**
   - Navigate to **Risk Analysis** (`/risk`) and adjust the 4 factor sliders to show dynamic tier shifts and mitigation suggestions.
   - Navigate to **Reports** (`/reports`) and click **Generate Printable Dossier (PDF)** for the executive intelligence briefing.

---

## 11. Future Scope & Roadmap

- **Graph Neural Networks (GNNs)**: Integration of PyTorch Geometric for automated link prediction on darknet escrow graphs.
- **Automated STIX 2.1 / TAXII Feeds**: Real-time push and subscription endpoints for national SOC interoperability.
- **Zero-Knowledge Multi-Party Computation**: Secure cross-agency indicator sharing without exposing sensitive watchlists.
- **Biometric Cross-Match API**: Integration with national identity databases for automated multi-identity fraud detection.
- **AI-Assisted Attribution (Gemini API)**: Natural language query interface for analyst-assisted threat investigation.

---

## 12. Author & Acknowledgments

- **Problem Statement:** 26151 — Dark Web Threat Actor De-anonymization
- **Organization:** National Technical Research Organisation (NTRO)
- **Built for:** Smart India Hackathon (SIH) 2026
