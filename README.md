# AEM-KD
This repository contains the official PyTorch implementation of **AEM-KD**: Adversarial Entropy Minimization for Cross-Modality Knowledge Distillation in SAR Building Segmentation.

The full source code and pre-trained models will be released upon the formal acceptance of the corresponding paper.

---

## Abstract

Building segmentation in synthetic aperture radar (SAR) imagery is critical for numerous remote sensing applications. Nevertheless, the inherent limitations of SAR imagery, such as speckle noise, complex scattering effects, and geometric distortions, pose significant challenges to accurate segmentation. Existing research introduces auxiliary information or handcrafted priors to improve segmentation performance, but often suffers from increased model complexity and poor generalization. Recently, knowledge distillation has emerged as a promising alternative, as the distillation of optical image semantics provides transferable spatial structural knowledge to enhance SAR segmentation, particularly in complex imaging environments. Nevertheless, conventional distillation methods rely on pixel-wise constraints, failing to accommodate the significant heterogeneity between SAR and optical imagery arising from their distinct imaging mechanisms. To overcome these challenges, we propose Adversarial Entropy Minimization Knowledge Distillation (AEM-KD), which distills logits-level knowledge via adversarial learning at the prediction layer. By leveraging structural–semantic correlations between heterogeneous modalities, AEM-KD encourages the SAR network to produce confident, low-entropy predictions consistent with those of the optical teacher, while avoiding rigid pixel-wise constraints. To further reduce feature-level discrepancy, a channel-wise knowledge distillation (CW-KD) module is introduced to align intermediate feature distributions along the channel dimension. With the assistance of CW-KD, AEM-KD further aligns high-level feature representations between the SAR and optical networks, thereby alleviating the progressively increasing feature discrepancy across deeper network layers. Experimental results on the Multi-Sensor All Weather Mapping (MSAW) dataset demonstrate that the proposed cross-modality knowledge distillation framework outperforms existing state-of-the-art (SOTA) distillation methods and achieves robust inference using SAR images alone.

---

## Environment Setup

```bash
conda create -n aem_kd python=3.9
conda activate aem_kd
pip install -r requirements.txt
