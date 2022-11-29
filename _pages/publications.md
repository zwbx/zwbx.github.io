---
layout: page
permalink: /publications/
title: Publications
description: 
years: [2022, 2021, 2020, 2019, 2018, 2017, 2016]
nav: true
---

[[Google scholar](https://scholar.google.com/citations?user=hBZ_tKsAAAAJ)] | [[DBLP](https://dblp.org/pid/19/2969-1.html)]

#### Preprints

- An Embarrassingly Simple Baseline for Imbalanced Semi-Supervised Learning. Hao Chen, Yue Fan, Yidong Wang, **Jindong Wang**, Bernt Schiele, Xing Xie, Marios Savvides, Bhiksha Raj. [[arxiv](https://arxiv.org/abs/2211.11086)] 
- GLUE-X: Evaluating Natural Language Understanding Models from an Out-of-distribution Generalization Perspective. Linyi Yang, Shuibai Zhang, Libo Qin, Yafu Li, Yidong Wang, Hanmeng Liu, **Jindong Wang**, Xing Xie, Yue Zhang. [[arxiv](https://arxiv.org/abs/2211.08073)]
- Domain-Specific Risk Minimization for Out-of-Distribution Generalization. YiFan Zhang, **Jindong Wang**, Jian Liang, Zhang Zhang, Baosheng Yu, Liang Wang, Xing Xie, and Dacheng Tao. [[arxiv](https://arxiv.org/pdf/2208.08661.pdf)]
- Out-of-distribution Representation Learning for Time Series Classification. Wang Lu, **Jindong Wang**, Xinwei Sun, Yiqiang Chen, and Xing Xie. [[arxiv](https://arxiv.org/abs/2209.07027)]
- Conv-Adapter: Exploring Parameter Efficient Transfer Learning for ConvNets. Hao Chen, Ran Tao, Han Zhang, Yidong Wang, Wei Ye, Jindong Wang, Guosheng Hu, and Marios Savvides. [[arxiv](https://arxiv.org/abs/2208.07463)]
- Towards Optimization and Model Selection for Domain Generalization: A Mixup-guided Solution. Wang Lu, **Jindong Wang**, Yidong Wang, Kan Ren, Yiqiang Chen, Xing Xie. [[arxiv](https://arxiv.org/abs/2209.00652)]
- Equivariant Disentangled Transformation for Domain Generalization under Combination Shift. Yivan Zhang, **Jindong Wang**, Xing Xie, and Masashi Sugiyama. [[arxiv](https://arxiv.org/abs/2208.02011)]
- Boosting Cross-Domain Speech Recognition with Self-Supervision. Han Zhu, Gaofeng Cheng, **Jindong Wang**, Wenxin Hou, Pengyuan Zhang, and Yonghong Yan. [[arxiv](https://arxiv.org/abs/2206.09783)]
- FreeMatch: Self-adaptive Thresholding for Semi-supervised Learning. Yidong Wang, Hao Chen, Qiang Heng, Wenxin Hou, Marios Savvides, Takahiro Shinozaki, Bhiksha Raj, Zhen Wu, **Jindong Wang**, and Bernt Schiele. [[arxiv](https://arxiv.org/abs/2205.07246)]
- Learning Invariant Representations across Domains and Tasks. **Jindong Wang**, Wenjie Feng, Chang Liu, Chaohui Yu, Mingxuan Du, Renjun Xu, Tao Qin, and Tie-Yan Liu. [[arxiv](https://arxiv.org/abs/2103.05114)]
- Learning to match distributions for domain adaptation. Chaohui Yu, **Jindong Wang**, Chang Liu, Tao Qin, Renjun Xu, Wenjie Feng, Yiqiang Chen, and Tie-Yan Liu. [[arxiv](https://arxiv.org/abs/2007.10791)]

#### Books

<div class="publications">

{% for y in page.years %}
  {% bibliography -f books -q @*[year={{y}}]* %}
{% endfor %}

</div>

#### Papers

<div class="publications">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f pubs -q @*[year={{y}}]* %}
{% endfor %}

</div>
