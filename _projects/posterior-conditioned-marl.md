---
layout: page
title: "Posterior-Conditioned Multi-Agent Cyber Defense"
description: "Decentralized defenders that adapt online to a shared belief about the active attack regime."
img: assets/img/proj-posterior-conditioned-marl.png
importance: 3
category: cybersecurity
related_publications: true
---

**Paper:** [Google Scholar](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=rJhy860AAAAJ&citation_for_view=rJhy860AAAAJ:Tyk-4Ss8FVUC) · [Publisher](https://doi.org/10.1016/j.artint.2026.104606)

Cyber defense increasingly relies on teams of autonomous agents that act on partial observations while adversaries shift tactics and objectives over time. Standard multi-agent reinforcement learning tends to overfit to fixed threat models. Worst-case robust training, in turn, can be overly conservative and ignores what the defenders observe about the active attack.

This work formulates defense as a decentralized partially observable Markov decision process (Dec-POMDP). Each defender conditions its policy on its local history and on a shared attack-context belief, a posterior over attack regimes inferred online from recent multi-agent trajectories. Defenders act conservatively while the regime is uncertain and specialize as evidence accumulates, with no test-time optimization or retraining. A performance analysis shows how errors in the inferred belief translate into lost long-term reward, which makes the tradeoff between robustness and adaptivity explicit.

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/proj-posterior-conditioned-marl-fig1.png" alt="Defense agents act independently on their local observations and a shared posterior over the unknown adversarial regime. The posterior is updated as new observations arrive." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Defense agents act independently on their local observations and a shared posterior over the unknown adversarial regime. The posterior is updated as new observations arrive.
  <br><span class="figure-credit">From A. Kazeminajafabadi et al., <i>Artificial Intelligence</i>, 2026, published under a <a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a> license.</span>
</div>

On the CybORG CAGE-4 testbed, posterior conditioning improves mission reward and adaptability over domain-randomized, worst-case robust and hierarchical baselines, particularly under mixed and switching attacks.

<div class="row justify-content-sm-center">
  <div class="col-sm-9 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/proj-posterior-conditioned-marl-fig2.png" alt="Average accumulated defense reward under mixed attack distributions (higher is better): the proposed defense (blue), GNN and hierarchical MARL baselines trained with domain randomization (orange, red), and an upper bound (green)." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Average accumulated defense reward under mixed attack distributions (higher is better): the proposed defense (blue), GNN and hierarchical MARL baselines trained with domain randomization (orange, red), and an upper bound (green).
  <br><span class="figure-credit">From A. Kazeminajafabadi et al., <i>Artificial Intelligence</i>, 2026, published under a <a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a> license.</span>
</div>

Published in *Artificial Intelligence, 2026* {% cite kazeminajafabadi2026posterior %}.
