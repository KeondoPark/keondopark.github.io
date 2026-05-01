---
title: "SleepMaMi: A Universal Sleep Foundation Model for Integrating Macro- and Micro-structures"
collection: publications
category: conferences
permalink: /publication/2026-SleepMaMi
excerpt: 'SleepMaMi is a novel Sleep Foundation Model integrating sleep micro-structure (second-scale signal morphologies) to macro-structure (hour-long sleep patterns observed over the full night).'
date: 2026-04-30
venue: 'ICML'
paperurl: 'https://arxiv.org/abs/2602.07628'
citation: 'Park, K., Na, Y., Choi, Y., Ryu, H., Shin, H.w., Kim. H.S., 2026., SleepMaMi: A Universal Sleep Foundation Model for Integrating Macro- and Micro-structures., Forty-third International Conference on Machine Learning.'
---


While the shift toward unified foundation models has revolutionized many deep learning domains, sleep medicine remains largely restricted to task-specific models that focus on localized micro-structure features. These approaches often neglect the rich, multi-modal context of Polysomnography (PSG) and fail to capture the global macro-structure of a full night's sleep. To address this, we introduce SleepMaMi , a Sleep Foundation Model engineered to master both hour-long sleep architectures and fine-grained signal morphologies. Our framework utilizes a hierarchical dual-encoder design: a Macro-Encoder to model full-night temporal dependencies and a Micro-Encoder to capture short-term characteristics from biosignals. Macro-Encoder is trained via Demographic-Guided Contrastive Learning, which aligns overnight sleep patterns with objective subject metadata, such as age, sex and BMI to refine global representations. Micro-Encoder is optimized via a hybrid Masked Autoencoder (MAE) and multi-modal contrastive objective. Pre-trained on a massive corpus of >20,000 PSG recordings (158K hours),SleepMaMi outperforms existing foundation models across a diverse suite of downstream tasks, demonstrating superior generalizability and label-efficient adaptation for clinical sleep analysis.