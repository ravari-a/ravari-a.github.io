---
layout: page
title: "Personalized Models of Cyber Defenders"
description: "Inferring individual defenders' cognitive traits from limited behavioral data, validated with 108 participants."
img: assets/img/proj-personalized-cyber-defense.png
importance: 2
category: cybersecurity
related_publications: true
---

**Paper:** [Google Scholar](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=rJhy860AAAAJ&citation_for_view=rJhy860AAAAJ:UeHWp8X0CEIC) · [Publisher](https://doi.org/10.1109/TAI.2025.3640159)

AI support in cyber defense works best when it adapts to the person it supports. Defenders differ in risk tolerance, curiosity and other traits that shape their decisions, and these differences are hard to infer from the small amount of behavior one person produces. The goal is to understand individual behavior rather than replicate it, so that assistive systems can calibrate trust, assign roles, personalize training and give different guidance to novices and experts.

This project formulates each defender's decision-making as a Markov decision process and proposes a kernel-based inverse learning framework. Kernel-density estimation over reference trajectories with known traits lets the method infer a new user's latent traits from limited data and generate a personalized policy.

<div class="row justify-content-sm-center">
  <div class="col-sm-12 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/proj-personalized-cyber-defense-fig1.png" alt="Kernel-based inverse learning. A user's behavioral data are compared with reference trajectories of known latent factors through kernel-density estimation, giving the user's inferred factors and a personalized policy." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Kernel-based inverse learning. A user's behavioral data are compared with reference trajectories of known latent factors through kernel-density estimation, giving the user's inferred factors and a personalized policy.
  <br><span class="figure-credit">© 2025 IEEE. Reprinted from A. Ravari et al., <i>IEEE Transactions on Artificial Intelligence</i>, 2026.</span>
</div>

The approach was validated with a psychological survey of 108 participants in the TTCP CAGE Challenge 2 testbed. It recovers individual traits accurately and keeps strong predictive accuracy under sparse data. The similarity between predicted and actual actions exceeds 0.8 in every participant group, while a group-level RL baseline stays at or below 0.6. The method also estimates traits more accurately than GPT-4o and an LSTM-encoder baseline.

<div class="row justify-content-sm-center">
  <div class="col-sm-9 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/proj-personalized-cyber-defense-fig2.png" alt="The CAGE Challenge 2 network used in the study, with user hosts, enterprise servers and an operational server. Participants act as the defender against an adversary." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  The CAGE Challenge 2 network used in the study, with user hosts, enterprise servers and an operational server. Participants act as the defender against an adversary.
  <br><span class="figure-credit">© 2025 IEEE. Reprinted from A. Ravari et al., <i>IEEE Transactions on Artificial Intelligence</i>, 2026.</span>
</div>

Published in *IEEE Transactions on Artificial Intelligence, 2026* {% cite ravari2025personalized %}.
