# Greenwatt Sim

A drop in GPU cluster + wholesale electricity simulator that lets any operator paste 7 days of nvidia smi + wholesale market CSVs and see exactly what a DeepAware style RL scheduler would have done - and saved - in their own facility.

## Why This Exists

DeepAware promises a 30% energy waste cut and a 15% pilot validation, but the only public artifact backing those numbers is a single paragraph claim on the YC launch page. For a sales motion targeting mid market operators (who don't have Google's published TPU efficiency papers to lean on) the missing primitive is a reproducible, vendor neutral, simulator backed benchmark that lets a prospective operator answer "what would DeepAware actually save me?" before signing.

## What It Builds

- Replays synthetic `deepaware` and `promises` cases against the project's evidence rules.
- Scores `deepaware_coverage`, `promises_risk`, and `energy_precision` so regressions are visible in CSV and JSON.
- Plants `deepaware drift` and `promises gap` failures as negative controls.
- Writes citation-locked decision claims; unsupported claims fail verification.
- Exports a review dashboard and demo pack for `greenwatt-sim` without hosted services.

## Local Run

```bash
uv sync
uv run greenwatt-sim all
uv run pytest -q
uv run ruff check .
```

## Outputs

- `outputs/analysis.json`
- `outputs/scenario_report.csv`
- `outputs/decision_report.md`
- `outputs/evidence_packet.md`
- `outputs/dashboard.html`
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

This repository uses synthetic fixtures only. It has no credentials, no customer data, no outreach data, and no dependency on a hosted API.
