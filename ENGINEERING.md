# Engineering decisions across the projects

## Make comparisons inspectable

The CNN separates training, validation and the official test set. The Transformer evaluates generated sequences rather than teacher-forced predictions. The DNA model records genomic coordinates and a training-only tokenizer. The tabular reference experiment retains a simpler baseline even when it wins.

These choices answer different failure modes: selecting on test data, measuring an easier inference setup, leaking sequence/tokenizer information, and mistaking model complexity for improvement.

## Separate correctness from quality

An attention implementation can pass a numerical reference test while its trained model performs poorly. A five-stage agent can execute correctly while producing weak advice. The repositories therefore keep regression tests, model experiments and provider-dependent quality evaluation separate.

Tests exercise behavior with real failure consequences: future-token leakage, invalid class-loss semantics, duplicate-comment leakage, malformed provider responses, unsafe HTML rendering and conflicting session writes. Synthetic latency checks are labeled with the exact model/input scope.

## Preserve working interfaces while fixing reproducibility

Historical notebooks and READMEs retain the learning trail. Maintained entry points use configurable paths, dependency manifests and environment-based credentials. Training artifacts include the configuration needed to reload models; data and large weights stay out of source control.

The agent uses separate state fields for parallel branches and merges only new timing events. The wellness demo uses revision-checked SQLite updates. Both default to an explicit offline mode so the application path can be inspected without spending API credits.

## Next experiments with the highest value

1. **Genomic generalization:** use sequence-cluster or species holdouts and a downstream labeled task. Compare BPE and k-mers at equal parameter and training budgets; report several seeds.
2. **Agent efficiency:** compare the graph with one structured model call on a fixed reviewed case set. Measure grounding, failure counts, tokens and latency together.
3. **Transformer depth:** vary causal masking, positional encoding and model width in controlled experiments, then inspect failure patterns beyond the training sequence length.
4. **Operational depth:** select one application and add authenticated access, structured tracing, deployment tests and measured concurrent-load behavior before calling it production-ready.

These are concrete extensions of the current projects, not claims that the work is already complete.
