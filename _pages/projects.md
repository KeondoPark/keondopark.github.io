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
          'Pretrained in self-supervised manner, on a large-scale dataset (20,942 PSG cases)',
          'Introduced a novel pretraining strategy: Demographic-Guided Contrastive Learning'
        ],
        gallery: [
          {
            image: '{{ base_path }}/images/projects/SleepMaMi/SleepMaMi_MicroEncoder.png',
            alt: 'SleepMaMi Micro-Encoder',
            title: 'SleepMaMi Micro-Encoder',
            text: 'The Micro-Encoder learns the fine-grained features of each modalities and common features across modalities. For this, it consists of Private-Shared encoders. It is pretrained via the combination of Masked AutoEncoder and Constrastive Learning.'
          },
          {
            image: '{{ base_path }}/images/projects/SleepMaMi/SleepMaMi_MacroEncoder.png',
            alt: 'SleepMaMi Macro-Encoder',
            title: 'SleepMaMi Macro-Encoder',
            text: 'The Macro-Encoder captures the dynamic pattenrs of overnight sleep across hour-long horizon. It is based on Mamba architecture to process the long sequence efficiently. Mamba is run in bidirectional manner to learn sleep patterns from the sleep onset and from the sleep termination.'
          },
          {
            image: '{{ base_path }}/images/projects/SleepMaMi/SleepMaMi_DGCL_formula.png',
            alt: 'SleepMaMi DGCL fomula',
            title: 'SleepMaMi DGCL fomula',
            text: 'DGCL is a generalized version of the standard constrastive learning. Instead of "Positive" or "Negative" labels, Weigthed Similarity is used as labels. The Weighted Similarity is calculated from the demographic distance of each subject pair (Age, BMI, Sex).'
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
        summary: 'I took the second place in Samsung AI/CE Challenge',
        image: '{{ base_path }}/images/projects/Samsung2025/Samsung2025_thumbnail.jpg',
        alt: 'Samsung 2025',
        points: [
          'Topic: Multimodal AI to understand daily life photos',
          'Combination of multiple techniques (pruning, targeted pretraining, LoRA finetuning, promt engineeering) led to small but powerful VLM.',
        ],
        gallery: [
            {
            image: '{{ base_path }}/images/projects/Samsung2025/Samsung2025_problem.png',
            alt: 'Samsung2025 Problem',
            title: 'Challenge Problem',
            text: "Participants develop an AI model that selects the correct answer when given multiple-choice questions about various everyday photos stored in a user's smartphone gallery. Input: Photo and Multiple-choice question / Output: Correct answer number"
          },
          {
            image: '{{ base_path }}/images/projects/Samsung2023/barrel-distortion-1400.webp',
            alt: 'Barrel Distortion',
            title: 'Source image adpatation to the target domain',
            text: 'To project the source domain (RectLinear) to the target domain (FishEye), we distorted the source image using Barrel distortion. The resulting images imitate the characteristics of FishEye image. After distortion, we cropped out the invalide parts outside the image area.'
          },
          {
            image: '{{ base_path }}/images/projects/Samsung2023/background-extraction-1400.webp',
            alt: 'Background extraction',
            title: 'Background fusion',
            text: 'FisyEye images include some background parts. To make the source images look more similar to FishEye images, we extracted the background parts from the FishEye images and fused this with barrel-distorted source images.'
          },
          
          {
            image: '{{ base_path }}/images/projects/Samsung2023/ensemble-1400.webp',
            alt: 'Pseudo-labels generation',
            title: 'Pseudo-labels generation for target iamges using ensemble',
            text: 'We used ensemble to produce the pseudo-labels for target-images. This pseudo-labels are used to fine-tune the model with target iamges.'
          },
          {
            image: '{{ base_path }}/images/projects/Samsung2023/result-1400.webp',
            alt: 'Results',
            title: 'Results',
            text: 'Our model outperformed all other competitors and is ranked at **1st place**! (Public score: mIoU 0.67502 , Private score: mIoU 0.67711)'
          }
        ],
        links: [
          { label: 'Slides', href: 'https://dacon.io/en/competitions/official/236500/codeshare/12688?page=1&dtype=recent' }
        ]
      },
      samsung2023: {
        year: '2023',
        title: 'Samsung AI/CE Challenge ',
        summary: 'My team (Keondo/Eunsu) took the first place in Samsung AI/CE Challenge',
        image: '{{ base_path }}/images/projects/Samsung2023/Samsung2023_thumbnail.jpeg',
        alt: 'Samsung 2023',
        points: [
          'Topic: Camera-Invariant Domain Adaptation',
          'We finetuned ViT-Adapter with augmentation trainig data adapted for fish-eye camera.',
          'Our model was ranked as the first on both public and private scores.'
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
            title: 'Source image adpatation to the target domain',
            text: 'To project the source domain (RectLinear) to the target domain (FishEye), we distorted the source image using Barrel distortion. The resulting images imitate the characteristics of FishEye image. After distortion, we cropped out the invalide parts outside the image area.'
          },
          {
            image: '{{ base_path }}/images/projects/Samsung2023/background-extraction-1400.webp',
            alt: 'Background extraction',
            title: 'Background fusion',
            text: 'FisyEye images include some background parts. To make the source images look more similar to FishEye images, we extracted the background parts from the FishEye images and fused this with barrel-distorted source images.'
          },
          
          {
            image: '{{ base_path }}/images/projects/Samsung2023/ensemble-1400.webp',
            alt: 'Pseudo-labels generation',
            title: 'Pseudo-labels generation for target iamges using ensemble',
            text: 'We used ensemble to produce the pseudo-labels for target-images. This pseudo-labels are used to fine-tune the model with target iamges.'
          },
          {
            image: '{{ base_path }}/images/projects/Samsung2023/result-1400.webp',
            alt: 'Results',
            title: 'Results',
            text: 'Our model outperformed all other competitors and is ranked at **1st place**! (Public score: mIoU 0.67502 , Private score: mIoU 0.67711)'
          }
        ],
        links: [
          { label: 'Slides and Codes', href: 'https://dacon.io/en/competitions/official/236132/codeshare/9175?page=1&dtype=recent' }
        ]
      }
    //   distsleep: {
    //     year: '2025',
    //     title: 'DistillSleep',
    //     summary: 'Real-time, on-device, interpretable sleep staging from single-channel EEG.',
    //     image: '{{ base_path }}/images/themes/homepage-light.png',
    //     alt: 'DistillSleep project thumbnail',
    //     points: [
    //       'Built for efficient sleep staging on edge devices.',
    //       'Published in SLEEP and recognized with a best paper award.',
    //       'Balances model efficiency with interpretable predictions.'
    //     ],
    //     gallery: [
    //       {
    //         image: '{{ base_path }}/images/themes/homepage-light.png',
    //         alt: 'DistillSleep lightweight model thumbnail',
    //         title: 'On-device inference',
    //         text: 'The model is shaped for edge deployment, so sleep staging stays fast enough for real-time use.'
    //       },          
    //     ],
    //     links: [
    //       { label: 'Paper', href: 'https://academic.oup.com/sleep/advance-article-abstract/doi/10.1093/sleep/zsaf240/8239690?redirectedFrom=fulltext' }
    //     ]
    //   },
    //   imagenetes: {
    //     year: '2024',
    //     title: 'ImageNet-ES',
    //     summary: 'A dataset for studying environmental and sensor shifts in image recognition.',
    //     image: '{{ base_path }}/images/editing-talk.png',
    //     alt: 'ImageNet-ES project thumbnail',
    //     points: [
    //       'Explores out-of-distribution shifts caused by changes in acquisition conditions.',
    //       'Accepted at CVPR 2024.',
    //       'Useful for studying robustness under realistic domain shifts.'
    //     ],
    //     gallery: [
    //       {
    //         image: '{{ base_path }}/images/editing-talk.png',
    //         alt: 'ImageNet-ES dataset thumbnail',
    //         title: 'Environmental shift study',
    //         text: 'This project focuses on how changes in the environment and camera sensor affect recognition performance.'
    //       },
    //       {
    //         image: '{{ base_path }}/images/image-alignment-1200x4002.jpg',
    //         alt: 'ImageNet-ES data collection thumbnail',
    //         title: 'Data collection and variation',
    //         text: 'A key part of the work is gathering data that intentionally varies the acquisition setup so robustness can be measured more realistically.'
    //       },
    //       {
    //         image: '{{ base_path }}/images/image-alignment-580x300.jpg',
    //         alt: 'ImageNet-ES evaluation thumbnail',
    //         title: 'Evaluation under shift',
    //         text: 'The dataset is intended to expose failure modes that are easy to miss when evaluation only uses a single clean distribution.'
    //       }
    //     ],
    //     links: [
    //       { label: 'Paper', href: 'https://openaccess.thecvf.com/content/CVPR2024/papers/Baek_Unexplored_Faces_of_Robustness_and_Out-of-Distribution_Covariate_Shifts_in_Environment_CVPR_2024_paper.pdf' }
    //     ]
    //   },
    //   pointsplit: {
    //     year: '2023',
    //     title: 'PointSplit',
    //     summary: 'On-device 3D object detection with heterogeneous low-power accelerators.',
    //     image: '{{ base_path }}/images/foo-bar-identity-th.jpg',
    //     alt: 'PointSplit project thumbnail',
    //     points: [
    //       'Targets efficient 3D perception under tight device constraints.',
    //       'Accepted at ISPN 2023.',
    //       'Fits the broader theme of lightweight AI for on-device inference.'
    //     ],
    //     gallery: [
    //       {
    //         image: '{{ base_path }}/images/foo-bar-identity.jpg',
    //         alt: 'PointSplit main project visual',
    //         title: 'Heterogeneous acceleration',
    //         text: 'The main goal is to split work across low-power accelerators so 3D detection can run efficiently on-device.'
    //       },
    //       {
    //         image: '{{ base_path }}/images/foo-bar-identity-th.jpg',
    //         alt: 'PointSplit thumbnail variation',
    //         title: 'Compact deployment',
    //         text: 'This version highlights the compact deployment setting, where the model has to stay small enough for edge hardware.'
    //       },
    //       {
    //         image: '{{ base_path }}/images/image-alignment-300x200.jpg',
    //         alt: 'PointSplit evaluation or results visual',
    //         title: 'Efficiency vs. accuracy',
    //         text: 'The project balances detection quality with compute constraints, which is the central tradeoff in on-device perception.'
    //       }
    //     ],
    //     links: [
    //       { label: 'Paper', href: 'https://arxiv.org/abs/2504.03654' }
    //     ]
    //   },
    //   mask: {
    //     year: '2020',
    //     title: 'Real-time mask detection on Google Edge TPU',
    //     summary: 'A real-time computer vision project for on-device mask detection.',
    //     image: '{{ base_path }}/images/kd_profile.jpg',
    //     alt: 'Real-time mask detection project thumbnail',
    //     points: [
    //       'Focused on practical deployment with Google Coral Edge TPU.',
    //       'Released publicly and covered on press in 2020.',
    //       'Represents the start of my on-device AI work.'
    //     ],
    //     gallery: [
    //       {
    //         image: '{{ base_path }}/images/kd_profile.jpg',
    //         alt: 'Mask detection model visual',
    //         title: 'Edge TPU deployment',
    //         text: 'The project is built around a deployment target rather than a benchmark-only setup, so the hardware constraint is part of the design.'
    //       },
    //       {
    //         image: '{{ base_path }}/images/kd_profile2.jpg',
    //         alt: 'Mask detection project photo',
    //         title: 'Real-time detection',
    //         text: 'The system was intended to detect masks in real time, which required keeping the pipeline lean enough for responsive inference.'
    //       },
    //       {
    //         image: '{{ base_path }}/images/bio-photo-2.jpg',
    //         alt: 'Mask detection release or presentation photo',
    //         title: 'Public release',
    //         text: 'The work was released publicly and later covered on press, which made it the first widely visible on-device project in my portfolio.'
    //       }
    //     ],
    //     links: [
    //       { label: 'Paper', href: '{{ base_path }}/files/MaskDetection_EdgeTPU.pdf' }
    //     ]
    //   }
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