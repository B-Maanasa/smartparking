# Phase 3 BEV Summary

- Total image pairs evaluated: 46
- Average usable area percent: 86.9286
- Average black area percent: 13.0714
- Average sharpness score: 229.9025
- Average edge preservation ratio: 0.438802
- Average SSIM score: 0.239907
- Average BEV usability score: 67.0903

## Status Counts
- usable_for_v1: 28
- needs_review: 18
- poor: 0

## Best BEV Image
- image_id: 36
- score: 84.9897
- status: usable_for_v1

## Worst BEV Image
- image_id: 17
- score: 51.3864
- status: needs_review

## Final Conclusion
BEV outputs are usable for controlled one-parking-lot V1 evaluation.

## Note
These metrics evaluate BEV image quality and structural usability. They do not prove real-world metric accuracy because physical ground-truth calibration points were not available.