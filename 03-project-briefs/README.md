# Project Briefs — Build These to Get Hired

## Why Projects Matter More Than Certifications in 2026

GCC interviews have changed. The question is no longer "what do you know?"

It is: **"Show me what you built in the last 90 days."**

A certification tells an interviewer you passed a test. A GitHub project tells them you can build, think, and ship. Every project here is designed to answer a real GCC interview question before it is even asked.

---

## How to Use These Briefs

1. Pick the project that matches your domain
2. Fill in the brief with your specific context
3. Build it over a weekend or two
4. Push to GitHub with a proper README (see `06-linkedin-github/readme-template.md`)
5. Write one LinkedIn post about what you built and what you learned

---

## Project 1 — AI-Powered Self-Healing Test Suite
**Best for:** Manual QA and Selenium Engineers
**Difficulty:** Beginner
**Time:** 1 weekend

### What to Build
A test suite using testRigor or Playwright that automatically adapts when the UI changes. Cover a real web application you use regularly.

### Minimum Viable Version
- 20+ test cases written in plain English (testRigor) or Playwright Python
- Tests cover: login, navigation, form submission, core user journey
- GitHub Actions CI pipeline that runs on every commit
- README explaining: what app is tested, why these test cases, what self-healing means

### Why It Works in Interviews
Shows you can modernise legacy manual test processes — the exact problem every GCC with inherited Selenium suites needs solved.

### Interview Question It Answers
*"Tell me about a testing framework you built or improved."*

---

## Project 2 — LLM Quality Evaluation Pipeline
**Best for:** SDET and QA Engineers targeting AI Quality roles
**Difficulty:** Intermediate
**Time:** 2 weekends

### What to Build
An evaluation pipeline using DeepEval that tests the output quality of any public LLM API. Design it around your domain — a banking chatbot, a healthcare FAQ, an e-commerce recommendation engine.

### Minimum Viable Version
```python
# Install: pip install deepeval
from deepeval import evaluate
from deepeval.metrics import AnswerRelevancyMetric, HallucinationMetric
from deepeval.test_case import LLMTestCase

test_case = LLMTestCase(
    input="Your domain-specific question here",
    actual_output="LLM response here",
    retrieval_context=["Your context documents here"]
)

metrics = [
    AnswerRelevancyMetric(threshold=0.7),
    HallucinationMetric(threshold=0.3)
]

evaluate([test_case], metrics)
```

- 10+ test cases covering your domain
- At least 3 different metrics (relevancy, hallucination, faithfulness)
- CI pipeline running evaluations on commit
- README explaining the domain, the thresholds chosen, and what failed

### Why It Works in Interviews
Shows you understand non-deterministic testing — the rarest and most valued QA skill in 2026.

### Interview Question It Answers
*"How would you test an AI-powered feature? How do you handle non-deterministic output?"*

---

## Project 3 — RAG Pipeline Evaluation (BFSI/Healthcare Focus)
**Best for:** QA Engineers with BFSI or Healthcare domain
**Difficulty:** Intermediate
**Time:** 2–3 weekends

### What to Build
A RAGAS evaluation pipeline for a document Q&A system in your domain. Use publicly available regulatory documents (RBI guidelines, IRDAI circulars, HIPAA summaries).

### Minimum Viable Version
```python
# Install: pip install ragas datasets
from ragas import evaluate
from ragas.metrics import faithfulness, answer_relevancy, context_precision
from datasets import Dataset

data = {
    'question': ['Domain-specific question from your industry'],
    'answer': ['LLM answer to evaluate'],
    'contexts': [['Relevant document passages']],
    'ground_truth': ['What the correct answer should be']
}

dataset = Dataset.from_dict(data)
result = evaluate(dataset, metrics=[faithfulness, answer_relevancy, context_precision])
print(result)
```

- 15+ domain-specific test cases
- Faithfulness, relevancy, and context precision all measured
- Threshold analysis documented in README
- Domain expertise evident in the questions chosen

### Why It Works in Interviews
BFSI and healthcare GCCs are deploying document AI urgently. Engineers who can evaluate RAG pipeline quality are exceptionally rare.

### Interview Question It Answers
*"Design a quality framework for an AI document processing system."*

---

## Project 4 — Selenium to Playwright Migration
**Best for:** Selenium Automation Engineers
**Difficulty:** Beginner-Intermediate
**Time:** 1–2 weekends

### What to Build
Take your 10 most-used Selenium test patterns and rewrite them in Playwright. Document the differences side by side.

### Minimum Viable Version
- 10+ Selenium tests migrated to Playwright Python
- Side-by-side comparison in README (what changed, why, what improved)
- Before: manual wait handling. After: auto-wait
- GitHub Actions CI running the Playwright suite
- Flaky test rate comparison if measurable

### Why It Works in Interviews
Shows you can modernise legacy infrastructure — the most common and urgent problem at GCCs with inherited Selenium codebases.

### Interview Question It Answers
*"Tell me about your experience with modern test automation frameworks."*

---

## Project 5 — AI Testing Framework Design Document
**Best for:** Senior QA Engineers and QA Leads targeting Architect roles
**Difficulty:** Advanced (no code required — this is a thinking exercise)
**Time:** 1 weekend

### What to Build
A 4–6 page PDF or Notion document describing how you would design a complete quality framework for an AI-powered application in your domain.

### What It Must Cover
1. **Clarify requirements** — what does quality mean for this system?
2. **Test layers** — UI, API, LLM evaluation, RAG evaluation
3. **Non-determinism strategy** — statistical thresholds, human review queues
4. **CI/CD integration** — what runs on every PR vs every model update
5. **Governance** — who owns release sign-off for AI features?

### Why It Works in Interviews
This is what GCCs hire AI Quality Architects to produce. A candidate who arrives with one already built signals seniority without needing to claim it.

### Interview Question It Answers
*"Design a testing framework for an AI-powered customer service application."*

---

## README Template for All Projects

See [`06-linkedin-github`](../06-linkedin-github/README.md) for the exact README structure that gets hiring managers to stop scrolling.

---

*© 2026 Sriram Advisory · sriramadvisory.com*
