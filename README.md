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

### 📄 [RoleFit AI](https://xinyiklin.com/rolefit-ai/) — Local-First Resume Tailoring Workbench
A local-first workbench that imports a job posting, scores how well your resume actually fits it, and runs honest, evidence-grounded AI polish on a real typeset editing surface — no fabricated achievements, strict recruiter-style review.

- **Recruiter-style review engine** that scores resume-to-role fit and refuses to score above what the resume actually evidences
- **Multi-provider AI polish** across 10+ hosted, local, and CLI backends (Claude Code / Codex / Antigravity CLIs, OpenAI / Anthropic / Gemini / OpenRouter and more, or fully local via Ollama)
- **Anti-fabrication by design**: prompt-injection fencing, a grounded-output sanitizer, an offline anti-fabrication eval suite, and every suggested edit surfaced as reviewable accept/edit/discard diffs
- **Built on the shared Typeset engine** — the editor *is* the preview: direct editing on the exported page layout, client-side PDF export, and portable `.resume` files, no external toolchain
- **Job-link import** (Workday-aware, with a generic fallback) plus a Chrome/Firefox extension that fit-checks any posting in-page and imports it in one click
- **On-disk application tracker** with table and calendar views — everything stays on your machine

🔗 **Live demo:** [xinyiklin.com/rolefit-ai](https://xinyiklin.com/rolefit-ai/)
💻 **Code:** [github.com/xinyiklin/rolefit-ai](https://github.com/xinyiklin/rolefit-ai)

### 📝 [Typeset](https://typeset.xinyiklin.com) — Browser-Native Resume Editor & Typesetting Engine
A WYSIWYG resume editor built on a from-scratch deterministic typesetting engine — edit the rendered page directly and export a pixel-faithful PDF that the app renders itself. Runs entirely in your browser; your resume never leaves your device.

- **From-scratch layout engine** (measure → line-break → blocks → layout) shared by the editor, browser print, and a client-side pdf-lib PDF emitter — the editor and the exported PDF render glyph-identically, verified by an automated font-parity suite
- **Direct editing on the engine-rendered page**: structured document model, inline formatting marks, and real undo/redo with exact caret restoration
- **Strict versioned `.resume` file format** with browser autosave, plus print-aware typography — three bundled font families (Latin Modern, Source Serif 4, Source Sans 3), 6–48 pt sizes, margins, and spacing controls
- **Engine and editor extracted into npm workspace packages** (`@typeset/engine`, `@typeset/editor`) powering both Typeset and RoleFit AI
- **Dockerized and deployed to AWS EC2** (custom domain, HTTPS) via a GitHub Actions CI/CD pipeline

🔗 **Live app:** [typeset.xinyiklin.com](https://typeset.xinyiklin.com)
💻 **Code:** [github.com/xinyiklin/typeset](https://github.com/xinyiklin/typeset)

---

## 🛠 Tech Stack

**Languages:** Python, TypeScript, JavaScript, Java, C++, SQL, HTML/CSS

**Frontend:** React, TypeScript, Vite, React Query, React Router, Tailwind CSS

**Backend:** Django, Django REST Framework, Node.js, REST APIs, JWT + CSRF auth

**Data & Storage:** PostgreSQL, Cloudflare R2 / S3-compatible object storage

**Tooling & Deployment:** Git, Docker, AWS (Amplify, RDS, EC2), GitHub Actions CI/CD, Render, ESLint, Prettier, pre-commit hooks

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
