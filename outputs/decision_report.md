# Decision Report: Greenwatt Sim

A drop in GPU cluster + wholesale electricity simulator that lets any operator paste 7 days of nvidia smi + wholesale market CSVs and see exactly what a DeepAware style RL scheduler would have done - and saved - in their own facility.

## Evidence-Grounded Findings

CLAIM: deepaware drift should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=2.5. [EVID: ev_0022]
CLAIM: deepaware evidence recall should `block release until replay is understood` because blocks=3 reviews=3 mean_severity=1.875. [EVID: ev_0000]
CLAIM: energy failure replay should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=3.333. [EVID: ev_0044]
CLAIM: promises gap should `block release until replay is understood` because blocks=3 reviews=2 mean_severity=3.333. [EVID: ev_0077]
CLAIM: promises reviewer handoff should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=2.583. [EVID: ev_0121]
CLAIM: waste policy boundary should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=1.708. [EVID: ev_0099]
