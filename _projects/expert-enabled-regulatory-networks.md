---
layout: page
title: "Expert-Enabled Inference of Gene Regulatory Networks"
description: "Using biologists' interventions as evidence when inferring gene regulatory networks from limited data."
img: assets/img/proj-expert-enabled-regulatory-networks.png
importance: 2
category: systems biology
related_publications: true
---

**Paper:** [Google Scholar](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=rJhy860AAAAJ&citation_for_view=rJhy860AAAAJ:u5HHmVD_uO8C) · [Publisher](https://doi.org/10.1109/LCSYS.2022.3229054) · [Free full text (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC9835687/)

Accurate inference of biological systems, such as gene regulatory networks and microbial communities, is key to understanding their mechanisms. Biological data are limited and the networks are complex, so inference from temporal changes alone is often inaccurate. The data, however, frequently include interventions chosen by biologists, for example to treat a disease, and those choices carry knowledge about how the network works.

This work models the regulatory network as a Boolean network with perturbation and develops an optimal expert-enabled maximum a posteriori (MAP) inference method. An offline step runs dynamic programming for each candidate network model. An online step combines those results with a softmax model of an imperfect expert and updates the posterior recursively as data arrive.

<div class="row justify-content-sm-center">
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/proj-expert-enabled-regulatory-networks-fig1.png" alt="The p53-MDM2 gene regulatory network. In healthy conditions it rests with all four genes inactive; in cancerous conditions it does not." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  The p53-MDM2 gene regulatory network. In healthy conditions it rests with all four genes inactive; in cancerous conditions it does not.
  <br><span class="figure-credit">© 2022 IEEE. Reprinted from A. Ravari, S. F. Ghoreishi and M. Imani, <i>IEEE Control Systems Letters</i>, 2023.</span>
</div>

On the p53-MDM2 network with five unknown regulatory interactions, expert-enabled inference concentrates on the true network faster and with lower error than standard MAP inference.

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/proj-expert-enabled-regulatory-networks-fig2.png" alt="Average maximum posterior probability as data accumulate, with five unknown regulatory interactions: expert-enabled MAP inference (blue) and standard MAP inference (red)." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Average maximum posterior probability as data accumulate, with five unknown regulatory interactions: expert-enabled MAP inference (blue) and standard MAP inference (red).
  <br><span class="figure-credit">© 2022 IEEE. Reprinted from A. Ravari, S. F. Ghoreishi and M. Imani, <i>IEEE Control Systems Letters</i>, 2023.</span>
</div>

Published in *IEEE Control Systems Letters, 2023* {% cite ravari2022optimal %}.
