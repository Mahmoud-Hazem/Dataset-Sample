# Beyond Damage Assessment: Recyclable Material Detection in Aerial Disaster Imagery Using a Lightweight Patch-Based Framework

*Anonymous ACCV 2026 submission, Paper ID #******

## Problem Definition

Aerial disaster imagery has mostly been studied for emergency response: damage assessment, affected-area mapping, and identifying structures that need assistance. Its potential for post-disaster environmental assessment and waste management has received far less attention. Damaged areas contain large amounts of debris that could be recovered and recycled, yet to the best of our knowledge no publicly available dataset supports identifying and classifying disaster debris by material and recycling potential. This work takes that complementary perspective. It shifts the focus from *where* damage occurred to *what* the debris is made of, with the broader goal of supporting post-disaster waste characterization and environmentally informed recycling and recovery strategies.

## RecyMat: The Dataset

RecyMat is a manually labeled dataset of debris material images cropped from aerial imagery of disaster-affected areas. It is built from the totally and majorly damaged regions of RescueNet, which are tiled into patches and then cropped by hand according to the visible material. It covers four classes: **brick**, **wood**, **tile**, and **other** (cement rubble, plastics, metals, vegetation, and remaining components). This repository provides an **anonymized sample** of RecyMat so reviewers can see its content, structure, and diversity and judge its relevance to the proposed research. The complete dataset will be released publicly after publication.

## RecyNet: The Model

RecyNet is a lightweight patch-based classifier for recyclable material detection, built on an ImageNet-pretrained MobileNetV2 and fine-tuned on RecyMat, owning RescueNet dataset characteristics. It was chosen over four other lightweight CNNs for the best trade-off between accuracy, model size, and training time, and it runs on CPU only. Damaged regions are split into a regular grid of patches, each patch is assigned its dominant material class, and the predictions are rendered as material overlay maps. These maps give per-region patch counts and a rough estimate of the surface-area ratio of each material. The trained model will be made publicly available after publication.
