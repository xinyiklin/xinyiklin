<h1>Hey there 👋</h1>

I'm **Xinyi (Kevin) Lin** — a full-stack software engineer building real-world tools at the intersection of **software and healthcare**.

I've spent more than three years inside a high-volume cardiology clinic, where I led an EHR migration and watched clinicians fight their EHR every day. I build software that tries to do better.

---

## 🧩 Featured Projects

### 🏥 [CareFlow](https://careflow.xinyiklin.com) — Full-Stack Clinic Platform
CareFlow connects patient self-service with a facility-scoped clinician workspace: a patient books a visit, staff find it on the schedule, and the chart is one click away. Modeled on the workflows I see in a real clinic — not generic CRUD.

- **Connected scheduling** with facility-local times and duration-aware provider/resource conflict checks, re-run under a facility-row lock (`select_for_update`) in one transaction — patient bookings reject conflicts, while staff can explicitly confirm an intentional overlap
- **Separate patient and clinician surfaces**: access resolved on the server per facility and per patient, a surface claim on every access token, and isolated refresh-cookie paths for the two portals
- **Patient Hub** that brings registration, appointments, SOAP charting, documents, medications, allergies, billing, and a unified timeline into one workspace; portal refill requests feed the staff queue
- **Multilingual patient portal** (i18next) with booking, records, medications, and secure clinician–patient messaging
- **Deliberate data handling**: SSNs encrypted at rest and masked by default, with intentional, audited reveal
- **Typed end-to-end** — Django's OpenAPI schema generates the TypeScript API package, and CI fails on contract drift
- **Deployed** as independently shipped AWS Amplify frontends with a Render backend and PostgreSQL

🔗 **Live demo:** [careflow.xinyiklin.com](https://careflow.xinyiklin.com) — clinician app at [clinician.xinyiklin.com](https://clinician.xinyiklin.com), patient portal at [patient.xinyiklin.com](https://patient.xinyiklin.com)
💻 **Code:** [github.com/xinyiklin/careflow](https://github.com/xinyiklin/careflow)

### 📄 [RoleFit AI](https://rolefit.xinyiklin.com/) — Local-First Job Application Workbench
RoleFit tailors resumes and cover letters, reviews them like a recruiter would, and tracks applications — in the browser, backed by a small Electron companion that runs the local server and AI providers. No account, no cloud workspace.

- **Evidence-grounded AI edits**: flags changes the resume or profile can't support, and applies only edits the user approves — with an optional review step that holds back low-impact or incorrect polish
- **Benchmarked, not vibes**: prompts and models compared with blinded pairwise judging by two model families plus per-edit fact checks, in an offline eval suite that runs without network access
- **Hardened local server**: loopback-bound Node.js with Host/Origin checks against CSRF and DNS rebinding; the Chrome/Firefox extension connects only after the user approves pairing
- **Five explicit providers** — Claude Code, Codex, and Antigravity through their own CLI sessions, plus OpenAI and Claude APIs with keys encrypted locally by the companion
- **Job intake from where postings actually live**: one click from the paired extension, with site-aware parsing for Workday, Ashby/Handshake, Greenhouse, Microsoft Careers, Rippling, and more, plus a generic structured-data fallback
- **Text-based PDF resume import**, and a local tracker with table and calendar views, duplicate detection, and revision-aware saves

🔗 **Product site:** [rolefit.xinyiklin.com](https://rolefit.xinyiklin.com/)
💻 **Code:** [github.com/xinyiklin/rolefit-ai](https://github.com/xinyiklin/rolefit-ai)

### 📝 [Typeset](https://typeset.xinyiklin.com) — Browser-Native Resume Editor & Typesetting Engine
A WYSIWYG resume editor built on a from-scratch deterministic typesetting engine — edit the rendered page directly and export a PDF the app renders itself. Runs entirely in your browser; your resume never leaves your device.

- **From-scratch layout engine** (measure → line-break → blocks → layout) shared by the editor, browser print, and a client-side pdf-lib PDF emitter — the editor and the exported PDF render glyph-identically, verified by an automated font-parity suite
- **Direct editing on the engine-rendered page**: structured document model, inline formatting marks, and real undo/redo with exact caret restoration
- **Strict versioned `.resume` file format** with browser autosave, and 30 bundled font families — including metric-compatible stand-ins for Times New Roman, Calibri, and Arial, so page count survives a round trip through a word processor
- **Shared by two products**: the engine and editor are npm workspace packages (`@typeset/engine`, `@typeset/editor`) inside the RoleFit AI monorepo, powering both Typeset and RoleFit from one source of truth
- **Dockerized and deployed to AWS EC2** (custom domain, HTTPS) via a path-filtered GitHub Actions CI/CD pipeline

🔗 **Live app:** [typeset.xinyiklin.com](https://typeset.xinyiklin.com)
💻 **Code:** [github.com/xinyiklin/rolefit-ai](https://github.com/xinyiklin/rolefit-ai) — `apps/typeset` + `packages/engine` / `packages/editor`

### 🧰 [Machine Bootstrap](https://github.com/xinyiklin/machine-bootstrap) — Portable AI-Agent Workspace Setup
The tooling behind how I work with coding agents: a Node.js CLI and reusable agent skills that set up Claude Code and Codex across a workspace of independent repositories — seeding, syncing, and auditing each project's agent guidance without overwriting local edits.

- **Sibling-only ownership model** — the workspace root holds no live guidance; each project owns its own `AGENTS.md` / `CLAUDE.md` after seeding
- **Idempotent initializers** that create only missing files, refuse unsafe targets (filesystem root, `$HOME`, Git-owned workspaces), and roll back only run-owned files on failure
- **Supply-chain-pinned skills**: every third-party skill pinned to an exact upstream revision and SHA-256 content hash, with drifted content rejected before installation
- **Plan → implement → verify workflow** compiled from shared, provider-neutral role contracts into Claude Code and Codex agents, with explicit approval gates
- **Skills for keeping guidance honest** — project init/sync, a read-only guidance audit, and a continuity ledger for handoffs between sessions
- **Filesystem regression suite** run in CI on Linux, Windows, and macOS, covering rollback, concurrency, and fail-closed paths

💻 **Code:** [github.com/xinyiklin/machine-bootstrap](https://github.com/xinyiklin/machine-bootstrap)

---

## 🛠 Tech Stack

**Languages:** Python, TypeScript, JavaScript, SQL, Java, HTML/CSS

**Frontend:** React, TypeScript, Vite, TanStack Query, React Router, Tailwind CSS, i18next

**Backend:** Django, Django REST Framework, Node.js, REST APIs, OpenAPI, JWT + CSRF auth

**Data & Storage:** PostgreSQL, Cloudflare R2 / S3-compatible object storage

**Desktop & Local Runtime:** Electron, loopback Node services, browser extensions, OS-encrypted credential storage

**AI Tooling:** Claude Code, Codex, OpenAI and Claude APIs, offline LLM evals

**Tooling & Deployment:** Git, Docker, npm workspaces (monorepo), AWS (Amplify, EC2), GitHub Actions CI/CD, Cloudflare, Render

---

## 🎯 About Me

- 🏥 3+ years inside a cardiovascular clinic — led an EHR migration and work daily on scheduling bottlenecks and clinical workflow
- 🛠 Comfortable across the full stack: schema design, REST APIs, React frontends, auth/security, deployment
- 🎓 B.A. in Computer Science, Hunter College (CUNY) — Daedalus Honors Scholar
- 🌱 Currently going deeper on system design, concurrency in scheduling systems, and clinical informatics
- 🌐 Bilingual in English and Mandarin Chinese

---

## 🌐 Get in Touch

- 📧 **Email:** xinyiklin@gmail.com
- 💼 **LinkedIn:** [linkedin.com/in/xinyiklin](https://www.linkedin.com/in/xinyiklin/)
- 🧍 **Portfolio:** [xinyiklin.com](https://xinyiklin.com)

---

> Currently exploring **early-career and SWE I roles in healthcare tech and full-stack** — always open to a coffee chat about clinical software, full-stack architecture, or building tools clinicians actually want to use.
