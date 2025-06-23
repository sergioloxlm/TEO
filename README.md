
# 🧠 TEO — Textile Exploration Operator

**An AI-powered multimodal agent that identifies clothing from two photos and automatically generates a full technical and environmental impact sheet.**

---

## 📌 Project Description

**TEO** (Textile Exploration Operator) is a smart assistant designed to analyze clothing using **two images**:

1. A general photo of the garment
2. A close-up of the inner label

Based on this, it generates an accurate technical profile including garment type, target gender, color, material, size, country of origin, and care instructions. But TEO goes further: it also estimates the **CO₂ emissions**, **water usage**, and **natural resource consumption** based on the material and origin data — giving a full picture of the garment's environmental footprint.

---

## 🎯 Goal

* Automate the identification and classification of clothing for platforms focused on reuse, donations, or sustainable fashion.
* Provide **environmental transparency** in fashion logistics and second-hand systems.
* Enable circular economy apps and traceability systems to better manage clothing inventory and impact.

---

## 📥 Input

1. 📷 **Photo 1:** Full view of the garment (well-lit, flat or worn).
2. 🏷️ **Photo 2:** Label photo (showing material, origin, washing symbols, size, etc.).

---

## 📤 Output: Tech + Eco Sheet

A structured output including:

| Field                | Example                        |
| -------------------- | ------------------------------ |
| Garment Type         | Shirt                          |
| Target Gender        | Male                           |
| Dominant Colors      | Navy blue with white buttons   |
| Main Material        | 100% Cotton                    |
| Country of Origin    | Made in Portugal               |
| Size                 | M                              |
| CO₂ Emissions (est.) | 2.1 kg CO₂                     |
| Water Use (est.)     | 2,700 liters                   |
| Natural Resource %   | 100% natural fibers            |
| Notes                | Wash at 30°, do not tumble dry |

---

## ⚙️ Technical Architecture

### 1. 📸 Garment Image Analysis

* Image classification model (e.g. CLIP, MobileNet, ResNet) to detect garment type and gender.
* Color extraction using OpenCV and clustering (e.g. k-means).

### 2. 🏷️ Label Image Analysis

* OCR (e.g. Tesseract, PaddleOCR, Google Vision) to extract text.
* Semantic classification using LLMs (e.g. BERT or GPT) to identify: material, country, size, care instructions.

### 3. 🌱 Environmental Estimation

* Internal database of textile impact metrics (based on LCA data sources like Ecoinvent or Higg Index).
* CO₂, water, and resource use estimations based on material and country of manufacture.

### 4. 🧠 Output Generation

* Data assembly + normalization into JSON/CSV or visual card.
* Optional connection to external APIs for live impact comparison or certification lookup.

---

## 🛠️ Tech Stack

* Python 3.11
* PyTorch / TensorFlow
* OpenCV
* Tesseract OCR
* LangChain or HuggingFace Transformers
* Optional: Gradio or Streamlit (demo interface)

---

## 🚀 Usage Flow

1. Upload the two images (garment + label).
2. TEO analyzes, classifies and estimates impact.
3. Receive a downloadable report (JSON / CSV / PDF / web card).

---

## 🔗 Potential Future Integrations

* Blockchain traceability with item-specific NFTs or tokens (e.g. DOAR).
* Marketplace listing automation for second-hand platforms.
* AI-assisted fashion filtering (by color, eco-score, material, etc.).
* Impact passport generation for brands or garments.

---

## 👥 Team

* Concept, coordination, vision: Jenny T.
* ML/AI: \[Your name or technical team]
* UX & visual design: \[Optional]

---

## 🏗️ Project Status

* [x] Project definition
* [ ] Model prototyping
* [ ] OCR + dataset testing
* [ ] Environmental data mapping
* [ ] MVP / functional demo

