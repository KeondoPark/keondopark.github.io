---
title: "Federated semi-supervised learning with prototypical networks"
collection: publications
category: preprints
permalink: /publication/2022-protofssl
excerpt: 'This paper proposes a federated semi-supervesed learning method, by sharing knowledge between cleints and server through prototypes.'
date: 2022-05-27
venue: 'Arxiv'
paperurl: 'http://keondopark.github.io/files/ProtoFSSL_arxiv_v2.pdf'
citation: 'Kim, W., Park, K., Sohn, K., Shu, R. and Kim, H.S., 2022. Federated semi-supervised learning with prototypical networks. arXiv preprint arXiv:2205.13921.'
---

With the increasing computing power of edge devices, Federated Learning (FL) emerges to enable model training without privacy concerns. The majority of existing studies assume the data are fully labeled on the client side. In practice, however, the amount of labeled data is often limited. Recently, federated semi-supervised learning (FSSL) is explored as a way to effectively utilize unlabeled data during training. In this work, we propose ProtoFSSL, a novel FSSL approach based on prototypical networks. In ProtoFSSL, clients share knowledge with each other via lightweight prototypes, which prevents the local models from diverging. For computing loss on unlabeled data, each client creates accurate pseudo-labels based on shared prototypes. Jointly with labeled data, the pseudo-labels provide training signals for local prototypes. Compared to a FSSL approach based on weight sharing, the prototype-based inter-client knowledge sharing significantly reduces both communication and computation costs, enabling more frequent knowledge sharing between more clients for better accuracy. In multiple datasets, ProtoFSSL results in higher accuracy compared to the recent FSSL methods with and without knowledge sharing, such as FixMatch, FedRGD, and FedMatch. On SVHN dataset, ProtoFSSL performs comparably to fully supervised FL methods.
