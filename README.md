<h1>Hey there 👋</h1>

I'm **Xinyi Lin** — a full-stack software engineer building real-world tools at the intersection of **software and healthcare**.

I've spent the last two years inside a high-volume cardiology clinic watching clinicians fight their EHR every day, and I build software that tries to do better.

---

## 🧩 Featured Projects

### 🏥 [CareFlow](https://careflow.xinyiklin.com) — Full-Stack EHR-Style Workflow App
A portfolio-grade EHR demo covering scheduling, clinical charting, billing, document management, and organization/facility administration. Modeled on the workflows I see in a real clinic — not generic CRUD.

- **Clinical charting** with SOAP progress notes (draft / signed / unsigned states), encounter lifecycle, and a 68-code CPT catalog
- **Configurable fee schedules** with payer and facility overrides
- **Patient timeline** that unifies appointments, encounters, medications, and allergies into one chronological view via a shared timeline component
- **Security**: SSN encryption at rest (Fernet), JWT + HTTP-only refresh cookies, CSRF protection, role-based permissions scoped per facility, and an audit log for sensitive actions
- **Typed end-to-end** via OpenAPI codegen (drf-spectacular + openapi-typescript)
- **Deployed** on AWS Amplify (frontend) + Render (backend), with PostgreSQL on Amazon RDS, Cloudflare R2 object storage, and Docker Compose for local dev

🔗 **Live demo:** [careflow.xinyiklin.com](https://careflow.xinyiklin.com) — clinician app at [clinician.xinyiklin.com](https://clinician.xinyiklin.com), patient portal at [patient.xinyiklin.com](https://patient.xinyiklin.com)
💻 **Code:** [github.com/xinyiklin/careflow](https://github.com/xinyiklin/careflow)

### 📄 [RoleFit AI](https://rolefit.xinyiklin.com/) — Browser-Primary, Local-First Job Application Workbench
RoleFit combines resume tailoring, recruiter-style review, and application tracking in the browser while a small Electron companion manages the local server and AI providers.

- **Evidence-grounded AI workflow** with prompt-injection fencing, output sanitization, offline adversarial evals, and reviewable edits instead of silent resume rewrites
- **Five explicit providers**: Claude Code, Codex, and Antigravity through provider-owned CLI sessions, plus OpenAI and Claude APIs with keys encrypted locally by the companion
- **Built on the shared Typeset engine** — edit the exported page directly, generate a deterministic client-side PDF, and save the structured document as a portable `.resume` file
- **Workday-aware job import** with AI distillation, deterministic fallback extraction, duplicate checks, and a fail-closed multi-stage polish/review workflow
- **Local application tracker** with table and calendar views; no RoleFit account or cloud workspace, and only the inputs required for the selected AI action leave the device

🔗 **Product site:** [rolefit.xinyiklin.com](https://rolefit.xinyiklin.com/)
💻 **Code:** [github.com/xinyiklin/rolefit-ai](https://github.com/xinyiklin/rolefit-ai)

### 📝 [Typeset](https://typeset.xinyiklin.com) — Browser-Native Resume Editor & Typesetting Engine
A WYSIWYG resume editor built on a from-scratch deterministic typesetting engine — edit the rendered page directly and export a pixel-faithful PDF that the app renders itself. Runs entirely in your browser; your resume never leaves your device.

- **From-scratch layout engine** (measure → line-break → blocks → layout) shared by the editor, browser print, and a client-side pdf-lib PDF emitter — the editor and the exported PDF render glyph-identically, verified by an automated font-parity suite
- **Direct editing on the engine-rendered page**: structured document model, inline formatting marks, and real undo/redo with exact caret restoration
- **Strict versioned `.resume` file format** with browser autosave, plus print-aware typography — six bundled font families, three of them metrically compatible with Times New Roman, Calibri, and Arial so page count survives a round trip through a word processor
- **Engine and editor live as npm workspace packages** (`@typeset/engine`, `@typeset/editor`) inside the RoleFit AI monorepo, powering both Typeset and RoleFit from one source of truth
- **Dockerized and deployed to AWS EC2** (custom domain, HTTPS) via a path-filtered GitHub Actions CI/CD pipeline

🔗 **Live app:** [typeset.xinyiklin.com](https://typeset.xinyiklin.com)
💻 **Code:** [github.com/xinyiklin/rolefit-ai](https://github.com/xinyiklin/rolefit-ai) — `apps/typeset` + `packages/engine` / `packages/editor`

### 🧰 [Machine Bootstrap](https://github.com/xinyiklin/machine-bootstrap) — Portable AI-Agent Workspace Setup
The tooling behind how I work with coding agents: one-time, idempotent seeding of agent guidance, shared skills, and a delivery workflow across a workspace of independent sibling repositories — without turning that workspace into a parent repo that silently owns every project's instructions.

- **Sibling-only ownership model** — the workspace root holds no live guidance; each project owns its own `AGENTS.md` / `CLAUDE.md` after seeding and is never re-synced against the template source
- **Idempotent Node initializers** that create only missing files, preserve existing ones, refuse unsafe targets (filesystem root, `$HOME`, Git-owned workspaces), and roll back only run-owned files on failure
- **`.gitignore` environment policy verified through Git itself** rather than by pattern matching — ambiguous or ineffective rules stop for manual review before any write
- **Supply-chain-pinned shared skills**: every skill pinned by repository, revision, and content SHA-256, with a missing-only installer and drift detection
- **Provider-neutral workflow packages** (Product Partner → Delivery Lead → Verifier, with explicit approval gates) compiled into deterministic Claude and Codex agent adapters
- **Verified on Linux and Windows** in CI against a disposable regression suite covering rollback, concurrency, and fail-closed paths

💻 **Code:** [github.com/xinyiklin/machine-bootstrap](https://github.com/xinyiklin/machine-bootstrap)

---

## 🛠 Tech Stack

**Languages:** Python, TypeScript, JavaScript, C++, SQL, HTML/CSS

**Frontend:** React, TypeScript, Vite, React Query, React Router, Tailwind CSS

**Backend:** Django, Django REST Framework, Node.js, REST APIs, JWT + CSRF auth

**Data & Storage:** PostgreSQL, Cloudflare R2 / S3-compatible object storage

**Desktop & Local Runtime:** Electron, loopback Node services, OS-encrypted credential storage

**Tooling & Deployment:** Git, Docker, npm workspaces (monorepo), AWS (Amplify, RDS, EC2), GitHub Actions CI/CD, GitHub Pages, Cloudflare, Render, ESLint, Prettier, pre-commit hooks

---

## 🎯 About Me

- 🏥 Two years inside a cardiovascular clinic — real exposure to EHR migrations, scheduling bottlenecks, and clinical workflow design
- 🛠 Comfortable across the full stack: schema design, REST APIs, React frontends, auth/security, deployment
- 🌱 Currently going deeper on system design, OpenAPI tooling, and clinical informatics
- 🌐 Bilingual in English and Mandarin Chinese

---

## 🌐 Get in Touch

- 📧 **Email:** xinyiklin@gmail.com
- 💼 **LinkedIn:** [linkedin.com/in/xinyiklin](https://www.linkedin.com/in/xinyiklin/)
- 🧍 **Portfolio:** [xinyiklin.com](https://xinyiklin.com)

---

> Currently exploring **early-career and SWE I roles in healthcare tech and full-stack** — always open to a coffee chat about clinical software, full-stack architecture, or building tools clinicians actually want to use.
