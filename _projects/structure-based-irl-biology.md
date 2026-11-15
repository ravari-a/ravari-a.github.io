---
layout: page
title: "Quantifying Biologists' Knowledge with Structure-Based IRL"
description: "Learning biologists' decision policies with reward functions shaped by the structure of the gene network."
img: assets/img/proj-structure-based-irl-biology.png
importance: 3
category: systems biology
related_publications: true
---

**Paper:** [Google Scholar](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=rJhy860AAAAJ&citation_for_view=rJhy860AAAAJ:u-x6o8ySG0sC) · [Publisher](https://doi.org/10.1109/CAI54212.2023.00126) · [Free full text (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC10552793/)

Gene regulatory networks (GRNs) govern processes such as stress response and DNA repair, as well as mechanisms of complex diseases such as cancer. Biologists take part in most biological analyses, and their decisions are recorded in the data they produce. Quantifying the policies behind those decisions can help us understand these systems. Standard inverse reinforcement learning struggles here because biological data are limited and highly uncertain.

This work uses the network structure of GRNs to define expert reward functions with exponentially fewer parameters than regular reward models. Fewer parameters means less to learn from scarce data.

<div class="row justify-content-sm-center">
  <div class="col-sm-12 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/proj-structure-based-irl-biology-fig1.png" alt="(a) Pathway diagram of the mammalian cell-cycle network. (b) Normalized mean squared error between the inferred and true model. (c) Mismatch between the inferred and true biologist policy. Both (b) and (c) are plotted against the number of reward-function evaluations." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  (a) Pathway diagram of the mammalian cell-cycle network. (b) Normalized mean squared error between the inferred and true model. (c) Mismatch between the inferred and true biologist policy. Both (b) and (c) are plotted against the number of reward-function evaluations.
  <br><span class="figure-credit">© 2023 IEEE. Reprinted from A. Ravari, S. F. Ghoreishi and M. Imani, <i>IEEE Conference on Artificial Intelligence (CAI)</i>, 2023.</span>
</div>

Experiments with the mammalian cell-cycle network and synthetic gene-expression data show superior performance in quantifying biologists' policies.

Published in *IEEE Conference on Artificial Intelligence (CAI), 2023* {% cite ravari2023structure %}.
