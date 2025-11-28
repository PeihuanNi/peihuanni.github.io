+++
date = '2025-11-28T14:11:33+08:00'
draft = false
title = "[DATE'26]APEX: Integer-only Non-linear Function Approximation for Efficient Cross-Modal Inference"
+++

<!-- **Peihuan Ni**, Zitao Mo, Tielong Liu, Hongli Wen, Zeyu Zhu, Minnan Pei, Junwen Si, Weifan Guan, Peisong Wang, Qinghao Hu, Gang Li and Jian Cheng, "APEX: Integer-only Non-linear Function Approximation for Efficient Cross-Modal Inference", in Design, Automation and Test in Europe Conference (DATE), IEEE, 2026 -->

<!--more-->

The non-linear functions introduced to modern Trans-formers are crucial to enhance the model performance. However, their high numerical precision requirements pose significant challenges for efficient inference, especially on resource-constrained hardware. Existing approximation methods still suffer from considerable computational overhead and limited generalization due to their sensitivity to the statistical distribution of activations. This limitation becomes particularly pronounced when a non-linear approximation designed for one modality is directly applied to another, as it fails to accommodate their divergent activation behaviors. To overcome these issues, we propose APEX, an efficient integer-only non-linear approximation method designed for robustness and general applicability. APEX integrates the computational graphs of non-linear functions into a unified dataflow, and performs bit-level optimization through static bit allocation and adaptive bit-width pruning (ABP), a technique that dynamically adjusts operand precision on-chip to lower computation costs and prevent underflow. We further co-design a unified and adaptive hardware architecture that supports the above two operand bit-width reduction schemes, significantly reducing hardware cost while maintaining accuracy. Extensive experiments across diverse language and vision models demonstrate that APEX achieves state-of-the-art performance. It improves accuracy by up to 0.7% on language models and 1.3% on vision models compared to prior work, with only a slight accuracy loss in multi- modal models. Furthermore, our proposed architecture achieves improvements of 1.73-8.71× in area efficiency and 1.21-10.83× in power efficiency, respectively.

<div style="display: flex; justify-content: center; align-items: center; gap: 100px; margin: 40px 0;">
    <img src="/images/roberta_large_act_distribution.png" alt="roberta" style="height:300px; width: auto;">
    <img src="/images/deit_tiny_patch16_224_act_distribution.png" alt="deit" style="height:300px; width: auto;">
</div>

<div style="display: flex; justify-content: center; margin: 40px 0;">
    <img src="/images/date26-architecture.pdf.png" alt="architecture" style="max-width: 80%; height: auto;">
</div>
