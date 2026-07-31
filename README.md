Title:

τ-Guard: Recalibration-Invariant, Label-Free Drift Detection for Visual Recognition Systems via Cross-Signal Rank-Agreement Decay

Abstract:

Vision systems in production are routinely monitored for silent degradation using only their own outputs, since ground-truth labels are typically unavailable at deployment time. Existing label-free monitors implicitly assume the model's confidence is stably calibrated; when a model is merely recalibrated (temperature or Platt scaling) with no change to the input distribution, these monitors mistake recalibration for drift. We introduce τ-Guard, a label-free signal monitoring the rank agreement (Kendall's τ) between predictive entropy and an independent feature-space novelty score, provably invariant to monotone recalibration — proven exactly via a lemma and bounded analytically for multiclass temperature scaling. We validate this on a classical image benchmark and, critically, on genuine deep-vision pipelines: two real pretrained CNNs (ResNet-20, RepVGG-A0) on real CIFAR-10 under real corruptions, plus a real CLIP foundation model on real cross-domain photographs (PACS), alongside six other datasets, three classifier families, six label-free methods (including STUDD and D3, reimplemented here), an energy-based novelty-score ablation, and a CUSUM sequential-testing comparison. Pooled over thousands of trials, two standard baselines collapse from a well-calibrated false-positive rate to near-total failure under pure recalibration — including on both architectures and on real CLIP embeddings — while τ-Guard's rate is unchanged. Under genuine shift with simultaneous recalibration, τ-Guard's signal is preserved or strengthened on most datasets, while baselines' alerts become uninformative once saturated. We report limitations as directly as strengths: architecture- and corruption-dependent sensitivity, a costlier baseline (D3) with better sensitivity, and what remains untested at ImageNet scale, for object detection, and for larger transformers.

Keywords:

drift detection, computer vision monitoring, model calibration, out-of-distribution detection, Kendall's tau, visual recognition systems, MLOps
