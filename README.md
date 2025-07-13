# SwarmTrack

**SwarmTrack: Swarm-Coupled Motion Modeling and Trajectory-Guided Feature Fusion for Air-to-Air Multi-UAV Tracking**  
(*Under Review at IEEE Transactions on Circuits and Systems for Video Technology*)

![Qualitative Results](assets/v0.2-exp-AIRMOT-DJI-M300.png)

![Qualitative Results](assets/v0.2-exp-UAVSwarm.png)

## 📌 Abstract

Air-to-air tracking of multiple UAVs in swarm scenarios presents significant challenges due to the small object sizes, weak visual cues, and complex nonlinear group movements, often leading to detection failures, trajectory fragmentation, and identity switches. Although existing methods incorporate trajectory prediction, they often model each object independently and fail to capture swarm-level coupling. Moreover, trajectory and appearance features are rarely integrated effectively.

We propose **SwarmTrack**, a novel tracking framework that introduces:
- **SMTP** (Swarm Motion-Aware Trajectory Prediction): to capture nonlinear, group-coupled motion dynamics and posture-aware appearance features.
- **TG-STFF** (Trajectory-Guided Spatio-Temporal Feature Fusion): to guide the fusion of predicted positions with current-frame features, improving spatial discriminability and temporal consistency.

Experiments on **AIRMOT**, **MOT-FLY**, and **UAVSwarm** datasets demonstrate that SwarmTrack significantly outperforms state-of-the-art methods in both accuracy and robustness.

## 📊 Benchmark Results

| Dataset  | MOTA ↑ | IDF1 ↑ | HOTA ↑ | IDSW ↓ | FPS ↑ |
| -------- | ------ | ------ | ------ | ------ | ----- |
| AIRMOT   | 32.30  | 30.15  | 25.54  | 476    | 21.8  |
| MOT-FLY  | 72.52  | 79.31  | 59.02  | 18     | 20.1  |
| UAVSwarm | 81.90  | 88.45  | 68.56  | 56     | 22.3  |

More detailed results can be found in `assets/performance_summary.md`.

## 📁 Project Structure

```bash
SwarmTrack/
│
├── assets/                         # Figures, visualizations, tables
│
├── datasets/                      # Dataset usage and download instructions
│
├── README.md
└── LICENSE
```

## 📦 Download Pre-trained Models

- [SwarmTrack_AIRMOT.pth]

  download link: https://pan.baidu.com/s/1T-7UxoEanetiZphMODuZcw?pwd=8nbp code: 8nbp 

- [SwarmTrack_MOTFLY.pth]
  download link: https://pan.baidu.com/s/1JAUQm32Cpm2ywXwugHjcZQ?pwd=72ny code: 72ny 

- [SwarmTrack_UAVSwarm.pth]
  download link: https://pan.baidu.com/s/1H0DJr8A9nqbZF7DmwKC4mA?pwd=tn45 code: tn45 

> 🚧 **Note**: Source code will be released after the paper is accepted.

## 📅 Planned Release

- ✅ Inference results and visualization
- ✅ Trained model weights (.pth)
- ✅ Dataset usage instructions
- ⏳ Source code (to be released **upon acceptance**)

## 📂 Datasets

We evaluate our method on three public datasets:

- **AIRMOT**: Real-world air-to-air UAV tracking dataset.
  download link: https://pan.baidu.com/s/1xZh2j7_xTJbKee7jsYb6aA?pwd=9a4r code: 9a4r 

- **MOT-FLY**: Synthetic dataset with fast motion.

  [CZC-123/MOT-FLY: the MOT-FLY dataset](https://github.com/CZC-123/MOT-FLY)

- **UAVSwarm**: Challenging dense UAV formation tracking.

  [UAVSwarm/UAVSwarm-dataset: UAVSwarm dataset was manually collected and annotated for UAV swarm detection and tracking, in which thirteen different scenes and more than nineteen types of UAV were recorded, including 12,598 annotated images—the number of UAV in each sequence is 3 to 23.](https://github.com/UAVSwarm/UAVSwarm-dataset)

