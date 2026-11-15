---
layout: page
title: "Human-Factor-Aware Inverse Learning for Cyber Defense"
description: "Learning operator-specific defense policies conditioned on fatigue, expertise and risk tolerance."
img: assets/img/proj-human-factor-cyber-defense.png
importance: 1
category: cybersecurity
related_publications: true
---

**Paper:** [Google Scholar](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=rJhy860AAAAJ&citation_for_view=rJhy860AAAAJ:2osOgNQ5qMEC) · [Publisher](https://doi.org/10.1109/IEEECONF60004.2024.10942949)

Learning defense policies from offline data and expert demonstrations avoids interacting with a live network or simulator during training. Existing imitation and inverse learning methods, however, ignore the human factors that shape how operators make decisions and carry out their workflow.

This project proposes an adversarial inverse reinforcement learning algorithm conditioned on models of three human factors: fatigue, expertise and risk tolerance. Each factor is modeled through the operator's reward function. The method therefore learns policies tailored to users with specific characteristics rather than one average operator. The learned models predict an operator's next actions, which is the basis for assistive AI in network defense.

<div class="row justify-content-sm-center">
  <div class="col-sm-9 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/proj-human-factor-cyber-defense-fig1.png" alt="Assistive AI for cyber defense. The AI learns a human operator's defense workflow from observed actions and uses it to predict and support the operator's next actions in a wireless and IoT network." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Assistive AI for cyber defense. The AI learns a human operator's defense workflow from observed actions and uses it to predict and support the operator's next actions in a wireless and IoT network.
  <br><span class="figure-credit">© 2024 IEEE. Reprinted from A. Ravari et al., <i>Asilomar Conference on Signals, Systems, and Computers</i>, 2024.</span>
</div>

In the CAGE Challenge 2 environment, users with different human factors behave in markedly different ways. The factor-conditioned method improves significantly over baselines that ignore those factors.

<div class="row justify-content-sm-center">
  <div class="col-sm-12 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/proj-human-factor-cyber-defense-fig2.png" alt="Average accumulated reward over time for users with different fatigue levels (left) and expertise levels (middle), and average accumulated security reward for different risk levels (right)." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Average accumulated reward over time for users with different fatigue levels (left) and expertise levels (middle), and average accumulated security reward for different risk levels (right).
  <br><span class="figure-credit">© 2024 IEEE. Reprinted from A. Ravari et al., <i>Asilomar Conference on Signals, Systems, and Computers</i>, 2024.</span>
</div>

Published in *Asilomar Conference on Signals, Systems, and Computers, 2024* {% cite ravari2024adversarial %}.
