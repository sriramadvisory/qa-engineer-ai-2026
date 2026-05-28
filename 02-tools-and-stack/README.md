# Tools and Stack — QA Engineer AI Era 2026

## How to Use This Guide

Do not try to learn all of these. Use the priority column to decide where to start based on your current role.

**Manual QA Engineer** → Start with testRigor, then Applitools, then DeepEval
**Selenium Engineer** → Start with Playwright, then Copilot, then DeepEval
**SDET** → Start with DeepEval, then RAGAS, then LangSmith

---

## Tier 1 — Learn These First (All Free to Start)

| Tool | What It Does | Why It Matters | Free Tier | Start Here |
|---|---|---|---|---|
| **testRigor** | Plain English test automation — no code required | Directly replaces manual test execution. Familiarity increasingly valued in GCC interviews for AI Quality roles. | 500 test steps/month | [testrigor.com](https://testrigor.com) |
| **Playwright** | Modern browser automation (replaces Selenium) | Standard at every GCC. Selenium engineers must know this. | Free (open source) | [playwright.dev](https://playwright.dev) |
| **GitHub Copilot** | AI-assisted test code generation | Doubles automation coding speed. Increasingly expected in GCC interviews — not knowing it signals you are behind the current standard. | Free for students / ~₹830/month (verify at github.com/features/copilot) | [github.com/features/copilot](https://github.com/features/copilot) |
| **Applitools Eyes** | AI visual regression testing | Visual testing is 95% automatable — owning the tool is leverage. | Free for open source | [applitools.com](https://applitools.com) |
| **DeepEval** | LLM output quality testing framework (Python) | Every GCC deploying AI needs LLM evaluation. This is the emerging standard. | Free (open source) | [docs.confident-ai.com](https://docs.confident-ai.com) |
| **RAGAS** | RAG pipeline evaluation framework | BFSI and healthcare GCCs deploying document AI need this urgently. | Free (open source) | [docs.ragas.io](https://docs.ragas.io) |

---

## Tier 2 — Learn After Tier 1 Is Solid

| Tool | What It Does | Priority | Link |
|---|---|---|---|
| **LangSmith** | LLM application tracing and production quality monitoring | High — when AI features go to production, someone must own quality monitoring | [smith.langchain.com](https://smith.langchain.com) |
| **Sauce Labs AI** | Cloud-based self-healing browser and mobile testing | High — recognised by GCC recruiters immediately | [saucelabs.com](https://saucelabs.com) |
| **PromptFoo** | LLM prompt testing and red-teaming | Medium — important for AI safety testing roles | [promptfoo.dev](https://promptfoo.dev) |
| **Pact** | Consumer-driven contract testing for microservices | High — required for microservices QA architect roles | [pact.io](https://pact.io) |
| **k6** | Load testing with AI-assisted analysis | Medium — performance testing is still human-judged | [k6.io](https://k6.io) |
| **GitHub Actions** | CI/CD pipeline for automated test execution | High — every portfolio project should run in CI | [github.com/features/actions](https://github.com/features/actions) |

---

## Tier 3 — Know the Names, Understand the Purpose

You do not need to use these. You need to be able to discuss them intelligently in interviews:

- **Functionize** — AI test generation platform
- **Mabl** — Low-code AI test automation
- **Katalon** — Unified testing platform
- **Chromatic** — UI component visual testing
- **Great Expectations** — Data quality testing
- **Copilot for Tests** — GitHub's test-specific AI assistant

---

## Tool Priority by Your Domain

| Your Domain | Learn This First | Why | Second Priority |
|---|---|---|---|
| BFSI | DeepEval + RAGAS | Most BFSI GCCs deploying AI for fraud, credit, compliance | PromptFoo for AI safety |
| E-Commerce | testRigor + Applitools | High UI surface area, fast product changes | k6 for performance |
| Healthcare | PromptFoo + DeepEval | AI safety and bias testing is regulatory requirement | RAGAS for clinical document AI |
| SaaS / Product | Playwright + DeepEval | Fast release cycles need both layers | Applitools for visual regression |
| IT Services | testRigor + Pact | Self-healing tests + API contract testing for microservices | RAGAS when client deploys LLM |

---

## Your First Weekend — 8 Hours

| When | Task | Output |
|---|---|---|
| Saturday morning (2 hrs) | Create testRigor account. Follow 'Your First Test' tutorial. Write 3 plain English tests. | 3 working automated tests — no code |
| Saturday afternoon (2 hrs) | Create Applitools free account. Run visual testing tutorial. Screenshot a UI change. | Visual regression baseline established |
| Sunday morning (2 hrs) | Install DeepEval (`pip install deepeval`). Follow quickstart. Write one LLM evaluation test. | First AI quality test passing |
| Sunday afternoon (2 hrs) | Push everything to a public GitHub repo. Write a README explaining what each test validates. | Portfolio entry live on GitHub |

**At the end of this weekend you have a portfolio entry. That is more than 90% of your competition has.**

---

## Quick Reference — Install Commands

```bash
# Playwright
pip install playwright
playwright install

# DeepEval
pip install deepeval

# RAGAS
pip install ragas

# k6 (Mac)
brew install k6

# Pact
# Add to pom.xml or package.json — see pact.io/getting-started
```

---

*© 2026 Sriram Advisory · sriramadvisory.com*
