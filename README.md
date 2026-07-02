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

🔗 **Live demo:** [careflow.xinyiklin.com](https://careflow.xinyiklin.com)
💻 **Code:** [github.com/xinyiklin/careflow](https://github.com/xinyiklin/careflow)

### 📄 [RoleFit AI](https://xinyiklin.com/rolefit-ai/) — Local-First Resume Tailoring Workflow
A local-first webapp that imports a job posting, scores how well your resume actually fits it, and runs honest, evidence-based AI polish — no fabricated achievements, strict recruiter-style review.

- **Recruiter-style review engine** that scores resume-to-role fit, capping scores at what the resume actually evidences
- **Multi-provider AI polish** across 10+ hosted, local, and CLI backends (Claude / OpenAI / Gemini / OpenRouter / Ollama and more) with a deterministic local fallback
- **Anti-fabrication by design**: schema-validated, section-scoped suggestions surfaced as accept/edit/discard diffs, a grounded-output sanitizer, and 120+ offline eval probes
- **Job-link import** (Workday / Greenhouse and more) plus a browser fit-check extension
- **LaTeX/PDF export** via Tectonic and an on-disk application tracker — everything stays on your machine

🔗 **Live demo:** [xinyiklin.com/rolefit-ai](https://xinyiklin.com/rolefit-ai/)
💻 **Code:** [github.com/xinyiklin/rolefit-ai](https://github.com/xinyiklin/rolefit-ai)

### ⚒️ [JakeForge](https://jakeforge.xinyiklin.com) — Self-Hosted LaTeX Resume Editor
A focused extraction of RoleFit AI's editor into a standalone Jake's-style resume editor — inline structured editing, drag-and-drop reordering, faithful LaTeX styling, and one-click PDF / .tex export via Tectonic.

- **On-page structured editing** with drag-and-drop sections, entries, and bullets (@dnd-kit)
- **Faithful Jake's template rendering** with layout, spacing, and typography controls
- **Dockerized and deployed to AWS EC2** (custom domain, HTTPS) via a GitHub Actions CI/CD pipeline
- **Privacy-first**: resume lives in localStorage; rendering only calls the app's own LaTeX endpoints

🔗 **Live demo:** [jakeforge.xinyiklin.com](https://jakeforge.xinyiklin.com)
💻 **Code:** [github.com/xinyiklin/jakeforge](https://github.com/xinyiklin/jakeforge)

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
