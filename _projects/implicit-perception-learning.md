---
layout: page
title: "Implicit Human Perception Learning for Rescue Operations"
description: "An agent that learns how its human teammate perceives an unknown environment, without communication."
img: assets/img/proj-implicit-perception-learning.png
importance: 1
category: disaster response
related_publications: true
---

**Paper:** [Google Scholar](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=rJhy860AAAAJ&citation_for_view=rJhy860AAAAJ:9yKSN-GCB0IC) · [Publisher](https://doi.org/10.23919/ACC60939.2024.10644975)

In crisis response, humans and autonomous agents often have only partial knowledge of the environment, such as where victims are or which paths are blocked. Communication can close this gap, but in many disasters there is no channel or no time to answer queries.

This project lets an agent reason implicitly about its human teammate's perception of the environment from limited human data, without direct communication. The human is modeled as a non-optimal reinforcement learning agent in a partially known Markov decision process. A recursive method optimally builds a probabilistic model of the environment from the agent's own experience and the quantified human perception. Any decision policy that relies on an environment model can use it.

<div class="row justify-content-sm-center">
  <div class="col-sm-12 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/proj-implicit-perception-learning-fig1.png" alt="Paths under the MAP policy with (left) and without (middle) human perception, and the agent's probability that an unknown cell is a wall (right). With human data, the agent identifies the wall after four steps." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Paths under the MAP policy with (left) and without (middle) human perception, and the agent's probability that an unknown cell is a wall (right). With human data, the agent identifies the wall after four steps.
  <br><span class="figure-credit">© 2024 AACC. Reprinted from A. Ravari, S. F. Ghoreishi and M. Imani, <i>American Control Conference (ACC)</i>, 2024.</span>
</div>

In a rescue operation with a human and an agent, incorporating human perception helps the agent identify the true environment sooner and earn a higher reward.

<div class="row justify-content-sm-center">
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/proj-implicit-perception-learning-fig2.png" alt="Average accumulated reward (top) and average posterior probability of the true environment (bottom) over time, for MAP policies with and without human perception and a baseline." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Average accumulated reward (top) and average posterior probability of the true environment (bottom) over time, for MAP policies with and without human perception and a baseline.
  <br><span class="figure-credit">© 2024 AACC. Reprinted from A. Ravari, S. F. Ghoreishi and M. Imani, <i>American Control Conference (ACC)</i>, 2024.</span>
</div>

Published in *American Control Conference (ACC), 2024* {% cite ravari2024implicit %}.
