## Nick Evans

**Senior Quality Engineer** · Ann Arbor, Michigan · **[evansnicholasa.github.io](https://evansnicholasa.github.io)**

Nearly eight years in quality engineering, all of it consulting for NTT DATA — which has put
me in a new domain every year or two: healthcare, utilities, consumer goods, logistics. I
work across UI, REST and SOAP APIs, mobile, databases and asynchronous messaging, in Java,
C#, TypeScript, Swift and SQL.

I've led four quality engineers on a cross-platform application serving more than five
million users, owned the risk-based regression call during production releases, and built a
reusable C#/.NET API automation framework containerized for pipeline use.

Three years writing code with **GitHub Copilot** day to day, including its pull request
reviewer. Alongside that I build with **Claude Code** — and, more usefully for a quality
engineer, I measure what it produces.

---

### Does an LLM beat a simple baseline at triaging test failures?

A test goes red overnight. Someone has to decide whether the product is broken, the test is
broken, the environment is broken, or it is simply flaky. I wanted to know whether a language
model does that better than something simple.

So I built the measuring instrument first — a deliberately defective application and API with
22 cataloged defects and 4 injectable flakes, each carrying the classification a correct
triage system should assign. Every failure it produces has a known right answer. That
repository contains no AI at all, deliberately: an instrument that shares components with the
thing it measures is not worth much.

> **The model lost.** Deterministic clustering scores **73.2% macro F1** at zero cost and
> with no dependencies. Adding `claude-opus-5` on the ambiguous cases dropped it to **61.3%**
> and cost **$0.31** a run.
>
> The whole gap is one behavior. The model finds exactly the same real broken tests the
> clustering finds — identical recall — then labels twenty more failures "broken test" that
> were not. Five of those were genuine product bugs.

It was also weakest on the deliberately ambiguous cases, which is precisely where the
argument for reaching for a model is strongest. The corpus is published as a checksummed
release and cited by tag, so the numbers can be reproduced rather than taken on faith.

**[ai-qa-proving-ground](https://github.com/nevans-ai-qa-claude/ai-qa-proving-ground)** — the measuring instrument · **[ai-qa-failure-triage](https://github.com/nevans-ai-qa-claude/ai-qa-failure-triage)** — the classifier and the scoring

### [Job Tracker](https://github.com/nevans-job-tracker) — full-stack, self-hosted

A working application rather than a demo. A FastAPI service in Python with SQLAlchemy models
and Alembic migrations against MariaDB, a React single-page front end built in Vite, shared
requirements and architecture in a third repo that both consume as a git submodule, and a
Chrome extension that pulls postings straight into it. Runs on a self-hosted Debian machine.

**[backend](https://github.com/nevans-job-tracker/job-tracker-backend)** · **[frontend](https://github.com/nevans-job-tracker/job-tracker-frontend)** · **[shared docs](https://github.com/nevans-job-tracker/job-tracker-docs)** · **[extension](https://github.com/nevans-job-tracker/chrome-extension-job-tracker)**

### Also here

**[ai-test-case-generator](https://github.com/nevans-ai-qa-chatgpt/ai-test-case-generator)** —
turns user stories and acceptance criteria into structured, validated test cases, schema-first
on the principle that model output is untrusted input.

---

### Toolkit

**Automation** — Playwright · Selenium WebDriver · REST Assured · RestSharp · Cucumber · Reqnroll · Citrus · TestNG

**Testing** — UI · REST/SOAP API · mobile and iOS · integration · end-to-end · regression · exploratory · database · cross-browser · asynchronous messaging

**Platforms** — Spring Boot · .NET · Azure DevOps · Jenkins · OpenShift · GCP · Maven · Docker · Jira · Postman

---

📍 Ann Arbor, Michigan &nbsp;·&nbsp; ✉️ [evansnicholasa@gmail.com](mailto:evansnicholasa@gmail.com) &nbsp;·&nbsp; 💼 [linkedin.com/in/evansnicholasa](https://linkedin.com/in/evansnicholasa) &nbsp;·&nbsp; 🌐 [evansnicholasa.github.io](https://evansnicholasa.github.io)
