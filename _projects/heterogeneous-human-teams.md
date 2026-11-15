---
layout: page
title: "Hybrid Models of Heterogeneous Human Teams"
description: "Modeling teams whose members differ in awareness and communication, from centralized to decentralized."
img: assets/img/proj-heterogeneous-human-teams.png
importance: 3
category: disaster response
related_publications: true
---

**Paper:** [Google Scholar](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=rJhy860AAAAJ&citation_for_view=rJhy860AAAAJ:qjMakFHDy7sC) · [PMLR](https://proceedings.mlr.press/v283/ravari25a.html) · [PDF](https://raw.githubusercontent.com/mlresearch/v283/main/assets/ravari25a/ravari25a.pdf)

AI systems that support human teams, for example in disaster response, need to anticipate what each member will do. Most behavioral models describe individuals, and multi-agent models usually assume homogeneous agents that are either fully centralized or fully decentralized. Real teams are heterogeneous: members differ in skills, knowledge and awareness, and each shares information with only some teammates.

This project models team behavior as a sub-optimal, hybrid form of multi-agent reinforcement learning, with centralized training and hybrid centralized/decentralized execution. Two parameters describe each member: an awareness range, within which they observe teammates, and a communication range, within which they exchange information. Inverse learning recovers these parameters from observed team behavior. The model therefore covers the whole spectrum from fully centralized to fully decentralized teams.

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/proj-heterogeneous-human-teams-fig1.png" alt="A team member's awareness range (teammates they can observe) and communication range (teammates they can exchange information with)." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  A team member's awareness range (teammates they can observe) and communication range (teammates they can exchange information with).
  <br><span class="figure-credit">© 2025 the authors. From A. Ravari et al., <i>Learning for Dynamics and Control Conference (L4DC)</i>, PMLR 283, 2025.</span>
</div>

In experiments with four agents and five goals, the inferred awareness and communication parameters approach their true values as data accumulate. The hybrid model predicts team actions more accurately than fully centralized and fully decentralized models.

<div class="row justify-content-sm-center">
  <div class="col-sm-7 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/proj-heterogeneous-human-teams-fig2.png" alt="Average accuracy in predicting the team's actions as behavioral data grow, for the hybrid model (blue), a fully centralized model (red) and a fully decentralized model (green)." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Average accuracy in predicting the team's actions as behavioral data grow, for the hybrid model (blue), a fully centralized model (red) and a fully decentralized model (green).
  <br><span class="figure-credit">© 2025 the authors. From A. Ravari et al., <i>Learning for Dynamics and Control Conference (L4DC)</i>, PMLR 283, 2025.</span>
</div>

Published in *Learning for Dynamics and Control Conference (L4DC), 2025* {% cite ravari2025hybrid %}.
