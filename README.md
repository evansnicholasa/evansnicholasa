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
reviewer. Alongside that I build with **Claude Code** — and, more usefully for a quality
engineer, I measure what it produces.

#### Can an LLM actually do test failure triage?

A deliberately structured experiment in how far AI can be pushed into a test automation
workflow, and where it should not go. Built so the answer could be **measured** rather than
demonstrated.

| | |
|---|---|
| **[ai-qa-proving-ground](https://github.com/nevans-ai-qa-claude/ai-qa-proving-ground)** | A deliberately defective app and API — 22 catalogued defects and 4 injectable flakes, each with a known-correct classification. The measuring instrument. It contains no AI at all, by design. |
| **[ai-qa-failure-triage](https://github.com/nevans-ai-qa-claude/ai-qa-failure-triage)** | Classifies each failure as a product bug, a test bug, an environment fault or a flake, and scores itself against that answer key. |

**The result is negative: the LLM lost.** Free deterministic clustering scores 73.2% macro
F1. Adding `claude-opus-5` on top drops it to **61.3%** and costs $0.31 a run — and it is
worst on the deliberately ambiguous cases, which is precisely where the argument for
reaching for a model is strongest.

The whole gap is one behaviour. The model finds exactly the same real test bugs the
clustering finds — identical recall — then invents twenty more, filing product tickets
against tests that were merely written badly. That is the false positive that destroys a
team's trust in automated triage.

The [corpus is published and checksum-pinned](https://github.com/nevans-ai-qa-claude/ai-qa-proving-ground/releases/tag/corpus-v2),
so the numbers can be reproduced rather than taken on faith.

*A parallel track using ChatGPT starts with
[ai-test-case-generator](https://github.com/nevans-ai-qa-chatgpt/ai-test-case-generator) —
user stories to validated test cases, schema-first, on the principle that model output is
untrusted input.*

#### [Job Tracker](https://github.com/nevans-job-tracker) — full-stack, self-hosted

A working application rather than a demo: a
[FastAPI](https://github.com/nevans-job-tracker/job-tracker-backend) service in Python
against MariaDB with Alembic migrations, a
[React and Vite](https://github.com/nevans-job-tracker/job-tracker-frontend) front end,
[shared documentation](https://github.com/nevans-job-tracker/job-tracker-docs) consumed by
both as a git submodule, and a
[Chrome extension](https://github.com/nevans-job-tracker/chrome-extension-job-tracker) that
pulls postings straight into it. Runs on a self-hosted Debian box.

---

### Toolkit

**Automation** — Playwright · Selenium WebDriver · REST Assured · RestSharp · Cucumber · Reqnroll · Citrus · TestNG

**Testing** — UI · REST/SOAP API · mobile and iOS · integration · end-to-end · regression · exploratory · database · cross-browser · asynchronous messaging

**Platforms** — Spring Boot · .NET · Azure DevOps · Jenkins · OpenShift · GCP · Maven · Docker · Jira · Postman

---

📍 Ann Arbor, Michigan &nbsp;·&nbsp; ✉️ [evansnicholasa@gmail.com](mailto:evansnicholasa@gmail.com) &nbsp;·&nbsp; 💼 [linkedin.com/in/evansnicholasa](https://linkedin.com/in/evansnicholasa)
