# AEM-KD

This repository contains the official PyTorch implementation of **AEM-KD**:

**Adversarial Entropy Minimization for Cross-Modality Knowledge Distillation in SAR Building Segmentation**,  
published in *IEEE Journal of Selected Topics in Applied Earth Observation and Remote Sensing*.

---

## Overview

Synthetic Aperture Radar (SAR) building segmentation is challenged by speckle noise, complex scattering mechanisms, and geometric distortions.  
AEM-KD addresses these issues by introducing an adversarial entropy minimization based cross-modality knowledge distillation framework, which transfers structural and semantic knowledge from optical imagery to SAR representations during training, without requiring optical data at inference time.

---

## Environment Setup

```bash
conda create -n aem_kd python=3.9
conda activate aem_kd
pip install -r requirements.txt
