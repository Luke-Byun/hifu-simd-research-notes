# Data and Figure Provenance

The two qualitative panels in this repository use frames from the authors' [public UFUV test release](https://huggingface.co/datasets/huihuixu/uterine_fibroid_ultrasound_video_segmentation). The dataset page lists an MIT license. Each panel shows the frame, ground-truth mask overlay, and model prediction. We checked the displayed pixels for names and dates and confirmed that the PNG files contain no metadata. The third figure plots per-video Dice from the same public test set. [Figure details](figures/README.md).

No GODIUS or other private clinical image, mask, or overlay is used in these figures. The [MIM note](notes/2026-10-04-ultrasound-mim.md) reports aggregate scores from a run that did use de-identified GODIUS images for pretraining. This repository does not contain those images, patient-level predictions, DICOM/NIfTI files, raw manifests, checkpoints, internal paths, logs, or credentials.

The `.gitignore` file admits only the reviewed notes and three public-UFUV figures. Check the source, visible text, metadata, and redistribution terms before adding another image.
