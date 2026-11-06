# CA-Judge
Code and data for the paper: CA-Judge: Teach Large Models to Judge Anomalies via Comparison for Video Anomaly Detection.

# Overview

![CA-Judge Framework](./pipeline_nips2026.png)

Video anomaly detection (VAD) is critical for identifying safety risks in surveillance and autonomous systems. Recent large-model-based VAD methods generate textual rationales and directly output anomaly scores. However, mapping rich semantic descriptions and analysis directly to absolute scalar scores can be poorly grounded and inconsistent, leading to scores that are not well aligned with anomaly severity. With the observation that for humans, it is usually easier to compare things than to rate things directly, we explore whether it also holds for large models in VAD by proposing **CA-Judge** (**C**omparative **A**nomaly **Judge**), a training-free framework that replaces direct scoring with comparative order inference. CA-Judge treats model-perceived anomaly severity as a latent coordinate, constructs this coordinate from self-comparisons among generated normal/anomalous reference events, and models how anomaly likelihood varies along this coordinate using the generated normal/anomalous reference identities. At test time, CA-Judge avoids exhaustive comparison by maintaining a posterior belief over query severity and selecting a few query--reference comparisons by their expected information about the anomaly status. The resulting comparison trace is aggregated under a Bradley--Terry likelihood and read out through the learned severity--anomaly association to produce the anomaly probability. Without fine-tuning or training data, CA-Judge substantially improves over direct-scoring baselines and surpasses prior training-free state-of-the-art methods on UCF-Crime and XD-Violence.


# Update
Repo initialized. Code is coming soon.
