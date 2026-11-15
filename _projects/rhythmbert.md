---
layout: page
title: "RhythmBERT: Reading ECGs as a Language"
description: "A self-supervised ECG language model that turns each heartbeat into tokens for its P, QRS and T waves."
img: assets/img/proj-rhythmbert.png
importance: 1
category: biomedical AI
related_publications: true
---

**Paper:** [Google Scholar](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=rJhy860AAAAJ&citation_for_view=rJhy860AAAAJ:IjCSPb-OGe4C) · [Publisher](https://doi.org/10.1109/ICASSP55912.2026.11461030)

Most self-supervised methods for electrocardiograms (ECGs) treat the signal as a generic time series. Contrastive methods rely on augmentations that distort waveform morphology. Generative methods cut the signal into fixed windows that do not align with cardiac cycles.

RhythmBERT treats the ECG as a language. Autoencoder-based tokenizers encode each P, QRS and T wave as a symbolic token, so every heartbeat becomes a short sentence over a learned wave vocabulary. Continuous embeddings keep the fine-grained morphology alongside the discrete tokens. The model is pretrained with masked prediction on about 800,000 unlabeled recordings and uses only Lead II. I co-developed RhythmBERT as a LEADERs Fellow working with Walkky.

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/proj-rhythmbert-fig1.png" alt="RhythmBERT overview. P, QRS and T waves map to cluster IDs from a learned wave vocabulary and form heartbeat sentences. Token, positional and morphology embeddings feed a Transformer encoder trained with masked prediction." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  RhythmBERT overview. P, QRS and T waves map to cluster IDs from a learned wave vocabulary and form heartbeat sentences. Token, positional and morphology embeddings feed a Transformer encoder trained with masked prediction.
  <br><span class="figure-credit">© 2026 IEEE. Reprinted from X. Wang et al., <i>IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)</i>, 2026.</span>
</div>

Despite using a single lead, RhythmBERT matches or exceeds strong 12-lead baselines. With all labels, it reaches a macro AUROC of 82.38 on CPSC2018 and 94.11 on Chapman–Shaoxing, against 77.87 and 82.49 for the best 12-lead baseline. On PTB-XL, the 12-lead HeartLang remains stronger. Performance holds from common conditions such as atrial fibrillation to harder cases such as subtle ST-T abnormalities and myocardial infarction.

Published in *IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), 2026* {% cite wang2026rhythmbert %}.
