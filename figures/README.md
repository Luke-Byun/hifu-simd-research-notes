# UFUV Figures

The two example panels use frame 25 from two different videos in the authors' [public UFUV test set](https://huggingface.co/datasets/huihuixu/uterine_fibroid_ultrasound_video_segmentation). The dataset page lists an MIT license; the accompanying paper is [LGRNet (MICCAI 2024)](https://papers.miccai.org/miccai-2024/460-Paper0813.html).

Left to right: ultrasound frame, ground truth in green, and prediction in red. The predictions come from the **12-epoch LGRNet Res2Net50 adaptation**, not the PVTv2 run. The examples were chosen to show different boundary behavior; they are not a random sample. The exported filenames omit the original video IDs, and the PNGs contain no metadata.

`ufuv_public_per_video_dice.png` plots Dice for all 17 public test videos from the Res2Net50 adaptation and the separate PVTv2 public-config run. Video IDs are omitted. The two runs used different settings, so the plot describes their spread rather than a controlled backbone comparison.
