````markdown
---
layout: page
title: SATTC
description: Structure-Aware Label-Free Test-Time Calibration for Cross-Subject EEG-to-Image Retrieval
img: assets/img/sattc_teaser.png
importance: 1
category: research
related_publications: false
---

# SATTC

**Structure-Aware Label-Free Test-Time Calibration for Cross-Subject EEG-to-Image Retrieval**

**Qunjie Huang, Weina Zhu**  
**IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), 2026**

{% include figure.liquid
  loading="eager"
  path="assets/img/sattc_teaser.png"
  title="SATTC overview"
  class="img-fluid rounded z-depth-1"
%}

## Overview

Cross-subject EEG-to-image retrieval aims to decode visual-semantic information from the neural signals of previously unseen individuals. In practice, however, subject-specific distribution shifts can substantially distort the geometry of the retrieval space and reduce decoding reliability.

SATTC is a **label-free test-time calibration framework** designed for cross-subject EEG-to-image retrieval. Instead of retraining the neural encoder, SATTC uses the structure of unlabeled test-time representations to recalibrate similarity relationships before retrieval.

## Research question

> How can an EEG visual-decoding system adapt to an unseen subject at test time without requiring target labels or retraining the backbone?

SATTC approaches this problem from the perspective of retrieval-space calibration rather than treating cross-subject generalization solely as an encoder-training problem.

## Approach

SATTC operates as a plug-and-play calibration stage on top of pretrained EEG-to-image retrieval models.

Its central ideas are:

- **Structure-aware calibration:** exploits relationships among unlabeled test-time representations to estimate reliable local structure.
- **Adaptive similarity correction:** recalibrates cross-modal similarities to reduce distortions caused by subject shift and retrieval hubness.
- **Consistency-aware refinement:** uses reciprocal and neighborhood-level relationships to improve the reliability of retrieved candidates.
- **Encoder-agnostic deployment:** can be applied without retraining or modifying the underlying EEG encoder.

## Why it matters

Most cross-subject neural-decoding methods focus primarily on learning a better invariant representation during training. SATTC shows that deployment-time calibration is another important component of generalizable neural decoding.

This perspective suggests that reliable brain–computer interface systems may require both:

1. strong pretrained neural representations, and
2. lightweight adaptation mechanisms for previously unseen users.

## Key takeaways

- Cross-subject retrieval errors arise not only from representation shift, but also from distorted retrieval geometry.
- Unlabeled test-time structure can provide useful signals for calibration.
- Test-time calibration can be separated from encoder design and applied as a plug-and-play component.
- Deployment reliability should be treated as a first-class problem in neural decoding.

## Resources

<!--
Uncomment and replace the URLs below when the corresponding resources are publicly available.

[Paper](PAPER_URL) ·
[Code](CODE_URL) ·
[Poster](POSTER_URL) ·
[Video](VIDEO_URL)
-->

## Citation

```bibtex
@inproceedings{huang2026sattc,
  title     = {SATTC: Structure-Aware Label-Free Test-Time Calibration for Cross-Subject EEG-to-Image Retrieval},
  author    = {Huang, Qunjie and Zhu, Weina},
  booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  year      = {2026}
}
````

```
```
