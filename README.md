# Drone-based 3D Reconstruction of Plants in Field Conditions using Neural Radiance Fields

This repository accompanies the paper:

**Drone-based 3D Reconstruction of Plants in Field Conditions using Neural Radiance Fields**  
Accepted at the *First International Workshop on AI in Agriculture (AgriAI)*,  
co-located with **AAAI 2026**.

Project website:  
https://idealab-isu.github.io/Drone-based-3D-Reconstruction-of-Plants-AAAI26/

---

## Overview

Accurate 3D reconstruction of plants in outdoor agricultural environments is challenging due to occlusion, illumination variation, wind-induced motion, and complex canopy geometry. This work investigates the effectiveness of **Neural Radiance Fields (NeRFs)** for reconstructing field-grown plants using imagery captured from multiple sensing platforms.

We compare three data collection modalities:

- **Drone-based imagery** (DJI Inspire 2 + Zenmuse X5S)
- **Handheld imagery** (iPhone 16 Pro)
- **Ground-based 360° imagery** (TerraSentia robot + Insta360 X4)

The resulting NeRF reconstructions are evaluated using a consistent image-based comparison pipeline to assess reconstruction fidelity under real-world field conditions.

---

## Key Contributions

- Systematic comparison of drone, handheld, and 360° imagery for outdoor plant NeRF reconstruction  
- Demonstration that **drone-based imagery yields the highest geometric fidelity** for field-scale plant reconstruction  
- Quantitative evaluation using **PSNR, SSIM, and LPIPS** computed from camera-aligned real and rendered views  
- Public release of **resulting 3D reconstructions** to support transparency and qualitative inspection

---

## 3D Reconstruction Outputs

The **resulting 3D point clouds generated from NeRF reconstructions** are publicly available on Hugging Face:

🔗 **Point Cloud Outputs**  
https://huggingface.co/datasets/ShambhaviJoshi/Drone_based_3D_Reconstruction_of_Plants_AAAI26

These files represent:
- Final reconstructed point clouds derived from NeRF models
- Outputs corresponding to different sensing modalities and crop plots


---

## Method Summary

1. Image sequences are captured using each sensing modality
2. Camera poses are estimated using **COLMAP**
3. NeRF models are trained using the estimated camera parameters
4. Final reconstructions are exported as 3D point clouds
5. Reconstruction quality is assessed using image-based metrics

Full methodological details are provided in the paper.

---

<!--
## Citation

```bibtex
@inproceedings{joshi2026drone,
  title     = {Drone-based 3D Reconstruction of Plants in Field Conditions using Neural Radiance Fields},
  author    = {Joshi, Shambhavi and Rairdin, Ashlyn and Tranel, Elizabeth and Ganapathysubramanian, Baskar},
  booktitle = {Proceedings of the First International Workshop on AI in Agriculture (AgriAI), AAAI},
  year      = {2026}
}
