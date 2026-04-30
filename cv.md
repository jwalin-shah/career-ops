# Jwalin Shah

Fremont, CA · (408) 908-9659 · jwalinshah13@gmail.com
github.com/jwalin-shah · linkedin.com/in/jwalin-shah · huggingface.co/jshah13

**Builds and ships open-source, local-first AI tools — and the evaluation infrastructure to know they actually work.**

AI Systems Engineer · LLM Evaluation & Reliability · Tool-Augmented Reasoning · Local/On-Device AI · Developer Tooling

## Selected Impact

- **Evaluation at Scale** — Built telemetry across 3,600+ tasks; identified retrieval errors and tool selection (not model reasoning) as the dominant failure source in grounded LLM systems.
- **LLM Reliability** — Demonstrated deterministic computation pipelines cut hallucination rates to <5% on real-world financial tasks.
- **Competition Result** — Ranked 7th place (Team: Zero Node) on a 246-task financial reasoning benchmark at Sentient Arena Cohort 0.
- **Open-Source Developer Tools** — Author of memjuice (Rust, Homebrew); core contributor to OpenHuman (39+ merged PRs across Rust core, RPC, memory, and notification systems).
- **Real-World Systems** — Scaled robotics data operations to 30+ operators across five platforms; ~40% task success improvement, ~50% overhead reduction.

## Technical Skills

- **AI Systems:** Tool-augmented LLMs, retrieval pipelines (BM25 + embeddings), structured extraction, deterministic computation, on-device inference (MLX, Apple Silicon)
- **Eval & Reliability:** Benchmark harnesses, telemetry, failure mode analysis (tool thrashing, retrieval errors, temporal misalignment), hallucination measurement, RL environments
- **Stack:** Python, Rust, SQL, Bash, FastAPI, SQLite + sqlite-vec, MLX, DSPy, TensorFlow, MediaPipe, Textual TUI

## Professional Experience

### Sentient Arena (Cohort 0) — Research Contributor, Grounded Reasoning
*March 2026 · Team: Zero Node (7th place, 246-task benchmark)*

- Built multi-agent LLM system for grounded financial reasoning; replaced in-model arithmetic with structured retrieval + deterministic computation.
- Developed evaluation infrastructure across 15+ runs (3,600+ tasks) analyzing stochastic behavior, tool use patterns, and system-level performance.
- Identified retrieval errors and tool selection — not model reasoning — as dominant failure source, validated across 3,600+ evaluations.
- Improved accuracy via tool prioritization, forced-answer heuristics, and database architecture changes.

### Skild AI — Data Operations Lead (ML Systems & Reliability)
*San Mateo, CA · Jul–Nov 2025*

- Built and scaled data validation and collection systems across five robotic platforms supporting model training and evaluation.
- Developed Python automation pipelines reducing operational overhead by ~50% and improving downstream task success by ~40%.
- Primary technical operator for 25+ live robot demos during $1B Series C; maintained zero-failure execution under pressure.
- Debugged edge-case failures in perception, manipulation, and locomotion systems in real-world deployment environments.

## Featured Projects

### memjuice — Cross-Harness Transcript→Context Codec
*[GitHub](https://github.com/jwalin-shah/memjuice) · Rust · Homebrew · Inspired by tokenjuice and rtk*

- Single-binary tool that reads session JSONL from Claude Code, Codex, Cursor, Aider, Continue, and Gemini CLI; extracts six observation types via deterministic regex and structural rules — no LLM, no API key, offline, hand-editable plain-text ledger.
- Sub-100ms `recall` over JSONL; supersession logic (Type A/B/C) keeps the ledger from going stale as decisions evolve across sessions.
- Empirically grounded: cross-harness audit of 14,718 Claude + 69 Codex sessions on one machine before designing the extraction rules.
- Same "deterministic > LLM in the hot path" philosophy as tokenjuice and rtk — install friction zero, cross-harness, predictable.

### OpenHuman — Local-First Agentic Desktop Assistant
*Core contributor · [tinyhumansai/openhuman](https://github.com/tinyhumansai/openhuman) · Rust core + TS desktop*

- 39+ merged PRs across core systems: memory namespaces with recall citations, provider-surfaces RPC, daemon lifecycle + retry hardening, core→shell DomainEvent notification bridge.
- Test infrastructure contributions: cross-process cron e2e, threads schema parse contract tests, RPC/registry edge-case coverage.
- On-device knowledge base, locally-encrypted workflow data, native desktop integrations (STT/TTS, screen intelligence) — privacy posture aligned with Jarvis and inbox.

### Jarvis — Local-First AI Assistant
*[GitHub](https://github.com/jwalin-shah/jarvis-ai-assistant) · 736 commits · DeveloperWeek 2026 Hackathon*

- Privacy-first assistant on Apple Silicon (8GB M2 Air): MLX inference + SQLite/sqlite-vec retrieval, zero cloud dependencies.
- Dual-path architecture: fast-path (mean latency 0.42s, p95 1.15s, ~230 tok/s) for simple queries; background pipeline for complex grounded reasoning.
- Evaluation harness across 37 model configs: retrieval hit@5 0.88, hallucination gate pass rate 96.2%, classifier p50 12ms, retrieval p50 3ms.

### inbox — Privacy-First Unified Communications TUI
*[GitHub](https://github.com/jwalin-shah/inbox)*

- Terminal UI consolidating iMessage, Gmail, Google Calendar, Google Sheets, Apple Notes, Apple Reminders, GitHub notifications, and Google Drive — zero cloud middleware.
- Local ML: MLX Whisper (transcription) + Qwen 3.5 0.8B (MLX 4-bit) for on-device AI; ambient audio capture and AI autocomplete.
- FastAPI + Textual architecture with direct macOS data integrations and multi-account Gmail routing.

### data-connect-framework — Local-First Personal Data Engine
*[GitHub](https://github.com/jwalin-shah/data-connect-framework)*

- Schema-driven ingestion, canonical entity modeling, and local-first data pipelines for personal data infrastructure.

### OpenEnv / RoboRePlan — RL Environment Design
*OpenEnv Hackathon 2026 · [GitHub](https://github.com/jwalin-shah/robo-replan) · [HuggingFace](https://huggingface.co/jshah13)*

- Custom RL environment simulating a robot arranging blocks to placement instructions; FastAPI state transitions and multi-dimensional reward.
- GRPO training with ~80% success baseline; published on Hugging Face (jshah13/robo-replan-grpo).

### Squat Coach — On-Device Biomechanics Coaching
*InstaLILY AI Hackathon*

- Real-time exercise analysis using MediaPipe pose estimation with temporal smoothing for joint angle tracking on consumer hardware.

## Research & Analysis

- Systematic failure analysis across 3,600+ LLM benchmark evaluations quantifying error attribution across system components.
- Demonstrated deterministic computation + structured extraction reduces hallucination rates from baseline to <5%.

## Education & Leadership

### University of Texas at Dallas — B.S. Computer Science
*GPA: 3.67*

- **UTD Ultimate Frisbee — Captain:** Led 30-member competitive program through recruitment, budgeting ($20K+), and tournament logistics.
- **UTD Chess Club:** USCF 1832 (91st percentile). Trained with GMs/FMs; coached 50+ students in positional analysis.
