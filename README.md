# Chaitanya Parate

B.Tech CS (AI & Data Science) · MIT-WPU, Pune · 2027  
Zero-shot morphology transfer across robot bodies using heterogeneous GNNs. Embedded firmware on STM32 at European Hyperloop Week 2025. Merged contributor to [metatensor/metatrain](https://github.com/metatensor/metatrain/pull/1003).  
Seeking ML/AI research internship · [LinkedIn](https://www.linkedin.com/in/chaitanyaparate) · paratechaitanya5@gmail.com

---

## Projects

### [Heterogeneous GNN Morphology Transfer](https://github.com/ChaitanyaParate/hetero-gnn-morphology-transfer) [![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.20187567-blue.svg)](https://doi.org/10.5281/zenodo.20187567)

Zero-shot locomotion policy transfer across robot morphologies using a 31,582-parameter heterogeneous GNN (GATv2Conv + PPO). MLP hard-fails on any unseen morphology due to fixed input dimensionality; the GNN handles arbitrary graph structure at inference time.

- **Zero-shot transfer (12-DOF → 18-DOF):** 106 ± 25 reward, ~47 steps survival — no retraining, no morphology-specific tuning
- **500K-step fine-tuning:** 3.8× reward gain (110 → 416 ± 114), survival 47 → 193 steps
- **85% fewer parameters** than MLP baseline (31,582 vs 210,457); MLP beats it in-distribution only — tradeoff is documented
- **Terrain robustness (zero-shot):** 95% success at 5° slope, 0% at 10° — hard cliff, no graceful degradation
- 200 Hz deployment with yaw-rate PI correction on HAA joints to eliminate circular drift from asymmetric training data
- LLM navigation layer: Qwen 2.5 7B via Ollama, natural language → skill → GNN → joint commands, fully on-device on ROS2 Jazzy + Gazebo

### [ResNet-50 From Scratch](https://github.com/ChaitanyaParate/ResNet50-From-Scratch-Pytorch-Imagenette)

Full PyTorch reimplementation of ResNet-50 trained on Imagenette — 86.63% top-1 accuracy. Exported and deployed live on ESP32-CAM for on-device inference. No pretrained weights used at any stage.

### [SE-Attention Half-UNet — Polyp Segmentation](https://github.com/ChaitanyaParate/SE-Attention-Half-UNet)

Encoder-decoder segmentation model combining SE blocks (channel recalibration) with attention gates on skip connections. Trained on Kvasir-SEG with BCE-Dice loss. Dice: 0.9436. Half-UNet cuts decoder depth vs standard UNet while SE recalibration compensates for lost spatial context.

### [Brain Tumor MRI Classification](https://github.com/ChaitanyaParate/Modified-Half-UNet-for-Medical-Image-Classification)

Modified Half-UNet repurposed for classification (encoder-only path). 98% accuracy on MRI scan classification across tumor types. Demonstrates the same backbone generalizing from segmentation to classification without architectural redesign.

### [DeskAI](https://github.com/ChaitanyaParate/Deskai)

Local-first Linux desktop AI daemon. Persistent systemd service with UNIX socket IPC, X11/OCR context capture, and streaming LLM inference via Ollama with online fallback — switches backends without daemon restart.

- Intent router dispatches to typed executors: summarize, explain_error, search
- Fault-tolerant streaming pipeline with full daemon-client lifecycle decoupling
- Online/offline switching determined at request time, not startup

### [stm32-hyperloop-embedded](https://github.com/ChaitanyaParate/stm32-hyperloop-embedded)

STM32 firmware in C for Team Vegapod's braking and power systems. Key constraint: safety-critical braking had to remain responsive under CAN bus saturation from concurrent BMS telemetry. Solved with FreeRTOS task priorities and FDCAN3 interrupt isolation. Represented MIT-WPU at European Hyperloop Week 2025 (Netherlands).

Custom Bluetooth bootloader flashes `.bin` over USART2 via HC-05 into application flash at `0x08008000`. Also covers 3-phase inverter PWM generation and inverter health monitoring.

---

## Open Source

**[metatensor/metatrain](https://github.com/metatensor/metatrain)** · [PR #1003](https://github.com/metatensor/metatrain/pull/1003) — Fixed a crash when `validation_set` size was zero. The existing constraint rejected `>= 0` as invalid; relaxed it to allow zero-sized splits for training-only workflows. Merged January 2026, 17 CI checks passed.

---

## Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![ROS2](https://img.shields.io/badge/ROS2-22314E?style=flat&logo=ros&logoColor=white)
![PyTorch Geometric](https://img.shields.io/badge/PyG-3C2179?style=flat&logo=pytorch&logoColor=white)
![STM32](https://img.shields.io/badge/STM32-03234B?style=flat&logo=stmicroelectronics&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)
