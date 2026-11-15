---
layout: page
title: "Latent Task Inference in Human–AI Teams"
description: "Identifying which task model explains a human teammate's behavior, from observed trajectories alone."
img: assets/img/proj-latent-task-inference.png
importance: 2
category: disaster response
related_publications: true
---

**Paper:** [Google Scholar](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=rJhy860AAAAJ&citation_for_view=rJhy860AAAAJ:zYLM7Y9cAGgC) · [Publisher](https://doi.org/10.1109/CCTA62090.2026.11684264)

Mixed human–AI teams often work with little explicit communication and with uncertainty about the task itself. To coordinate, the AI has to work out quickly which latent task or environment model best explains what its human teammate is doing.

This project models collaboration as a task-uncertain cooperative Markov decision process. The AI agent keeps a posterior over a finite set of candidate task models, updated by a fully recursive Bayesian rule that combines its own experience with passively observed human state trajectories. The human's actions are not observed; they are integrated out under a bounded-rational, cooperative policy model. The posterior can drive maximum a posteriori decisions or decisions weighted across hypotheses. An analysis identifies when human trajectories are informative and when they add little.

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/proj-latent-task-inference-fig1.png" alt="A cooperative human–AI team shares a reward in a partially known environment. The question is which task or environment model best explains the observed human trajectory." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  A cooperative human–AI team shares a reward in a partially known environment. The question is which task or environment model best explains the observed human trajectory.
  <br><span class="figure-credit">© 2026 IEEE. Reprinted from A. Ravari et al., <i>IEEE Conference on Control Technology and Applications (CCTA)</i>, 2026.</span>
</div>

In grid-world rescue tasks with hidden environmental structure, the agent identifies the correct hypothesis faster and earns a higher cooperative return than with agent-only inference. The gains grow when human decisions are more reliable.

<div class="row justify-content-sm-center">
  <div class="col-sm-9 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/proj-latent-task-inference-fig2.png" alt="Average cumulative cooperative return over 100 runs with the human likelihood term (red), without it (blue), and for an oracle that knows the true model (black)." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Average cumulative cooperative return over 100 runs with the human likelihood term (red), without it (blue), and for an oracle that knows the true model (black).
  <br><span class="figure-credit">© 2026 IEEE. Reprinted from A. Ravari et al., <i>IEEE Conference on Control Technology and Applications (CCTA)</i>, 2026.</span>
</div>

Published in *IEEE Conference on Control Technology and Applications (CCTA), 2026* {% cite ravari2026inference %}.
