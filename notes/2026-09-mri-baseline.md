# MRI Segmentation Baseline

*September 2026 · Public UMD uterine fibroid MRI*

## Question

Is medical-image pretraining a useful starting point for LoRA adaptation to fibroid segmentation? Where does the model struggle by lesion size?

## Setup

The public UMD study used a patient-level split of 213 training, 26 validation, and 28 test cases. I compared SAM3-LoRA with a MedSAM3-initialized LoRA model. The initial runs used rank 16, alpha 32, dropout 0.1, and a physical batch size of 1 with four accumulation steps. Predictions were examined at both image and lesion level.

## What I saw

The MedSAM3-initialized model became the working baseline for follow-up analysis. The smallest lesions were the clearest remaining target: a pixel-level overlap score can look reasonable while individual lesions are missed. I therefore tracked image-level and matched-lesion results alongside the pooled pixel score.

## Next

For each candidate, record pixel micro Dice, mean per-image Dice, and mean matched-instance Dice. Track small-lesion recall on the same validation split before changing the model or sampling rule.
