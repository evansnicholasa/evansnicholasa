## Nick Evans

**Senior Quality Engineer** · Ann Arbor, Michigan · **[evansnicholasa.github.io](https://evansnicholasa.github.io)**

Nearly eight years in quality engineering, all of it consulting for NTT DATA, which has put
me in a new domain every year or two: healthcare, utilities, consumer goods, logistics. I
have automated React and Angular UI, API, integration and mobile testing in object-oriented
Java, C#, TypeScript and Swift, and have worked across REST and SOAP APIs, databases and
asynchronous messaging.

I've led and mentored four quality engineers on a cross-platform application serving more
than five million users, directed onshore, nearshore and offshore quality engineers, was my
team's release quality gate on production releases, and designed a containerized .NET API
framework whose tests ran in a GitHub Actions pipeline.

I've used **GitHub Copilot Plugin** for three years as a force multiplier while writing and
debugging automated test cases. I also build with **Anthropic Claude Code** and **OpenAI
Codex**, and I published a measurement of LLM-assisted failure triage against a deterministic
baseline.

---

### Does an LLM beat a simple baseline at triaging test failures?

A test fails overnight. Someone has to decide whether the product, the test or the
environment is at fault, or whether the test is simply flaky. I wanted to know whether a
language model does that better than a simple baseline.

So I first built a test application: a deliberately defective application and API with 22
cataloged defects and 4 injectable flakes. Each defect carries the classification a correct
triage system should assign, so every failure it produces has a known right answer. That
repository contains no AI, so the application shares no components with the classifiers being
measured.

> **Result:** deterministic clustering scored **73.2% macro F1** at no cost and with no
> dependencies. Adding Claude Opus 5 (`claude-opus-5`) on the ambiguous cases lowered it to
> **61.3%** and cost **$0.31** a run.
>
> The difference comes from one behavior. The model finds the same real broken tests the
> clustering finds, with identical recall, then labels twenty more failures "broken test" that
> were not. Five of those were genuine product bugs.

The model was also weakest on the deliberately ambiguous cases, where a model would be
expected to help most. The corpus is published as a checksummed release and cited by tag, so
the numbers can be reproduced.

**[ai-qa-proving-ground](https://github.com/nevans-ai-qa-claude/ai-qa-proving-ground)** (the defective application and its corpus) · **[ai-qa-failure-triage](https://github.com/nevans-ai-qa-claude/ai-qa-failure-triage)** (the classifier and the scoring)

### [Job Tracker](https://github.com/nevans-job-tracker): full-stack and self-hosted

Built with Anthropic Claude Code. A FastAPI service in Python with SQLAlchemy models and
Alembic migrations against MariaDB, a React single-page front end built in Vite, shared
requirements and architecture in a third repo that both consume as a git submodule, and two
Chrome extensions: one scrapes a posting and files it, the other marks an existing application
closed in a single click. Runs on a self-hosted Debian machine.

**[backend](https://github.com/nevans-job-tracker/job-tracker-backend)** · **[frontend](https://github.com/nevans-job-tracker/job-tracker-frontend)** · **[shared docs](https://github.com/nevans-job-tracker/job-tracker-docs)** · **[import extension](https://github.com/nevans-job-tracker/chrome-extension-job-tracker)** · **[close-posting extension](https://github.com/nevans-job-tracker/chrome-extension-job-tracker-close-posting)**

### [Jira Command-Line Client](https://github.com/evansnicholasa/jira-cli): replacing a metered integration with a small script

I was driving the Job Tracker project's Jira board through Atlassian's hosted Rovo MCP
server. It worked, but it meters against Rovo credits and is not offered on the Free plan, so
keeping one integration alive meant paying for a tier I had no other use for. The REST API
underneath it is on every plan, unmetered.

So I built, with Claude Code, a short Python program that talks to it directly: a single
file, no dependencies, any Python 3.9 or later. It runs anywhere there is a shell (a terminal,
an editor, a CI job, more than one AI coding agent), whereas an MCP server only works where it
has been configured. And it can be read, tested and changed, which a hosted service cannot.

### [Job Search Workflow](https://github.com/evansnicholasa/job-application-workflow): a manager agent and its subagents

Built with Anthropic Claude Code. Each step of a job application (fit review, résumé
tailoring, cover letter, finalizing) is a Claude Code skill run by a subagent. A manager agent
hands each step to a subagent, keeps a state file for every job, and shows what needs my
attention on an HTML job board that refreshes itself. Nothing is applied for, published or
sent without my explicit approval at that step. The repository includes a demo with fictional
data.

---

### Toolkit

**Automation**: Playwright · Selenium WebDriver · REST Assured · RestSharp · Cucumber · Reqnroll · Citrus · TestNG

**Testing**: UI · REST/SOAP API · mobile and iOS · integration · end-to-end · regression · exploratory · database · cross-browser · asynchronous messaging

**Platforms**: Spring Boot · .NET · Azure DevOps · Jenkins · OpenShift · GCP · Maven · Docker · Jira · Postman

---

📍 Ann Arbor, Michigan &nbsp;·&nbsp; ✉️ [evansnicholasa@gmail.com](mailto:evansnicholasa@gmail.com) &nbsp;·&nbsp; 💼 [linkedin.com/in/evansnicholasa](https://linkedin.com/in/evansnicholasa) &nbsp;·&nbsp; 🌐 [evansnicholasa.github.io](https://evansnicholasa.github.io)
