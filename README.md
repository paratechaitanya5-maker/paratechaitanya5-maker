# Chaitanya Parate

B.Tech Computer Science (AI & Data Science) · MIT-WPU, Pune · 2027  
Building at the intersection of robotics, deep learning, and systems engineering.  
Open to ML/AI research internships.

---

## Experience

**Research Intern (AI & Robotics) · Centre for Artificial Intelligence and Robotics (CAIR), IIT Mandi** · Jul 2026 – Dec 2026

- Developed and trained deep RL control policies for quadrupedal locomotion in simulation with domain randomization for sim-to-real transfer
- Engineered low-latency ROS 2 communication pipelines using UNIX domain sockets bridging C++ and Python environments
- Converted trained PyTorch networks to ONNX / C++ binaries for deployment on Jetson edge hardware
- Deployed and stabilized inference on physical hardware, compensating for real-world friction and sensor noise

**Embedded Systems Engineer · Team Vegapod Hyperloop, MIT-WPU** · Aug 2024 – Nov 2025

- Developed real-time firmware for hyperloop subsystems using STM32, FreeRTOS, UART, SPI, CAN, I2C
- Built fault-detection and sensor integration pipelines under strict latency requirements
- Represented MIT-WPU at European Hyperloop Week 2025, Netherlands

---

## Projects

### [Heterogeneous GNN Morphology Transfer](https://github.com/ChaitanyaParate/hetero-gnn-morphology-transfer) [![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.20187567-blue.svg)](https://doi.org/10.5281/zenodo.20187567)

Zero-shot locomotion policy transfer across robot morphologies using a 31,582-parameter heterogeneous GNN (GATv2Conv + PPO), with YOLOv8 perception and LLM-guided navigation deployed on ROS2 Jazzy + Gazebo.

- **Zero-shot quadruped → hexapod transfer** (12-DOF → 18-DOF): 106 ± 25 reward, ~47 steps survival. MLP hard-fails with RuntimeError on any unseen morphology — fixed-input-dim structural limitation
- **500K-step fine-tuning**: 3.8× reward gain (110 → 416 ± 114), survival 47 → 193 steps
- **85% fewer parameters** than MLP baseline (31,582 vs 210,457), while MLP scores higher in-distribution only — GNN trades peak reward for architectural generalization
- **Terrain robustness** (zero-shot, no terrain training): 95% success at 5° slope, 0% at 10°
- Deployed at 200 Hz with yaw-rate PI correction (HAA joint offset) to eliminate circular drift from training bias
- LLM planning layer: Qwen 2.5 7B via Ollama, natural language → skill → GNN → joint commands, fully on-device

### [SE-Attention Half-UNet](https://github.com/ChaitanyaParate/SE-Attention-Half-UNet)
Polyp segmentation model combining attention gates and SE blocks with BCE-Dice loss. Evaluated on Kvasir-SEG. Dice: 0.9436.

### [DeskAI](https://github.com/ChaitanyaParate/Deskai)
Local-first Linux desktop AI daemon. Persistent daemon with UNIX socket IPC, X11/OCR context tracking, and streaming LLM inference via Ollama with online fallback.

- Intent router dispatches to typed executors (summarize, explain_error, search)
- Fault-tolerant streaming pipeline with full daemon-client lifecycle decoupling
- Internet-aware backend switching without daemon restart

### [stm32-hyperloop-embedded](https://github.com/ChaitanyaParate/stm32-hyperloop-embedded)
STM32 firmware in C for Team Vegapod. Custom Bluetooth bootloader, FreeRTOS BMS/VCU braking, 3-phase inverter PWM, CAN bus. Represented MIT-WPU at European Hyperloop Week 2025.

### Other
[ResNet-50 from scratch](https://github.com/ChaitanyaParate/ResNet50-From-Scratch-Pytorch-Imagenette) (86.63% on Imagenette, live ESP32-CAM inference) · [Brain Tumor MRI Classification](https://github.com/ChaitanyaParate/Modified-Half-UNet-for-Medical-Image-Classification) (98% accuracy, encoder-only Half-UNet)

---

## Open Source

**[metatensor/metatrain](https://github.com/metatensor/metatrain)** · Fixed zero-sized validation split edge case in ML training pipelines. [PR #1003](https://github.com/metatensor/metatrain/pull/1003) merged January 2026.

---

## Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![PyTorch Geometric](https://img.shields.io/badge/PyG-3C2179?style=flat&logo=pytorch&logoColor=white)
![ROS2](https://img.shields.io/badge/ROS2_Humble-22314E?style=flat&logo=ros&logoColor=white)
![Gazebo](https://img.shields.io/badge/Gazebo-F58113?style=flat&logo=gazebo&logoColor=white)
![PyBullet](https://img.shields.io/badge/PyBullet-346F9F?style=flat&logo=python&logoColor=white)
![ONNX](https://img.shields.io/badge/ONNX-005CED?style=flat&logo=onnx&logoColor=white)
![TensorRT](https://img.shields.io/badge/TensorRT-76B900?style=flat&logo=nvidia&logoColor=white)
![YOLOv8](https://img.shields.io/badge/YOLOv8-111F68?style=flat&logo=yolo&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat&logo=ollama&logoColor=white)
![FreeRTOS](https://img.shields.io/badge/FreeRTOS-8CC84B?style=flat&logo=freertos&logoColor=white)
![STM32](https://img.shields.io/badge/STM32-03234B?style=flat&logo=stmicroelectronics&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)

---

[LinkedIn](https://www.linkedin.com/in/chaitanyaparate) · paratechaitanya5@gmail.com
