# Greenwatt Sim

A drop in GPU cluster + wholesale electricity simulator that lets any operator paste 7 days of nvidia smi + wholesale market CSVs and see exactly what a DeepAware style RL scheduler would have done - and saved - in their own facility.

![Greenwatt Sim working dashboard](outputs/project_working.svg)

## Why it exists

DeepAware promises a 30% energy waste cut and a 15% pilot validation, but the only public artifact backing those numbers is a single paragraph claim on the YC launch page.

Most internal demos stop at a pretty chart. This repository is built around the harder part: a repeatable path from fixture, to failure, to evidence, to the operator action a serious team would actually trust.

## What is inside

- A deterministic replay harness tuned around deepaware, promises, and energy.
- Company-specific strategy code in `src/greenwatt_sim/strategy.py`, not just README-level customization.
- Citation-locked reports where every decision claim has to point back to a generated evidence ID.
- Two visual artifacts generated from the latest run: `outputs/project_working.svg` and `outputs/evidence_map.svg`.
- A portable demo pack with JSON, CSV, Markdown, HTML, SVG, and benchmark artifacts.

![Greenwatt Sim evidence map](outputs/evidence_map.svg)

## Signals it measures

- `deepaware coverage`
- `promises risk`
- `energy precision`
- `waste latency`

## Failure modes it plants

- deepaware drift
- promises gap
- energy misroute
- waste blindspot

## Run it locally

```bash
uv sync
uv run greenwatt-sim all
uv run pytest -q
uv run ruff check .
```

## Outputs worth opening

- `outputs/dashboard.html`
- `outputs/project_working.svg`
- `outputs/evidence_map.svg`
- `outputs/operator_brief.md`
- `outputs/decision_report.md`
- `outputs/strategy_model.json`
- `outputs/demo_pack.zip`

## Sources

- https://www.ycombinator.com/launches/OBl-deepaware-automation-for-next-gen-ai-data-centers
- https://www.deepawareai.com/product
- https://www.deepawareai.com/
- https://www.ycombinator.com/companies/deepaware-ai/jobs
- https://www.deepawareai.com/knowledge-base/ireland-data-center-regulation
- https://www.greenai.institute/profile/jerry-huang
- https://www.greenai.institute/news/2025-Second-Green-AI-Summit-Concludes
- https://www.greenai.institute/news/green-ai-summit-concludes-with-major-steps-toward-sustainable-development
- https://sustainable.harvard.edu/person/jerry-huang/
- https://www.linkedin.com/in/jerryh01/

## Boundary

Everything runs locally against synthetic fixtures. There are no credentials, no customer records, no outreach files, and no hosted API dependency.
