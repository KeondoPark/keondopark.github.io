---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

<p class="projects-intro">A few previous projects and research efforts. Click a thumbnail to open a full-page detail view.</p>

<style>
  .projects-shell {
    margin-top: 1.5rem;
  }

  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1.25rem;
  }

  .project-card,
  .project-detail {
    border: 1px solid rgba(15, 23, 42, 0.10);
    border-radius: 20px;
    background: linear-gradient(180deg, rgba(255, 255, 255, 0.98), rgba(248, 250, 252, 0.96));
    box-shadow: 0 12px 30px rgba(15, 23, 42, 0.08);
    overflow: hidden;
  }

  .project-card:hover {
    transform: translateY(-2px);
    border-color: rgba(15, 23, 42, 0.16);
    box-shadow: 0 18px 40px rgba(15, 23, 42, 0.12);
  }

  .project-card {
    transition: transform 180ms ease, box-shadow 180ms ease, border-color 180ms ease;
    padding: 0;
    text-align: left;
    cursor: pointer;
    appearance: none;
    width: 100%;
    color: inherit;
  }

  .project-card:focus-visible,
  .project-detail__back:focus-visible {
    outline: 3px solid rgba(15, 23, 42, 0.32);
    outline-offset: 3px;
  }

  .project-card__inner {
    display: grid;
    gap: 0.9rem;
    padding: 1rem;
  }

  .project-card__media {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 180px;
    overflow: hidden;
    border-radius: 16px;
    background: #fff;
  }

  .project-card__media img {
    width: auto;
    height: auto;
    max-width: 100%;
    max-height: 100%;
    object-fit: contain;
    display: block;
    background: #fff;
  }

  .project-card__badge {
    position: absolute;
    top: 12px;
    left: 12px;
    padding: 0.35rem 0.6rem;
    border-radius: 999px;
    background: rgba(15, 23, 42, 0.82);
    color: #fff;
    font-size: 0.75rem;
    letter-spacing: 0.04em;
    text-transform: uppercase;
  }

  .project-card__content {
    display: grid;
    gap: 0.35rem;
  }

  .project-card__title {
    margin: 0;
    font-size: 1.1rem;
    line-height: 1.25;
  }

  .project-card__meta {
    margin: 0;
    color: #475569;
    font-size: 0.95rem;
    line-height: 1.5;
  }

  .project-card__hint {
    margin: 0;
    color: #64748b;
    font-size: 0.85rem;
  }

  .project-card__body {
    padding: 0 1rem 1rem;
    color: #334155;
  }

  .project-card__body ul {
    margin: 0.75rem 0 0;
    padding-left: 1.1rem;
  }

  .project-card__body li + li {
    margin-top: 0.45rem;
  }

  .project-card__links {
    margin-top: 0.9rem;
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
  }

  .project-card__links a {
    color: #0f172a;
    text-decoration: underline;
    text-underline-offset: 0.18em;
  }

  .project-detail {
    display: grid;
    gap: 1.25rem;
    padding: 1rem;
  }

  .project-detail[hidden] {
    display: none;
  }

  .project-detail__top {
    display: flex;
    justify-content: space-between;
    gap: 1rem;
    align-items: center;
    flex-wrap: wrap;
  }

  .project-detail__back {
    border: 1px solid rgba(15, 23, 42, 0.12);
    border-radius: 999px;
    background: #fff;
    color: #0f172a;
    padding: 0.55rem 0.9rem;
    cursor: pointer;
    font: inherit;
  }

  .project-detail__panel {
    display: grid;
    grid-template-columns: minmax(0, 1.1fr) minmax(320px, 0.9fr);
    gap: 1.25rem;
    align-items: start;
  }

  .project-detail__image {
    border-radius: 18px;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 320px;
    background: #fff;
  }

  .project-detail__image img {
    width: auto;
    height: auto;
    max-width: 100%;
    max-height: 100%;
    min-height: 0;
    object-fit: contain;
    display: block;
    background: #fff;
  }

  .project-detail__content {
    display: grid;
    gap: 0.85rem;
    padding: 0.25rem 0.1rem;
  }

  .project-detail__content h2 {
    margin: 0;
    font-size: clamp(1.7rem, 3vw, 2.4rem);
    line-height: 1.1;
  }

  .project-detail__content p {
    margin: 0;
    color: #334155;
    line-height: 1.65;
  }

  .project-detail__content ul {
    margin: 0.25rem 0 0;
    padding-left: 1.1rem;
    color: #334155;
  }

  .project-detail__content li + li {
    margin-top: 0.45rem;
  }

  .project-detail__links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
    margin-top: 0.35rem;
  }

  .project-detail__links a {
    display: inline-flex;
    align-items: center;
    border-radius: 999px;
    border: 1px solid rgba(15, 23, 42, 0.12);
    padding: 0.5rem 0.85rem;
    text-decoration: none;
    color: #0f172a;
    background: #fff;
  }

  .project-detail__gallery {
    display: grid;
    gap: 1rem;
  }

  .project-detail__photo {
    display: grid;
    grid-template-columns: minmax(240px, 0.95fr) minmax(0, 1.05fr);
    gap: 1rem;
    align-items: center;
    padding: 1rem;
    border-radius: 18px;
    border: 1px solid rgba(15, 23, 42, 0.10);
    background: rgba(255, 255, 255, 0.85);
  }

  .project-detail__photo-media {
    border-radius: 14px;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    background: #fff;
    min-height: 220px;
  }

  .project-detail__photo-media img {
    width: auto;
    height: auto;
    max-width: 100%;
    max-height: 100%;
    min-height: 0;
    object-fit: contain;
    display: block;
    background: #fff;
  }

  .project-detail__photo-copy {
    display: grid;
    gap: 0.5rem;
  }

  .project-detail__photo-copy h3 {
    margin: 0;
    font-size: 1.05rem;
    line-height: 1.3;
  }

  .project-detail__photo-copy p {
    margin: 0;
    color: #334155;
    line-height: 1.65;
  }

  .projects-shell.is-detail .projects-grid {
    display: none;
  }

  @media (max-width: 640px) {
    .projects-grid {
      grid-template-columns: 1fr;
    }

    .project-detail__panel {
      grid-template-columns: 1fr;
    }

    .project-detail__photo {
      grid-template-columns: 1fr;
    }

    .project-detail__image,
    .project-detail__image img {
      min-height: 220px;
    }
  }
</style>

<div class="projects-shell" id="projects-shell">
  <div class="projects-grid" id="projects-grid"></div>

  <section class="project-detail" id="project-detail" hidden aria-live="polite">
    <div class="project-detail__top">
      <button class="project-detail__back" type="button" id="project-detail-back">Back to all projects</button>
      <p class="project-card__hint">Only the selected project is shown here.</p>
    </div>

    <div class="project-detail__panel">
      <div class="project-detail__image">
        <img id="project-detail-image" src="" alt="">
      </div>
      <div class="project-detail__content">
        <span class="project-card__badge" id="project-detail-year"></span>
        <h2 id="project-detail-title"></h2>
        <p id="project-detail-summary"></p>
        <ul id="project-detail-points"></ul>
        <div class="project-detail__links" id="project-detail-links"></div>
      </div>
    </div>

    <div class="project-detail__gallery" id="project-detail-gallery"></div>
  </section>
</div>

<script>
  (function () {
    var projectsShell = document.getElementById('projects-shell');
    var projectsGrid = document.getElementById('projects-grid');
    var projectDetail = document.getElementById('project-detail');
    var detailImage = document.getElementById('project-detail-image');
    var detailYear = document.getElementById('project-detail-year');
    var detailTitle = document.getElementById('project-detail-title');
    var detailSummary = document.getElementById('project-detail-summary');
    var detailPoints = document.getElementById('project-detail-points');
    var detailLinks = document.getElementById('project-detail-links');
    var detailGallery = document.getElementById('project-detail-gallery');
    var backButton = document.getElementById('project-detail-back');

    var projects = {
      sleepmami: {
        year: '2026',
        title: 'SleepMaMi (ICML 2026)',
        summary: 'A universal sleep foundation model that integrates macro- and micro-structures.',
        image: '{{ base_path }}/images/projects/SleepMaMi/SleepMaMi_Thumbnail.png',
        alt: 'SleepMaMi project thumbnail',
        points: [
          'Multimodal foundation model that integrates sleep macro- and micro-structures',          
          'Pretrained in a self-supervised manner on a large-scale dataset (20,942 PSG cases)',
          'Introduced a novel pretraining strategy: Demographic-Guided Contrastive Learning'
        ],
        gallery: [
          {
            image: '{{ base_path }}/images/projects/SleepMaMi/SleepMaMi_MicroEncoder.png',
            alt: 'SleepMaMi Micro-Encoder',
            title: 'SleepMaMi Micro-Encoder',
            text: 'The Micro-Encoder learns the fine-grained features of each modality as well as the common features across modalities. To this end, it consists of private-shared encoders. It is pretrained via a combination of Masked Autoencoding and Contrastive Learning.'
          },
          {
            image: '{{ base_path }}/images/projects/SleepMaMi/SleepMaMi_MacroEncoder.png',
            alt: 'SleepMaMi Macro-Encoder',
            title: 'SleepMaMi Macro-Encoder',
            text: 'The Macro-Encoder captures the dynamic patterns of overnight sleep across an hour-long horizon. It is based on the Mamba architecture to process long sequences efficiently. Mamba is run in a bidirectional manner to learn sleep patterns from both sleep onset and sleep termination.'
          },
          {
            image: '{{ base_path }}/images/projects/SleepMaMi/SleepMaMi_DGCL_formula.png',
            alt: 'SleepMaMi DGCL formula',
            title: 'SleepMaMi DGCL formula',
            text: 'DGCL is a generalized version of standard contrastive learning. Instead of "Positive" or "Negative" labels, a Weighted Similarity is used as the label. The Weighted Similarity is calculated from the demographic distance of each subject pair (Age, BMI, Sex).'
          }
        ],
        links: [
          { label: 'Paper', href: 'https://arxiv.org/abs/2602.07628' },
          { label: 'Code', href: 'https://github.com/keondopark/SleepMaMi' }
        ]
      },
      samsung2025: {
        year: '2025',
        title: 'Samsung Collegiate Programming Challenge ',
        summary: 'I took second place in the Samsung AI/CE Challenge',
        image: '{{ base_path }}/images/projects/Samsung2025/Samsung2025_thumbnail.jpg',
        alt: 'Samsung 2025',
        points: [
          'Topic: Lightweight multimodal AI to understand everyday photos',
          'A combination of multiple techniques (pruning, targeted finetuning, LoRA finetuning, prompt engineering) led to a small but powerful VLM.',
        ],
        gallery: [
            {
            image: '{{ base_path }}/images/projects/Samsung2025/Samsung2025_problem.png',
            alt: 'Samsung2025 Problem',
            title: 'Challenge Problem',
            text: "Participants develop a lightweight AI model that selects the correct answer to multiple-choice questions about various everyday photos stored in a user's smartphone gallery. The number of parameters should not exceed 3 billion."
          },
          {
            image: '{{ base_path }}/images/projects/Samsung2025/Baseline_MobileVLM.png',
            alt: 'MobileVLM',
            title: 'Baseline - MobileVLM',
            text: 'A lightweight pretrained Vision-Language Model is selected as the base model for finetuning: MobileVLM (EMNLP 2024) is a lightweight VLM based on a combination of CLIP and MobileLLaMA. Depthwise convolution is used for computationally efficient vision-language projection.'
          },
          {
            image: '{{ base_path }}/images/projects/Samsung2025/Pruning.png',
            alt: 'Pruning',
            title: 'Pruning',
            text: 'Pretrained MobileVLM has a slightly greater number of parameters (3.03B) than the model specification (3B) required by the Challenge. To make it eligible, LLM-Pruner (NeurIPS 2023) is utilized to reduce the resulting model to fewer than 3B parameters.'
          },
          
          {
            image: '{{ base_path }}/images/projects/Samsung2025/Finetuning_Datasets.png',
            alt: 'Finetuning datasets',
            title: 'Targeted finetuning',
            text: 'The released MobileVLM checkpoint is pretrained on the LLaVA-1.5 dataset - this dataset is relatively small (665K instruction-tuning examples) and known to be messy. The model is finetuned on a large-scale, high-quality dataset to refine it (instruction-tuning data from LLaVA-Next (760K) and LLaVA-OneVision (3.6M)).'
          },
          {
            image: '{{ base_path }}/images/projects/Samsung2025/lora_finetuning.png',
            alt: 'LoRA',
            title: 'LoRA finetuning and Prompt engineering',
            text: 'The model is finetuned with LoRA using the challenge data. LoRA is used to prevent overfitting to the challenge data, given the small size of the dataset. The prompt is refined to obtain the best results.'
          },
          {
            image: '{{ base_path }}/images/projects/Samsung2025/Results.png',
            alt: 'Results',
            title: 'Results',
            text: 'With everything combined, the final model achieved good accuracy while keeping its size sufficiently small.'
          }
        ],
        links: [
          { label: 'Slides', href: 'https://dacon.io/en/competitions/official/236500/codeshare/12688?page=1&dtype=recent' }
        ]
      },
      eegband: {
        year: '2023',
        title: 'On-device Real-time Sleep Stage Classification with Single Channel EEG on Coral',
        summary: 'Class project for EEG-band based on-device sleep staging system',
        image: '{{ base_path }}/images/projects/EEG_band/EEG_band_thumbnail.png',
        alt: 'EEG_band',
        points: [
          'We developed an AI model that can classify sleep stages from EEG-band inputs',
          'The model is extremely small to be run on Coral board in less than 10ms.',
          'Smart watch results (Apple and Galaxy watch) are obtained and compared'
        ],
        gallery: [
            {
            image: '{{ base_path }}/images/projects/EEG_band/EEG_band_thumbnail.png',
            alt: 'EEG band',
            title: 'EEG band',
            text: 'To be completed'
          },
          
        ],
        links: [
          { label: 'YouTube', href: 'https://youtu.be/gDrmccp6O6g?si=9cqQed00Ht04FIDb' }
        ]
      },
      samsung2023: {
        year: '2023',
        title: 'Samsung AI/CE Challenge ',
        summary: 'My team (Keondo/Eunsu) took first place in the Samsung AI/CE Challenge',
        image: '{{ base_path }}/images/projects/Samsung2023/Samsung2023_thumbnail.jpeg',
        alt: 'Samsung 2023',
        points: [
          'Topic: Camera-Invariant Domain Adaptation',
          'We finetuned ViT-Adapter with augmented training data adapted for the fish-eye camera.',
          'Our model ranked first on both the public and private scores.'
        ],
        gallery: [
            {
            image: '{{ base_path }}/images/projects/Samsung2023/ss_problem-1400.webp',
            alt: 'Samsung2023 Problem',
            title: 'Challenge Problem',
            text: 'Autonomous driving utilizes various sensors to perceive its surroundings and control the vehicle accordingly. For camera sensors, a domain gap occurs between images depending on factors such as mounting position, sensor type, and driving environment. Previous studies have widely applied Unsupervised Domain Adaptation techniques to overcome the degradation in recognition performance caused by differences in image photometry and texture. However, most existing research does not account for the domain gap caused by the optical properties of cameras, particularly geometric distortion. Therefore, this competition proposes the development of an **AI algorithm that utilizes undistorted images (Source Domain) and their labels to perform high-performance semantic segmentation on distorted images (Target Domain).**'
          },
          {
            image: '{{ base_path }}/images/projects/Samsung2023/barrel-distortion-1400.webp',
            alt: 'Barrel Distortion',
            title: 'Source image adaptation to the target domain',
            text: 'To project the source domain (Rectilinear) onto the target domain (FishEye), we distorted the source image using barrel distortion. The resulting images imitate the characteristics of a FishEye image. After distortion, we cropped out the invalid parts outside the image area.'
          },
          {
            image: '{{ base_path }}/images/projects/Samsung2023/background-extraction-1400.webp',
            alt: 'Background extraction',
            title: 'Background fusion',
            text: 'FishEye images include some background regions. To make the source images look more similar to FishEye images, we extracted the background regions from the FishEye images and fused them with the barrel-distorted source images.'
          },
          
          {
            image: '{{ base_path }}/images/projects/Samsung2023/ensemble-1400.webp',
            alt: 'Pseudo-labels generation',
            title: 'Pseudo-label generation for target images using an ensemble',
            text: 'We used an ensemble to produce the pseudo-labels for the target images. These pseudo-labels are used to fine-tune the model on the target images.'
          },
          {
            image: '{{ base_path }}/images/projects/Samsung2023/result-1400.webp',
            alt: 'Results',
            title: 'Results',
            text: 'Our model outperformed all other competitors and ranked in **1st place**! (Public score: mIoU 0.67502, Private score: mIoU 0.67711)'
          }
        ],
        links: [
          { label: 'Slides and Codes', href: 'https://dacon.io/en/competitions/official/236132/codeshare/9175?page=1&dtype=recent' }
        ]
      }
    };

    function clearChildren(node) {
      while (node.firstChild) {
        node.removeChild(node.firstChild);
      }
    }

    function appendFormattedText(node, text) {
      var parts = text.split(/(\*\*[^*]+\*\*)/g);

      parts.forEach(function (part) {
        if (!part) {
          return;
        }

        if (part.startsWith('**') && part.endsWith('**')) {
          var strong = document.createElement('strong');
          strong.textContent = part.slice(2, -2);
          node.appendChild(strong);
          return;
        }

        node.appendChild(document.createTextNode(part));
      });
    }

    function renderProjectCards() {
      clearChildren(projectsGrid);

      Object.keys(projects).forEach(function (projectKey) {
        var project = projects[projectKey];
        var card = document.createElement('button');
        card.className = 'project-card';
        card.type = 'button';
        card.setAttribute('data-project', projectKey);

        var inner = document.createElement('div');
        inner.className = 'project-card__inner';

        var media = document.createElement('div');
        media.className = 'project-card__media';

        var image = document.createElement('img');
        image.src = project.image;
        image.alt = project.alt;

        var badge = document.createElement('span');
        badge.className = 'project-card__badge';
        badge.textContent = project.year;

        var content = document.createElement('div');
        content.className = 'project-card__content';

        var title = document.createElement('h2');
        title.className = 'project-card__title';
        title.textContent = project.title;

        var summary = document.createElement('p');
        summary.className = 'project-card__meta';
        summary.textContent = project.summary;

        var hint = document.createElement('p');
        hint.className = 'project-card__hint';
        hint.textContent = 'Click to open details';

        media.appendChild(image);
        media.appendChild(badge);
        content.appendChild(title);
        content.appendChild(summary);
        content.appendChild(hint);
        inner.appendChild(media);
        inner.appendChild(content);
        card.appendChild(inner);

        card.addEventListener('click', function () {
          showProject(projectKey);
        });

        projectsGrid.appendChild(card);
      });
    }

    function renderGallery(project) {
      clearChildren(detailGallery);

      project.gallery.forEach(function (photo) {
        var item = document.createElement('article');
        item.className = 'project-detail__photo';

        var media = document.createElement('div');
        media.className = 'project-detail__photo-media';

        var image = document.createElement('img');
        image.src = photo.image;
        image.alt = photo.alt;
        media.appendChild(image);

        var copy = document.createElement('div');
        copy.className = 'project-detail__photo-copy';

        var title = document.createElement('h3');
        title.textContent = photo.title;

        var text = document.createElement('p');
        appendFormattedText(text, photo.text);

        copy.appendChild(title);
        copy.appendChild(text);
        item.appendChild(media);
        item.appendChild(copy);
        detailGallery.appendChild(item);
      });
    }

    function showProject(projectKey) {
      var project = projects[projectKey];
      if (!project) {
        return;
      }

      detailImage.src = project.image;
      detailImage.alt = project.alt;
      detailYear.textContent = project.year;
      detailTitle.textContent = project.title;
      detailSummary.textContent = project.summary;

      clearChildren(detailPoints);
      project.points.forEach(function (point) {
        var item = document.createElement('li');
        item.textContent = point;
        detailPoints.appendChild(item);
      });

      clearChildren(detailLinks);
      project.links.forEach(function (link) {
        var anchor = document.createElement('a');
        anchor.href = link.href;
        anchor.target = '_blank';
        anchor.rel = 'noopener';
        anchor.textContent = link.label;
        detailLinks.appendChild(anchor);
      });

      renderGallery(project);

      projectsShell.classList.add('is-detail');
      projectDetail.hidden = false;
      projectDetail.scrollIntoView({ behavior: 'smooth', block: 'start' });
    }

    function hideProject() {
      projectDetail.hidden = true;
      projectsShell.classList.remove('is-detail');
      projectsShell.scrollIntoView({ behavior: 'smooth', block: 'start' });
    }

    renderProjectCards();

    backButton.addEventListener('click', hideProject);
  }());
</script>