---
title: "Real-time mask detection on google edge TPU"
collection: publications
category: preprints
permalink: /publication/2020-edgetpu
excerpt: 'This paper introduces a new application for real-time mask detection on-device, utilizing Google Coral EdgeTPU'
date: 2020-10-09
venue: 'Arxiv'
paperurl: 'http://keondopark.github.io/files/MaskDetection_EdgeTPU.pdf'
citation: 'Park, K., Jang, W., Lee, W., Nam, K., Seong, K., Chai, K. and Li, W.S., 2020. Real-time mask detection on google edge TPU. arXiv preprint arXiv:2010.04427.'
---

After the COVID-19 outbreak, it has become important to automatically detect whether people are wearing masks in order to reduce risk of front-line workers. In addition, processing user data locally is a great way to address both privacy and network bandwidth issues. In this paper, we present a light-weighted model for detecting whether people in a particular area wear masks, which can also be deployed on Coral Dev Board, a commercially available development board containing Google Edge TPU. Our approach combines the object detecting network based on MobileNetV2 plus SSD and the quantization scheme for integer-only hardware. As a result, the lighter model in the Edge TPU has a significantly lower latency which is more appropriate for real-time execution while maintaining accuracy comparable to a floating point device.