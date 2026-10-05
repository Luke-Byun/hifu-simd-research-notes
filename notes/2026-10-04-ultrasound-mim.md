# Masked-Image Pretraining for UFUV Segmentation

*2026-10-04 · Five-fold development study*

## Question

Does masked-image modeling (MIM) on unlabeled uterine ultrasound improve downstream fibroid segmentation?

## Setup

I compared the Medical-SAM3 segmentation baseline (C2) with two MIM checkpoints. Version 2 reformatted the ultrasound field of view to look more like UFUV. Downstream training used 336-pixel inputs, 30 epochs, and five video-group folds. The prespecified primary score was **frame-mean Dice at the final epoch**. MIM pretraining used public sources and de-identified GODIUS images; only aggregate results are shown here.

## Results

| Condition | Five-fold mean Dice ± fold SD |
|---|---:|
| C2, seed 2024 | 0.6127 ± 0.039 |
| MIM v1 | 0.6058 ± 0.050 |
| MIM v2 | 0.6066 ± 0.044 |
| C2 with LoRA r8 | 0.6044 ± 0.039 |
| MIM with LoRA r8 | 0.6059 ± 0.053 |

The C2 means for two other seeds were 0.6107 and 0.6116. MIM holdout reconstruction loss fell from 0.727 to 0.627 in v1 and from 0.733 to 0.635 in v2. A frozen-feature probe gave similar AUROC before and after MIM.

## Readout

The pretraining objective was learned, but downstream Dice did not improve in this setup. Reformatting the images and restricting adaptation to LoRA did not change that result. Each MIM condition used one seed, so the small differences between conditions need replication before making a broader claim.

## Next

Test a pretraining task closer to the segmentation target on the same video-group folds.
