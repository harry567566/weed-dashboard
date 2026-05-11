# Autonomous Weed Detection — Live Dashboard

Live snapshot of the autonomous data-discovery pipeline at
[greatroboticslab/agentAI](https://github.com/greatroboticslab/agentAI).
Auto-regenerated from cluster on each Job-D harvest cycle.

**Live URL**: https://harry567566.github.io/weed-dashboard/

## What you'll see

- **Home** — totals, scale, latest canonical mAP (pycocotools)
- **Datasets** — every dataset Brain has discovered, with 6 sample images each,
  bounding boxes drawn (green = human label, orange = AI label).
  NEVER_TRAIN slugs (cwd12 holdout) outlined in red.
- **Categories** — annotation type, crop/topic, source breakdowns
- **Progress** — canonical mAP history + Job-D run log

## Truth anchors

- **cwd12 test+valid** (1,977 hand-labeled imgs by Yang Lu et al.) is the
  NEVER_TRAIN evaluation set — stem-filtered to guarantee 0 leak.
- **pycocotools** is the canonical mAP eval, not ultralytics
  (which overestimates by ~0.15 on this task).
- Current baseline: cwd12 mAP50-95 = **0.7446** pycocotools (yolo26x
  trained on cwd12 train alone). Goal: **≥ 0.90**.
