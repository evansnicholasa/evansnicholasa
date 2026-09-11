## Nick Evans

**Senior Quality Engineer** · Ann Arbor, Michigan

Nearly eight years in quality engineering, all of it consulting for NTT DATA — which has put
me in a new domain every year or two: healthcare, utilities, consumer goods, logistics. I
work across UI, REST and SOAP APIs, mobile, databases and asynchronous messaging, in Java,
C#, TypeScript, Swift and SQL.

I've led four quality engineers on a cross-platform application serving 5M+ users, owned the
risk-based regression call during production releases, and built a reusable C#/.NET API
automation framework containerised for pipeline use.

---

### AI-assisted engineering

Three years writing code with **GitHub Copilot** day to day, including its pull request
reviewer. Alongside that I build with **Claude Code**, and test what it produces.

#### [Job Tracker](https://github.com/nevans-job-tracker) — full-stack, self-hosted

A working application rather than a demo. Tracks job applications end to end: company, role,
source, status, salary range, dates, notes, next action and contacts.

| | |
|---|---|
| **[job-tracker-backend](https://github.com/nevans-job-tracker/job-tracker-backend)** | FastAPI REST API in Python. SQLAlchemy models with Alembic migrations, against MariaDB over the MySQL wire protocol. |
| **[job-tracker-frontend](https://github.com/nevans-job-tracker/job-tracker-frontend)** | React single-page app built with Vite. |
| **[job-tracker-docs](https://github.com/nevans-job-tracker/job-tracker-docs)** | Requirements and architecture, consumed by both code repos as a git submodule so there is one source of truth rather than copies. |
| **[chrome-extension-job-tracker](https://github.com/nevans-job-tracker/chrome-extension-job-tracker)** | Extracts job details from a posting and saves them straight into the tracker. |

Two repos deployed independently, shared docs in a third, and the whole thing runs on a
self-hosted Debian box. Work tracked in Jira.

#### Also here

Experiments in where AI fits into a test automation workflow:

- **[ai-qa-proving-ground](https://github.com/nevans-ai-qa-claude/ai-qa-proving-ground)** — a
  deliberately defective web app and API. Twenty-two catalogued defects and four injectable
  flakes, each with a known-correct classification, so that a triage system can be scored
  against an answer key rather than eyeballed.
- **[ai-qa-failure-triage](https://github.com/nevans-ai-qa-claude/ai-qa-failure-triage)** —
  classifies each test failure as a product bug, a test bug, an environment fault or a
  flake, and scores itself against that answer key.
- **[ai-test-case-generator](https://github.com/nevans-ai-qa-chatgpt/ai-test-case-generator)**
  — turns user stories and acceptance criteria into structured, validated test cases.

---

### Toolkit

**Automation** — Playwright · Selenium WebDriver · REST Assured · RestSharp · Cucumber · Reqnroll · Citrus · TestNG

**Testing** — UI · REST/SOAP API · mobile and iOS · integration · end-to-end · regression · exploratory · database · cross-browser · asynchronous messaging

**Platforms** — Spring Boot · .NET · Azure DevOps · Jenkins · OpenShift · GCP · Maven · Docker · Jira · Postman

---

📍 Ann Arbor, Michigan &nbsp;·&nbsp; ✉️ [evansnicholasa@gmail.com](mailto:evansnicholasa@gmail.com) &nbsp;·&nbsp; 💼 [linkedin.com/in/evansnicholasa](https://linkedin.com/in/evansnicholasa)
