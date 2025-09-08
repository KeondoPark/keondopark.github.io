---
title: "DistillSleep: Real-Time, On-Device, Interpretable Sleep Staging from Single-Channel EEG"
collection: publications
category: manuscripts
permalink: /publication/2025-distillsleep
excerpt: 'This paper is about automatic sleep staging AI model. We developed a lightweight AI model using knowledge distillation, while providing verifiability.'
date: 2025-08-22
venue: 'SLEEP'
# slidesurl: 'http://academicpages.github.io/files/slides1.pdf'
paperurl: 'http://keondopark.github.io/files/DistillSleep_submitted_sleep.pdf'
bibtexurl: 'http://keondopark.github.io/files/distillsleep.bibtex'
citation: 'Park, K., Hong, J., Lee, W., Shin, H.W. and Kim, H.S., 2025. DistillSleep: Real-Time, On-Device, Interpretable Sleep Staging from Single-Channel EEG. SLEEPJ, p.zsaf240.'
---
Polysomnography is the gold standard for sleep staging, but its high cost, laboratory equipment, and lengthy manual scoring limit patient access. DistillSleep replaces the typical 12-20-sensor setup with a single-channel EEG and performs inference in <10 ms per epoch on a Raspberry Pi, Jetson orin nano, or Coral dev board. Trained and tested on >10,000 overnight recordings from six independent cohorts, it matches expert accuracy (Macro-F1 up to 80%) and supplies clinicians with frequency-band saliency, inter-epoch context, and well-calibrated confidence scores. By combining interpretability, millisecond-level latency, and an open-source code release, DistillSleep supports point-of-care diagnostics, same-night CPAP titration, and large-scale home monitoring, substantially broadening the reach of sleep medicine.
 

