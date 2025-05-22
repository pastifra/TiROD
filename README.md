# TiROD: Tiny Robotics Dataset and Benchmark for Continual Object Detection

<div align="center">
<img src="images/TiROD.png" width="400"/>
</div>

## Abstract
This is the official website for the TiROD dataset and benchmark.

Detecting objects in mobile robotics is crucial for numerous applications, from autonomous navigation to inspection.
However, robots are often required to perform tasks in different domains with respect to the training one and need to adapt to these changes.
Tiny mobile robots, subject to size, power, and computational constraints, encounter even more difficulties in running and adapting these algorithms.
Such adaptability, though, is crucial for real-world deployment, where robots must operate effectively in dynamic and unpredictable settings.
In this work, we introduce a novel benchmark to evaluate the continual learning capabilities of object detection systems in tiny robotic platforms. Our contributions include: 

-  Tiny Robotics Object Detection~(TiROD), a comprehensive dataset collected using a small mobile robot, designed to test the adaptability of object detectors across various domains and classes;
-  an evaluation of state-of-the-art real-time object detectors combined with different continual learning strategies on this dataset, providing detailed insights into their performance and limitations;
-  moreover, we publish the data and the code to replicate the results to foster continuous advancements in this field.
Our benchmark results indicate key challenges that must be addressed to advance the development of robust and efficient object detection systems for tiny robotics.

## 🌐 Links
* [Paper Code](https://github.com/pastifra/TiROD_code)
* [Data Download](https://zenodo.org/records/13834550)
* [Paper PDF](https://arxiv.org/pdf/2409.16215)
* [Video](https://www.youtube.com/watch?v=e76m3ol1i4I)

## 📹 Dataset Video
Check out the demo video of the dataset (click the image):

[![Watch the video](images/youtube.png)](https://www.youtube.com/watch?v=e76m3ol1i4I)

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
| **Download Link**| [Download Dataset](https://zenodo.org/records/13834550)                          |

The distribution of labels across different tasks can be observed in the following figure.
<div align="center">
<img src="images/dataset.png" width="700"/>
</div>

## 💻 Data Preview
Here are some example frames from each of the 10 CL tasks:

<div align="center">
<img src="images/TiROD_images.png" width="900"/>
</div>

## 📂 Folder Structure:

```
TiROD
├── Domain1
│   ├── High
│   │   ├── annotations
│   │   │   ├── train.json
│   │   │   ├── val.json
│   │   │   ├── test.json
│   │   ├── images
│   │   │   ├── train
│   │   │   │   ├── frame1.png
│   │   │   │   ├── ...
│   │   │   ├── val
│   │   │   │   ├── ...
│   │   │   ├── test
│   │   │   │   ├── ...
│   ├── Low
│   │   ├── ...
├── ...
└── docs
    └── README.md
```

## TiROD Benchmark results

Results for the implementation of **NanoDet Plus**

| Method               | Final mAP ↑  | RSD ↑ | RPD ↑ |
|----------------------|------|-------|-------|
| Fine-Tuning           | 10.7 | 0.17  | 0.97  |
| LWF                  | 12.6 | 0.27  | 0.98  |
| IncDet               | 12.9 | 0.18  | 0.91  |
| SID                  | 16.4 | 0.41  | 0.84  |
| Replay               | 37.8 | 0.70  | 0.74  |
| Temporal Replay      | 25.9 | 0.50  | 0.96  |
| K-Means Replay       | **42.2** | **0.75** | **0.95** |
| Latent Distillation  | 14.5 | 0.38  | 0.76  |
| Latent Replay        | 36.5 | 0.65  | 0.90  |
| Latent K-Means Replay    | 37.8 | 0.68  | 0.90  |
| **Joint Training [mAP]** |  **63%**  |

Results for **YOLOv8 nano**

| Method               | Final mAP ↑  | RSD ↑ | RPD ↑ |
|----------------------|------|-------|-------|
| Fine-Tuning           | 15.9% | 0.19  | 1.00 |
| SID                  | 17.1% | 0.24  | 1.00 |
| Replay               | 40.7% | 0.70  | 0.95  |
| K-Means Replay       | **41.3** | **0.75** | **0.99** |
| **Joint Training [mAP]** |  **59%**  |

To replicate the results, clone this [repository](https://github.com/pastifra/TiROD_code) and follow the instructions of the Readme.md

For the YOLOv8 nano implementation, use this repository [repository](https://github.com/riccardodmts/TiROD_YOLO)

## Citation

If you find this project useful in your research, please add a star and cite us 😊 

```BibTeX
@misc{pasti2024tinyroboticsdatasetbenchmark,
      title={Tiny Robotics Dataset and Benchmark for Continual Object Detection}, 
      author={Francesco Pasti and Riccardo De Monte and Davide Dalle Pezze and Gian Antonio Susto and Nicola Bellotto},
      year={2024},
      eprint={2409.16215},
      archivePrefix={arXiv},
      primaryClass={cs.RO},
      url={https://arxiv.org/abs/2409.16215}, 
}
```

****

## Related works

```BibTeX
@inproceedings{pasti2024LatentDistillation,
  title={Latent Distillation for Continual Object Detection at the edge.},
  author={Pasti, Francesco and Ceccon, Marina and Dalle Pezze, Davide and Paissan, Francesco and Farella, Elisabetta and Susto, Gian Antonio and Bellotto, Nicola},
  booktitle={ECCV 2024 Workshops},
  year={2024},
  publisher={Springer}
}
```
[https://github.com/pastifra/Continual_Nanodet](https://github.com/pastifra/Continual_Nanodet)

## Thanks

[https://github.com/RangiLyu/nanodet](https://github.com/pastifra/Continual_Nanodet)


