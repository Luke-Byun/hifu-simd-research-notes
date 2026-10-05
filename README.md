# Uterine Fibroid Segmentation: Research Notes

Working notes from MRI and ultrasound segmentation experiments. Last updated **2026-10-05**. Each entry records the setup, the result, and the question it left open.

| Date | Note | What it covers |
|---|---|---|
| Sep 2026 | [MRI baseline](notes/2026-09-mri-baseline.md) | SAM3/MedSAM3 LoRA setup and lesion-size analysis |
| Sep 2026 | [Cross-plane feasibility](notes/2026-09-cross-plane-feasibility.md) | Resolution limits of the public UMD MRI volumes |
| Oct 2, 2026 | [UFUV baselines](notes/2026-10-02-ufuv-baselines.md) | Public ultrasound benchmark scores and example predictions |
| Oct 4, 2026 | [Ultrasound MIM](notes/2026-10-04-ultrasound-mim.md) | Five-fold downstream results after masked-image pretraining |

The MRI and ultrasound numbers use different datasets and averaging rules. The UFUV figures come only from the [public UFUV release](https://huggingface.co/datasets/huihuixu/uterine_fibroid_ultrasound_video_segmentation). The MIM note includes aggregate results from pretraining that used de-identified GODIUS images; no GODIUS image, mask, or overlay is published here. [Data and figure provenance](PRIVACY.md).
