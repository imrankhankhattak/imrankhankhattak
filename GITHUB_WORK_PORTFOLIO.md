# Imran Khan — GitHub Work Portfolio

> **Purpose:** Source material for an LLM to create a resume, CV, professional bio, or portfolio.
>
> **Profile:** [github.com/imrankhankhattak](https://github.com/imrankhankhattak)
>
> **Prepared:** 2026-09-17
>
> **Scope:** Public repositories visible from the GitHub profile at the time of preparation. Descriptions below are grounded in repository metadata and README documentation; claims should be verified against commit history, deployed applications, publications, and formal employment records before being used as resume facts.

---

## Executive Profile

Imran Khan works across **AI engineering, large language models, explainable AI, AI safety, AI governance, educational technology, and mission-driven web applications**. His public projects demonstrate a combination of research experimentation, applied AI product development, full-stack engineering, technical documentation, and public-interest technology.

### Core themes

- **Generative AI applications:** Gemini-powered applications, AI Studio projects, document understanding, vision-language grading, and conversational tools.
- **LLM engineering:** Training a small GPT-style transformer from scratch using PyTorch, Hugging Face datasets, and GPU acceleration.
- **Explainable AI (XAI):** Benchmarking feature attribution methods, constructing linguistic unit tests for black-box LLMs, and implementing experiment pipelines and evaluation metrics.
- **Responsible AI:** AI governance analysis, fairness in machine translation, gender-bias evaluation, and public-interest AI policy tooling.
- **Education technology:** Adaptive MCQ testing, document ingestion, quiz generation, personalized difficulty scoring, and handwritten answer-sheet grading.
- **Web and product engineering:** TypeScript/Next.js, Python/Streamlit, Firebase, Firestore, static websites, responsive UX, accessibility, and deployment documentation.
- **Community and social impact:** Websites and tools supporting youth organizations, nonprofits, policy professionals, educators, and communities in Pakistan and the Global South.

### Technologies evidenced across projects

**Languages:** Python, TypeScript, JavaScript, HTML, CSS, SQL-like data workflows

**AI/ML:** Google Gemini, Google GenAI SDK, Hugging Face Transformers, PyTorch, Captum, feature attribution, vision-language models, structured generation, prompt engineering

**Application frameworks:** Next.js, React ecosystem, Streamlit, vanilla JavaScript

**Cloud and infrastructure:** Firebase Authentication, Firestore, Firebase Storage, AWS PartyRock, Google AI Studio, Google Colab, Streamlit Community Cloud, CUDA

**Data and tooling:** Pandas, NumPy, Hugging Face Datasets, Pydantic, Pillow, OpenPyXL, python-docx, GSAP, Flowbite

**Engineering practices:** API integrations, structured JSON outputs, schema validation, hash-based deduplication, transactions, adaptive scoring, retry/backoff logic, modular storage backends, accessibility, responsive design, and technical documentation.

---

## Selected Project Highlights

### 1. GradePanel — Agentic Grading for Handwritten Answer Sheets

- **Repository:** [imrankhankhattak/team-fti](https://github.com/imrankhankhattak/team-fti)
- **Role/evidence:** Project repository under Imran's account; README documents the application design and implementation.
- **Summary:** Built an agentic AI application that reads handwritten exam answer sheets and grades them against a teacher's rubric.
- **Key capabilities:**
  - Accepts model answer sheets, marking guidelines, student photographs, and PDFs.
  - Uses a vision LLM to read handwriting and grade answers in one pass, avoiding a separate OCR stage.
  - Returns marks awarded, maximum marks, reasoning, and confidence for each question.
  - Flags low-confidence answers instead of guessing.
  - Provides teacher review, manual score editing, finalization, dashboards, and XLSX/CSV export.
- **Architecture:** Three-agent examiner panel:
  1. **Rubric Architect** creates a structured rubric.
  2. **Grader / First Marker** grades confident answers and writes precedents to a consistency ledger.
  3. **Summarizer** creates per-student feedback and a pending-review list.
- **Technical implementation:** Python 3.12, Streamlit, Gemini vision models, provider-agnostic LLM wrapper, Pydantic schemas, local JSON storage or Firestore, optional Firebase Authentication, Pillow, pandas, OpenPyXL, and python-docx.
- **Strong resume angles:** Agentic AI; multimodal document understanding; human-in-the-loop review; confidence-aware automation; educational assessment; consistency and auditability.

### 2. TestMate — AI-Powered MCQ Testing Application

- **Repository:** [imrankhankhattak/Antigravity](https://github.com/imrankhankhattak/Antigravity)
- **Project path:** `mcq-app/`
- **Summary:** Developed a full-stack AI-powered multiple-choice testing system for ingesting, organizing, and delivering customized tests.
- **Key capabilities:**
  - Uploads MCQ documents and answer keys in PDF or image format.
  - Uses a Next.js API endpoint and Google GenAI to parse questions.
  - Prevents duplicate questions using SHA-256 hashes of normalized question text.
  - Separates global/admin questions from user-isolated question banks.
  - Supports subject, topic, and difficulty filters.
  - Tracks adaptive question hardness globally and per user.
  - Uses Firestore transactions to update question and user performance records safely.
  - Provides immediate answer feedback, scoring, and repeat-test flows.
- **Technical implementation:** Next.js 16 App Router, TypeScript, CSS Modules, Firebase Authentication, Firestore, Firebase Storage, Google GenAI SDK, and Gemini Flash.
- **Strong resume angles:** Full-stack AI application; document ingestion; data modeling; adaptive learning; transactional consistency; authentication and cloud storage.

### 3. LLM-Units — Benchmarking Explainability Methods for Black-Box LLMs

- **Repository:** [imrankhankhattak/xai-llm-units](https://github.com/imrankhankhattak/xai-llm-units)
- **Summary:** Created a benchmark framework for evaluating feature attribution methods on black-box large language models using linguistically grounded unit tests.
- **Research contributions documented in the repository:**
  - Six test categories: fact retrieval, negation reversal, irrelevant-information filtering, adjective-noun interaction, multi-step reasoning, and instruction following.
  - Three API-compatible attribution approaches: token deletion, token masking, and multi-perturbation gradient approximation.
  - Evaluation with Precision@K, Recall@K, F1@K, classification F1, and Spearman rank correlation.
  - Experiments using Google Gemini through the Gemini API.
  - Analysis of API rate limits, attribution cost, scalability, and black-box explainability constraints.
- **Reported findings in README:** Multi-perturbation gradient approximation performed best among tested methods, with reported overall F1@3 of 0.36; fact retrieval was substantially easier than instruction following, negation, and multi-step reasoning.
- **Strong resume angles:** LLM interpretability research; experimental design; benchmark construction; API-based model evaluation; explainability metrics; responsible AI research.

### 4. XAI-Units — Explainable AI Benchmarking Library

- **Repository:** [imrankhankhattak/xaiunits](https://github.com/imrankhankhattak/xaiunits)
- **Summary:** Contributed to or maintained a Python library for benchmarking and comparing explainable AI feature attribution methods.
- **Capabilities documented in the repository:**
  - Synthetic and real-world datasets for weighted, conflicting, pertinent-negative, interacting-feature, uncertainty-aware, boolean, image, and text scenarios.
  - Neural-network models compatible with the datasets.
  - Wrappers for attribution methods and evaluation metrics.
  - End-to-end experiment and results pipelines.
  - AutoTrainer functionality.
  - Tutorials, examples, and Sphinx documentation.
  - Integration with methods such as Integrated Gradients, InputXGradient, and LIME, plus Captum metrics including sensitivity and infidelity.
- **Related publication:** The README references **XAI-Units: Benchmarking Explainability Methods with Unit Tests**, published in the 2025 ACM Conference on Fairness, Accountability, and Transparency.
- **Strong resume angles:** Python library development; machine learning experimentation; software packaging; documentation; reproducible XAI research.

### 5. FairTranslate — Moral Prompt Experiment for Gender Bias in Machine Translation

- **Repository:** [imrankhankhattak/Moral-Prompt-Experiment](https://github.com/imrankhankhattak/Moral-Prompt-Experiment)
- **Summary:** Investigated whether adding a fairness-oriented moral prompt can reduce gender bias in English-to-French machine translation.
- **Dataset:** 2,419 English–French sentence pairs with controlled gender variants, ambiguity labels, occupation categories, and stereotype annotations.
- **Methodology:** Compared a locally run `google/gemma-2-2b-it` model with Google Gemini 2.0 Flash under baseline and moral-prompt conditions.
- **Evaluation:** Measured gender-bias tendencies in ambiguous contexts and lexical choices such as gender-neutral alternatives.
- **Outputs:** Automated experiment script, annotated dataset, notebook, baseline results, and moral-prompt results.
- **Strong resume angles:** Fairness evaluation; prompt engineering; machine translation; dataset design; responsible AI experimentation; local-vs-cloud model comparison.

### 6. AI Policy Compass — No-Code AI Governance Tool

- **Repository:** [imrankhankhattak/ai-policy-compass](https://github.com/imrankhankhattak/ai-policy-compass)
- **Summary:** Built a no-code AI governance analysis tool using AWS PartyRock for youth, policy professionals, researchers, educators, and civil-society practitioners.
- **Capabilities:**
  - Accepts an AI deployment scenario in a country or sector.
  - Generates risk classification, OECD AI Principles analysis, stakeholder mapping, a draft policy position, and ungoverned-risk analysis.
  - Includes a follow-up chatbot for deeper questions.
  - Uses an audit-card workflow to help users identify contextual errors, missing stakeholders, and community harms.
- **Frameworks referenced:** EU AI Act, OECD AI Principles, UNESCO Recommendation on the Ethics of AI, UN Global Digital Compact, and Pakistan National AI Policy.
- **Context:** Designed for public-interest AI governance and Global South participation, including a Geneva global AI governance dialogue/event.
- **Strong resume angles:** AI governance; public-interest technology; policy translation; no-code prototyping; stakeholder-centered design; responsible innovation.

### 7. TinyStories Model Training Guide

- **Repository:** [imrankhankhattak/Training-your-own-llm](https://github.com/imrankhankhattak/Training-your-own-llm)
- **Summary:** Implemented a hands-on workflow for training a small GPT-style transformer on the TinyStories dataset.
- **Technical work:**
  - Loaded data with Hugging Face `datasets`.
  - Tokenized text with `transformers`.
  - Built a custom GPT-style transformer model in a notebook.
  - Used PyTorch for training and validation.
  - Added CUDA/GPU detection and training configuration.
  - Diagnosed an incompatible Python/PyTorch environment and moved training to Python 3.12 with CUDA-enabled PyTorch.
- **Strong resume angles:** Transformer fundamentals; PyTorch; GPU training; Hugging Face; environment debugging; practical LLM education.

### 8. AI Engineer — Pearson Career Path Examples

- **Repository:** [imrankhankhattak/AI-Engineer-Pearson-Career-Path](https://github.com/imrankhankhattak/AI-Engineer-Pearson-Career-Path)
- **Summary:** Maintained notebooks and examples associated with an AI Engineer learning path, designed to run in Google Colab.
- **Strong resume angles:** Continued professional learning; practical AI engineering exercises; notebook-based experimentation; cloud-hosted development environments.

### 9. Talk to Sigma — Conversational AI Studio Application

- **Repository:** [imrankhankhattak/Talk-to-Sigma](https://github.com/imrankhankhattak/Talk-to-Sigma)
- **Summary:** Built an AI Studio application intended to run locally with a Gemini API key.
- **Technical evidence:** Node.js application, npm-based setup, environment-based Gemini API configuration, and AI Studio deployment link.
- **Strong resume angles:** Conversational AI prototyping; Google AI Studio; Gemini integration; JavaScript/Node.js application setup.

### 10. Acts of Kindness Pakistan Website

- **Repository:** [ksherani/actsofkindness.pk](https://github.com/ksherani/actsofkindness.pk)
- **Note:** This is a collaborative repository under the `ksherani` account, not Imran's personal namespace. Include as collaborative/client/community work only if the contribution is confirmed.
- **Summary:** Developed a polished, responsive static website for a youth-focused nonprofit organization in Pakistan.
- **Features:** Mission and vision sections, six program areas, team profiles, volunteer enrollment, contact information, newsletter signup, animated calls to action, responsive layouts, semantic HTML, keyboard navigation, focus states, and accessibility support.
- **Technical implementation:** HTML5, CSS3, vanilla JavaScript, GSAP, Flowbite via CDN, Google Fonts, and static hosting/cPanel deployment documentation.
- **Strong resume angles:** Front-end development; responsive UX; accessibility; nonprofit technology; deployment and maintenance documentation.

### 11. Personal Website

- **Repository:** [imrankhankhattak/Lovable](https://github.com/imrankhankhattak/Lovable)
- **Summary:** Personal website project.
- **Available evidence:** Repository metadata describes it as a personal website; the repository README contains little additional technical detail.
- **Resume use:** Include as a portfolio/personal-brand project after confirming the live URL, stack, and personal contribution details.

### 12. GitHub Profile Repository

- **Repository:** [imrankhankhattak/imrankhankhattak](https://github.com/imrankhankhattak/imrankhankhattak)
- **Summary:** GitHub profile repository.
- **Available evidence:** Public profile README is currently minimal.
- **Resume use:** Use the profile URL as the primary portfolio link; add profile README content later if desired.

### 13. Additional `team-fti` Repository

- **Repository:** [itstalhaarshad/team-fti](https://github.com/itstalhaarshad/team-fti)
- **Note:** This is a separate repository under another account and appears to be related to the `team-fti` project. Confirm the exact contribution and role before listing it separately from [imrankhankhattak/team-fti](https://github.com/imrankhankhattak/team-fti).
- **Available metadata:** Python is listed as the primary language and the repository has a fork.

---

## Suggested Resume Skill Inventory

### AI and machine learning

- Generative AI application development
- Large language models and transformer architectures
- Gemini and Google GenAI SDK integration
- Prompt engineering and structured-output generation
- Vision-language document understanding
- Machine translation evaluation
- Explainable AI and feature attribution
- Fairness, bias, and responsible AI evaluation
- AI governance and policy analysis
- PyTorch model training and GPU/CUDA workflows
- Hugging Face Transformers and Datasets
- Captum-based interpretability experiments

### Software engineering

- Python application development
- TypeScript and JavaScript development
- Next.js full-stack applications
- Streamlit applications
- Firebase Authentication, Firestore, and Storage
- API design and integration
- Transaction-safe data updates
- Schema validation with Pydantic
- Hash-based deduplication
- Modular storage backends
- Retry and exponential backoff logic
- Data export to CSV/XLSX
- Technical documentation and reproducible setup guides

### Product and impact

- Human-in-the-loop AI systems
- Confidence-aware automation
- Adaptive learning and assessment systems
- Public-interest technology
- AI governance for Global South contexts
- Nonprofit and community websites
- Accessibility and responsive design
- Translating complex technical/policy concepts into usable tools

---

## Potential Resume Project Bullets

These bullets are drafts and should be edited to match verified role, dates, ownership, and measurable outcomes.

- Built **GradePanel**, an agentic AI grading platform that uses vision-language models to assess handwritten exam sheets against structured rubrics, return per-question marks and reasoning, flag low-confidence answers, and maintain a consistency ledger across student submissions.
- Developed **TestMate**, a Next.js and Firebase assessment platform with Gemini-powered MCQ document ingestion, SHA-256 question deduplication, user-isolated question banks, adaptive difficulty scoring, and transactional Firestore updates.
- Designed **LLM-Units**, a linguistic unit-testing benchmark for black-box LLM explainability, implementing deletion, masking, and multi-perturbation attribution methods and evaluating them with Precision@K, Recall@K, F1, classification metrics, and rank correlation.
- Built and documented an **XAI benchmarking library** with synthetic datasets, neural-network models, attribution-method wrappers, evaluation metrics, experiment pipelines, tutorials, and automated training utilities.
- Conducted a **FairTranslate** study comparing baseline and fairness-prompted LLM translation behavior across 2,419 annotated English–French occupation sentence pairs to investigate gender bias and inclusive lexical choices.
- Created **AI Policy Compass**, a no-code AWS PartyRock tool that translates AI deployment scenarios into risk classifications, OECD principles analysis, stakeholder maps, policy positions, and ungoverned-risk assessments.
- Trained a custom GPT-style transformer on TinyStories using PyTorch, Hugging Face tooling, and CUDA, while documenting Python/PyTorch compatibility troubleshooting and reproducible GPU setup.
- Built a responsive nonprofit website for **Acts of Kindness Pakistan** with accessible semantic HTML, GSAP animations, mobile-first layouts, volunteer enrollment, team profiles, and deployment documentation.

---

## Evidence and Verification Checklist

Before using this document to produce a final resume, verify:

- Exact project dates and duration.
- Whether each project was solo, collaborative, academic, professional, or experimental.
- Your exact role and contribution in collaborative repositories.
- Quantitative impact: users, papers, datasets, performance improvements, deployment usage, or time saved.
- Publication authorship and relationship to the XAI-Units repositories.
- Live deployment URLs and whether they remain active.
- Employment titles, organization names, and dates.
- Education, certifications, awards, talks, workshops, and community leadership not represented by repositories.
- Whether reported benchmark results are final, reproducible, or illustrative.

---

## LLM Instructions

When using this document to create a resume:

1. Do not invent employers, job titles, dates, metrics, users, awards, or responsibilities.
2. Distinguish verified personal repositories from collaborative repositories.
3. Prefer the strongest 3–5 projects for the target role rather than listing everything.
4. Tailor project selection to the job: AI engineer, ML engineer, AI safety/governance, XAI researcher, full-stack AI developer, or education technology.
5. Convert technical details into outcome-oriented bullets.
6. Preserve uncertainty where this document explicitly says that ownership or contribution must be confirmed.
7. Ask for missing dates, role titles, measurable outcomes, and education details before finalizing a one-page resume.
