---
layout: page
title: Westlake CenBRAIN — iBCI Speech Decoding
description: invasive brain-computer interface Chinese speech decoding from sEEG
img: assets/img/3.jpg # TODO: replace with a real teaser (sEEG signal / decoding architecture diagram)
importance: 3
category: research
related_publications: true
---

Internship at the **CenBRAIN Lab, Westlake University** (Jun 2025 – Sep 2025) as an **Algorithm Engineer Intern**, working on **invasive brain-computer interface (iBCI) speech decoding** from clinical sEEG signals.

## sEEG data acquisition & preprocessing
Built the clinical sEEG data pipeline:
- Low-pass filtering, power-line notch, down-sampling
- Channel selection and differential referencing
- Used **MFA**, **pyPinyin**, and **IPA** mapping to generate word-level time boundaries and **initial / tone / final** labels

## Acoustic-inspired hierarchical decoding
Designed a hierarchical architecture for Chinese sentence decoding:
- A **shared 1D-CNN / RNN** temporal backbone encodes `C × T` sEEG segments
- Three parallel decoders for **Initial**, **Tone**, and **Final**
- Sentence-level Chinese output recovered via **Beam Search**, **pinyin-to-char** mapping, and **LLM re-ranking**

<!-- TODO: add a video of the decoding demo or an architecture walkthrough.
{% include video.liquid path="assets/video/cenbrain_demo.mp4" controls="true" %} -->
<div class="row mt-3">
  <div class="col-sm mt-3 mt-md-0">
    <div class="ratio ratio-16x9">
      <iframe src="https://www.youtube-nocookie.com/embed/VIDEO_ID" allow="autoplay; encrypted-media" allowfullscreen></iframe>
    </div>
  </div>
</div>
<div class="caption">
  TODO: replace with a video of the iBCI speech-decoding demo or the model architecture.
</div>
