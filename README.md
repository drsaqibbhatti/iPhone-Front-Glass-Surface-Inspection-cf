# AOI System for Apple iPhone Front Glass Surface Inspection

## ⚠️ Confidential / Proprietary
This repository contains a public summary only. The full implementation and training data are confidential and are maintained in a private repository.

**Hybrid AOI pipeline** for iPhone front-glass surface inspection, built for **real-time production deployment**:
- **Object Detection:** (fast multi-class defect localization)
- **Segmentation:** (pixel-level localization for small defects)
- **Acceleration:** TensorRT optimization for production speed

Project page (demo + overview):

https://drsaqibbhatti.com/projects/iphone-front-glass-aoi.html

This project targets **14 defect classes** (scratches, particles, contamination, pinholes, cracks, chips, bubbles, etc.) and is designed for challenging **reflective glass surfaces** in high-throughput manufacturing environments.

> ⚠️ **Data note:** Training/evaluation media and some deployment details are omitted due to data confidentiality. 

---

## Key Challenges (What this solves)

- **14 defect categories** requiring both detection and precise localization
- **Real-time inference** needed for high-throughput production
- **Tiny defects** (pinholes/particles) require **pixel-level accuracy**
- **Reflective glass** creates difficult imaging conditions (glare/low-contrast) 

---

## Solution Overview

Hybrid inspection pipeline:
1. **YOLOv11 detection** provides fast candidate defect locations (bounding boxes)
2. **SegNExt segmentation** refines defect regions at pixel level (small/subtle defects)
3. **TensorRT** accelerates inference for production-grade throughput

---

## Tech Stack

- **Languages:** Python & C#  
- **Libraries/Runtime:** PyTorch, OpenCV, TensorRT (production)
