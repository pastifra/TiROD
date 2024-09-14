# TiROD: Tiny Robotics Dataset and Benchmark for Continual Object Detection

![Dataset Logo](images/TiROD.png)

---

## Overview

**TiROD** is a benchmark to evaluate the performances of Continual Learning for Object Detection algorithms based on the data collected by a tiny robot rover.
We define 10 distinct CL tasks, characterized by the 5 different environments explored by the robot and the two illumination conditions. The tasks range from d1_h (read Domain 1, High illumination) to d5_l (Domain 5, Low illumination). The first two tasks correspond to an indoor environment, while the remaining ones are outdoor.

TiROD addresses the challenges of both Domain Incremental and Class Incremental Learning, requiring CLOD systems to adapt to domain shifts and varying data distributions.
Moreover, by capturing the data with a low-cost sensor of the Tiny Robot, TiROD raises additional challenges that must be addressed in real-world tiny robotics scenarios such as noise and motion blur in the images.

---

## 📊 Dataset Information

| Attribute        | Description                                              |
|------------------|----------------------------------------------------------|
| **Name**         | TiROD                                                    |
| **Size**         | 2 GB                                                     |
| **Number of Images** | 6.7K                                                 |
| **Number of Classes** | 13                                                  |
| **Number of BBoxes** | 17.9K                                                |
| **Data Format**  | png                                                      |
| **Annotations**  | COCO format                                              |
| **Download Link**| [Download Dataset](coming_soon)                          |

The distribution of labels across different tasks can be observed in the following figure.
![Datastats](images/dataset.pdf)
---

## 💻 Preview
![Examples](images/TiROD_images.pdf)

---

## 📹 Demo Video

Check out the demo video of the dataset:

[![Watch Video](coming-soon)

---

## 🧑‍💻 Usage Instructions
Coming soon

---

## Benchmark
Results for the implementation of **NanoDet Plus**

| Method               | Ω ↑  | RSD ↑ | RPD ↑ |
|----------------------|------|-------|-------|
| Fine-Tuning           | 0.19 | 0.19  | 0.99  |
| LWF                  | 0.24 | 0.27  | 0.95  |
| IncDet               | 0.20 | 0.27  | 0.99  |
| SID                  | 0.27 | 0.44  | 0.86  |
| Replay               | 0.63 | 0.70  | 0.95  |
| Temporal Replay      | 0.48 | 0.54  | 0.96  |
| K-Means Replay       | **0.65** | **0.75** | **0.99** |
| Latent Distillation  | 0.26 | 0.38  | 0.69  |
| Latent Replay        | 0.62 | 0.67  | 0.91  |
| **Joint Training [mAP]** | **0.66** |       |       |

To replicate the results, clone the [Repository](coming_soon)  and follow the instructions of the Readme.md 

## 📂 Folder Structure

```plaintext
TiROD/
├── Domain1/
│   ├── High
|       ├── annotations
|           ├── train.json
|           ├── val.json
|           ├── test.json
|       ├── images
|           ├── train
|               ├── frame1.png
|               ├── ...
|           ├── val
|               ├── ...
|           ├── test
|               ├── ...
│   ├── Low
|       ├── ...
├── ...
└── docs/
    └── README.md
