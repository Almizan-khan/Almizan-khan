# Almizan Khan

**AI / ML engineering · Python · PyTorch · LLM applications**

I build machine-learning experiments and AI workflows, with a growing focus on genomic sequence modeling. My projects connect model implementation with evaluation, tests and usable interfaces.

Based in Kanpur, India. Interested in AI/ML engineering and research engineering opportunities.

[LinkedIn](https://www.linkedin.com/in/almizan-khan-349298334/) · [Project evidence](PORTFOLIO.md) · [Engineering decisions](ENGINEERING.md)

## Selected projects

| Project | Engineering focus | Evidence to inspect |
|---|---|---|
| [DNA Transformer](https://github.com/Almizan-khan/-DNABERT-Style-Transformer-From-Scratch) | Custom attention, DNA BPE, masked pretraining, genomic-region splits | Real E. coli experiment, frequency baseline, split manifest and masking tests |
| [Transformer from scratch](https://github.com/Almizan-khan/transformers-from-scratch) | Encoder–decoder attention, causal masking, trainable embeddings | Autoregressive held-out evaluation and attention-reference tests |
| [InsightWeaver](https://github.com/Almizan-khan/insightweaver-agent) | Parallel LangGraph branches, structured outputs, provider adapters | Exactly-once stage tests, failure handling and explicit offline/live modes |
| [Tabular regression](https://github.com/Almizan-khan/Gradient-Boosting-pipeline) | CatBoost cross-validation, OOF predictions, saved fold models | Three-seed comparison against mean and Ridge baselines |
| [MNIST CNN](https://github.com/Almizan-khan/CNN-with-PyTorch) | PyTorch training, checkpoint selection and image inference | **98.50% official test accuracy**, confusion matrix and reproducible workflow |
| [Rule-conditioned classifier](https://github.com/Almizan-khan/Rule-Violation-Classifier) | DeBERTa, explicit classification loss, grouped splits | Loss/gradient tests, TF-IDF baseline path and per-rule error reports |

## Measured experiments

- **MNIST:** 98.50% accuracy on 10,000 official test images after validation-based checkpoint selection; seed 42, five epochs.
- **Sequence copy:** 68.75% exact match on 256 held-out sequences after 2,000 steps. This is a small algorithm-learning task, not a language-model benchmark.
- **DNA masked modeling:** held-out cross-entropy 4.8491 versus 4.9527 for a train-token-frequency baseline in a small, single-genome E. coli experiment.
- **Tabular regression:** Ridge beats the fixed-budget CatBoost configuration on the bundled diabetes reference dataset. Both results are retained.

Each result links to raw metrics, configuration and an executed GitHub Actions run through the [evidence index](PORTFOLIO.md). Live-provider prototypes and synthetic checks are labeled separately from model-quality measurements.

## Additional work

[SwarLab — Harmonium Ear Trainer](https://swarlab-staging.onrender.com/): live practice app with an interactive harmonium, melody and chord exercises, Firebase sign-in, and a FastAPI/PostgreSQL backend.

[Wellness reflection demo](https://github.com/Almizan-khan/-Mental-Health-Assistant): FastAPI, SQLite sessions, validation and a local interface. An educational application, not a clinical assessment.

[DreamBooth furniture concept](https://github.com/Almizan-khan/-Sofa-Fine-Tuning-using-DreamBooth): image manifests, reproducible training commands and paired base/fine-tuned evaluation. Image-quality results require the actual dataset and checkpoint.

## Current technical direction

I am deepening my work in reliable model evaluation, Transformer internals and genomic ML. The next experiments are multi-seed ablations, stronger sequence-similarity holdouts and comparisons that measure quality alongside runtime and cost.
