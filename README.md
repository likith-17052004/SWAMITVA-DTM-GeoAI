# Geo-AI Hackathon: DTM Generation & Drainage Network using PointNet

## 🏆 Achievement

This project was developed as part of the **National Geo-AI Hackathon (Techfest 2025–26, IIT Bombay)** which was conducted in collaboration with the Ministry of Panchayati Raj.

🥈 **Awarded 2nd Prize for Team Alpha(Theme 2: DTM Creation & Drainage Network Design)**

---

## 📌 Problem Statement


Rural areas in India frequently face flooding and waterlogging due to poor drainage planning and lack of topographic intelligence. The **data used in this project is collected under the SWAMITVA Scheme by the Ministry of Panchayati Raj**, leveraging high-resolution drone surveys and geospatial technologies.

With the availability of such drone-based point cloud data, there is an opportunity to:

* Generate **Digital Terrain Models (DTM)** using AI/ML
* Identify **natural water flow paths and low-lying regions**
* Predict **waterlogging hotspots**
* Design **optimized drainage networks** for rural (abadi) areas

---

## 🚀 Solution Overview

This repository provides an end-to-end pipeline for:

1. **Point Cloud Classification** using deep learning (PointNet-based architecture)
2. **Ground Point Extraction** from raw LiDAR/point cloud data
3. **DTM Generation** from classified ground points
4. **Hydrological Analysis** for:

   * Flow direction
   * Flow accumulation
   * Waterlogging detection
5. **Drainage Network Design** using GIS-based optimization

---

## 🧠 Model Architecture

We use a modified **PointNet** architecture for point cloud classification:

* Input: Nx3 (XYZ coordinates)
* Feature Learning: Shared MLP layers
* Global Feature Extraction via Max Pooling
* Classification Head for ground vs non-ground points

Enhancements:

* Data normalization and augmentation
* Class balancing for imbalanced terrain classes
* Batch-wise training for scalability


## 📂 Repository Structure
├── training.ipynb   # Training notebook (PointNet implementation)
├── requirements.txt         # Dependencies
└── README.md

```
---

## ⚙️ Installation


bash
git clone https://github.com/likith-17052004/SWAMITVA-DTM-GeoAI.git
cd SWAMITVA-DTM-GeoAI
pip install -r requirements.txt

```


---

## ▶️ Usage

### 1. Train the Model

```
bash
python src/train.py --config configs/train.yaml
```

### 2. Run Inference

```
bash
python src/inference.py --input data/sample.las
```
```
bash
python src/dtm.py --input outputs/classified_points.las
```


---

## 📊 Results

- Accurate classification of **ground vs non-ground points**
- High-quality **DTM generation**
- Effective identification of **waterlogging zones**
- Optimized **drainage network design**

---

## 🗺️ Applications

- Rural infrastructure planning
- Flood risk assessment
- Smart village development
- Government GIS workflows (SVAMITVA scheme)

---

## 🔮 Future Work

To enhance the robustness, scalability, and real-world applicability of this pipeline, the following directions are proposed:

- **Scalability & Deployment**: Extend the current pipeline to handle large-scale, multi-village datasets with efficient batch processing and cloud-based deployment.
- **Automation of End-to-End Workflow**: Integrate all stages—from point cloud ingestion to drainage network generation—into a fully automated, production-ready pipeline.
- **Real-time Integration**: Enable compatibility with real-time or near real-time drone data acquisition systems for faster decision-making.
- **Incorporation of Environmental Factors**: Enhance hydrological analysis by integrating rainfall data, soil properties, and seasonal variations.
- **Web-based GIS Platform**: Develop an interactive dashboard for visualization, analysis, and decision support for government agencies and planners.
- **Impact at Scale**: With sufficient computational resources and institutional support, this pipeline has the potential to significantly reduce manual surveying, terrain analysis, and drainage planning efforts, enabling faster, more consistent, and scalable rural infrastructure planning.

---

## 🤝 Contributors

- [Likith Muni Narakala](https://www.linkedin.com/in/likith-muni-narakala-7b525722a/)
- [Manas Avinashe](https://www.linkedin.com/in/manas-avinashe-011907229/)
- [Shubhashish Saha](https://www.linkedin.com/in/shubhashish-saha/)

---

## 📦 Dataset Access

The dataset used in this project is part of the **SWAMITVA Scheme** and is not publicly hosted.

- 📩 The dataset can be made available **upon reasonable request**.
- 🤝 Interested users are encouraged to **contact the authors of this repository** for access.

---

## 📜 License

This project is licensed under the MIT License.

---

## ⭐ If you found this useful
Give this repo a ⭐ and feel free to contribute!

---

## 🤝 Future Collaboration

We are open to collaborations and suggestions to enhance this project!

**We are looking to scale this idea into a complete, production-ready product** and are actively seeking talented individuals and teams to join us on this exciting journey.

### Why Join Us?
- Transform research into real-world impact for rural infrastructure development
- Work on cutting-edge geospatial AI and machine learning technologies
- Contribute to government-scale projects (SWAMITVA Scheme)
- Build a scalable SaaS platform for drainage and terrain analysis

### How to Get Involved
If you're interested in collaborating, contributing, or joining our product development team, reach out!

📧 **Contact:** [likith.narakala@gmail.com](mailto:likith.narakala@gmail.com)

Feel free to reach out if you're interested in contributing, have ideas for improvements, or want to discuss potential applications of this work.

