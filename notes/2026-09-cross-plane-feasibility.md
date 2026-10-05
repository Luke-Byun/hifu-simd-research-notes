# Cross-plane MRI: Is Reslicing Enough?

*September 2026 · Public UMD MRI volumes*

## Question

Can sagittal volumes be resliced into useful axial and coronal views, or is the through-plane spacing too large?

## Measurement

I checked in-plane resolution, slice spacing, and slice count in 239 public UMD MRI volumes.

| Quantity | Mean |
|---|---:|
| In-plane resolution | 0.49 mm |
| Through-plane spacing | 5.75 mm |
| Spacing ratio | 12.2× |
| Slices per volume | about 22 |

## Readout

Most of the pixels in an orthogonal reslice would have to be interpolated across a much coarser axis. Reslicing alone is unlikely to reproduce the detail in a directly acquired axial or coronal scan. There are also no target-plane masks in this evaluation set, so cross-plane segmentation accuracy cannot yet be measured.

## Next

Once target-plane labels are available, compare direct inference and geometric reprojection on a patient-level split using the same metrics.
