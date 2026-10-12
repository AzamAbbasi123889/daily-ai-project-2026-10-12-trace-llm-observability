# Implementation Checklist

Build the application yourself using `PROJECT_BRIEF.md`.

## Initial setup

- [ ] Read the project specification.
- [ ] Review the architecture and data model.
- [ ] Create a Python virtual environment.
- [ ] Install and pin the required dependencies.
- [ ] Configure credentials through environment variables.
- [ ] Review the data privacy and security requirements.

## Project acceptance criteria

- [ ] HTTP 200 returns a trace_id
- [ ] Latency recorded in ms
- [ ] Prompt, response and metadata saved in PostgreSQL
- [ ] Eval score persisted with the trace
- [ ] Score is reproducible for identical inputs
- [ ] Prometheus metrics visible at /metrics
- [ ] Dashboard graphs update within 5 seconds of a new trace
- [ ] All four charts load with data from at least 10 traces
- [ ] Filters correctly adjust the displayed data
- [ ] Initialize repo with Docker‑Compose (Postgres, Redis, FastAPI, React)
- [ ] Implement /traces endpoint and LangChain LLM call
- [ ] Add OpenTelemetry instrumentation and /metrics endpoint
- [ ] Create Evaluation Service using a second LLM call
- [ ] Build React dashboard with four charts
- [ ] Write unit & integration tests, set up GitHub Actions
- [ ] Unit tests for each FastAPI route using pytest‑asyncio
- [ ] Integration test that submits a prompt and verifies DB record, span, and eval_score
- [ ] Load test with Locust: 100 concurrent users for 2 min, assert 95th‑pct latency < 1 s
- [ ] Security test: ensure API key header required for /traces, verify rate limiting (50 rpm)
- [ ] Schema validation test: response JSON conforms to defined OpenAPI spec
- [ ] Build multi‑stage Docker images (backend & frontend)
- [ ] Push to Docker Hub (or GitHub Container Registry)
- [ ] Deploy via Docker‑Compose on a cheap VPS (e.g., Hetzner) or Render free tier
- [ ] GitHub Actions workflow: lint → test → build → push → trigger remote deploy
- [ ] Configure Prometheus + Grafana on the same host for optional advanced dashboards

## Before completion

- [ ] Implement the planned MVP features.
- [ ] Add unit and integration tests.
- [ ] Run the test suite.
- [ ] Measure the evaluation metrics in the brief.
- [ ] Record actual results and known limitations.
- [ ] Document setup and deployment.
- [ ] Update the README to reflect the implemented features.
- [ ] Add only verified outcomes to your resume.
