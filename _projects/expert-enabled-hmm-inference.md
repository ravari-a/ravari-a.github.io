---
layout: page
title: "Expert-Enabled Inference of Hidden Markov Models"
description: "Inferring hidden Markov models from the decisions experts make, not only from how the system behaves."
img: assets/img/proj-expert-enabled-hmm-inference.png
importance: 1
category: systems biology
related_publications: true
---

**Paper:** [Google Scholar](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=rJhy860AAAAJ&citation_for_view=rJhy860AAAAJ:d1gkVwhDpl0C) · [Publisher](https://doi.org/10.1109/TAI.2024.3358261) · [Free full text (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC11324238/)

Many datasets record more than how a system evolves. They also record what an expert did to it: a biologist's interventions, a defender's responses, a driver's maneuvers. Standard methods for inferring hidden Markov models (HMMs) use only the temporal changes in the data and ignore the knowledge behind those decisions.

This project models the expert as an imperfect reinforcement learning agent whose actions reflect their perception of the system. Combining dynamic programming with optimal recursive Bayesian estimation gives an exact, recursive inference method that uses both the expert's actions and the system's temporal behavior. The method works with standard criteria such as maximum likelihood and maximum a posteriori. When the expert's confidence is unknown, it can be inferred jointly with the system model.

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/proj-expert-enabled-hmm-inference-fig1.png" alt="An HMM observed through expert-acquired data. The hidden state X evolves under the expert's actions a and is seen only through the measurements Y." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  An HMM observed through expert-acquired data. The hidden state X evolves under the expert's actions a and is seen only through the measurements Y.
  <br><span class="figure-credit">© 2024 IEEE. Reprinted from A. Ravari, S. F. Ghoreishi and M. Imani, <i>IEEE Transactions on Artificial Intelligence</i>, 2024.</span>
</div>

In experiments on a benchmark problem and on biological networks, accounting for the expert makes the true model easier to distinguish from the alternatives. The advantage is largest when the expert is confident.

<div class="row justify-content-sm-center">
  <div class="col-sm-7 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/proj-expert-enabled-hmm-inference-fig2.png" alt="Benchmark problem: rate of identifying the true model (top) and average error (bottom) as data accumulate, for expert-enabled maximum likelihood (blue) and standard maximum likelihood (red)." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Benchmark problem: rate of identifying the true model (top) and average error (bottom) as data accumulate, for expert-enabled maximum likelihood (blue) and standard maximum likelihood (red).
  <br><span class="figure-credit">© 2024 IEEE. Reprinted from A. Ravari, S. F. Ghoreishi and M. Imani, <i>IEEE Transactions on Artificial Intelligence</i>, 2024.</span>
</div>

Published in *IEEE Transactions on Artificial Intelligence, 2024* {% cite ravari2024optimal %}.
