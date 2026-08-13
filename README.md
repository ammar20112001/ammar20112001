# Ammar Jawed — ML Engineer

**Research depth meets production engineering.**

[LinkedIn](https://www.linkedin.com/in/ammarjawed/) · [X](https://x.com/ammar_20112001) · [Email](mailto:ammarjawed.1111@gmail.com)

---

## About

I design and implement models from first principles — custom loss functions, novel architectures, from-scratch reproductions — then own the full path to deployment: fault-tolerant backends, distributed training (8× A100 / DDP), async job orchestration, and serving.

I've shipped production systems across document intelligence, agentic LLM pipelines, spatial-flow modelling, and computer vision — equally comfortable reading a paper and building the system it describes.

📍 Pakistan / Kuwait · open to remote, worldwide

## Experience

**ML Engineer — Appedology** · Dec 2024 – present

Lead end-to-end production ML systems:

- [**Data Analytics & Intelligence Platform**](https://claude.ai/code/artifact/6602461b-f649-477a-b392-e18f6c276818) — full-stack market-intelligence dashboard (FastAPI, Vue 3, MySQL/Redis) replacing manual analyst workflows with self-service market segmentation (custom hierarchical clustering), a proprietary competitive-share metric, and demographic-driven office-placement recommendations.
  - [**ZIP-level demand forecasting**](https://claude.ai/code/artifact/d4a6e836-ca4f-4307-beca-f70c303edbf9) — XGBoost (Poisson) model predicting patient-panel volume 1–12 months out across 32 specialties; shipped as an independent FastAPI microservice with zero-downtime, API-triggered retrain-and-hot-swap, tracked in W&B.
  - **Agentic analytics assistant** — turns plain-English questions into governed SQL + sandboxed Python over a live warehouse. Structural safety (read-only DB role, zero write-tools asserted in CI, per-execution container teardown) with durable turn-state surviving process restarts and multi-hour human approvals; SSE-streamed reasoning. FastAPI + React + MySQL, Docker, Langfuse.
  - **Lead-scoring & competitor analytics** — resolves QME-to-company relationships, quantifies boarding impact, and ranks outreach leads across categories.
- **Applied research — spatial-flow modelling** — optimal-transport neural network with custom temporal encoders and multi-head attention to model regional flows and surface high-impact locations; owned the full data-curation → training → evaluation lifecycle.
- **Medical Scribe Agent** — end-to-end agentic system: Playwright browser automation, local Whisper transcription, LLM extraction, and deterministic PDF/DOCX report rendering — split into a FastMCP tools microservice and a React/FastAPI orchestration layer communicating over MCP, so browser-automation and LLM-inference workloads scale independently.
- **Document-intelligence pipeline** — converts complex medical & financial documents into structured relational JSON; fault-tolerant backend with async job orchestration via RabbitMQ, retry guarantees, and audit logging.

## Selected Work

[**AI-Generated Video Detection**](https://claude.ai/code/artifact/eae853e5-854a-4479-a5f3-5838f8aaaceb) — Curated ~1.5 TB of video end-to-end (frame sampling, augmentation, RAFT optical flow). Trained semantic (XCLIP / DeMamba) and motion-based (AIGVDet) models from scratch with DDP on 8× A100 GPUs; feature-level fusion with gradual unfreezing to avoid catastrophic forgetting. **~90% val / ~85% on unseen holdout.**

**Privacy-Preserving Fraud Detection** — Rate-coded Spiking Neural Network (custom LIF neurons) + Fully Homomorphic Encryption for inference directly on encrypted inputs — end-to-end private predictions, raw data never exposed.

**Transformer, reproduced from scratch** — Full architecture in vanilla PyTorch (multi-head attention, positional encoding, encoder–decoder) in a modular framework with training, hyperparameter search, and serverless deployment. → [repo](https://github.com/ammar20112001/Attention-Is-All-You-Need--reproduced)

**Real-Time Multilingual Speech Translation** — Speech-to-speech translation for medical / enterprise use cases; live on Hugging Face Spaces. → [repo](https://github.com/ammar20112001/Real-Time-Translation--GenAI)

## Stack

- **Languages** — Python, C/C++, SQL
- **ML / DL** — PyTorch, PyTorch Lightning, Hugging Face Transformers
- **LLM / Agents** — LangChain, LangGraph, OpenAI & Anthropic APIs
- **Backend / Systems** — FastAPI, Flask, RabbitMQ, async job orchestration, REST APIs
- **Data** — Pandas, NumPy, Scikit-learn, Matplotlib
- **Cloud / Infra** — AWS (EC2, S3, Lambda, EBS), Azure, Docker, Distributed Training (DDP)
- **Tooling** — Weights & Biases, Git, Hugging Face Spaces
