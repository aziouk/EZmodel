# 🚀 EZmodel  
**A collection of ComfyUI workflows for creating Reactor Face Models from large datasets**

<p align="center">
  <img width="1205" height="533" alt="comfyui-ezmodel" src="https://github.com/user-attachments/assets/d0df01a1-9a12-45a2-9eb0-cf1567fbaaf1" />
</p>
EZfacemodelmaker: Creating a single batch of models, starting from file increment #250, in batch customly defined to 25 images.


<p align="center">
  <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License: MIT"></a>
  <img src="https://img.shields.io/badge/Python-3.10+-blue.svg" alt="Python 3.10+">
  <img src="https://img.shields.io/badge/ComfyUI-Compatible-orange.svg" alt="ComfyUI Compatible">
  <img src="https://img.shields.io/badge/Reactor-Supported-purple.svg" alt="Reactor Supported">
  <img src="https://img.shields.io/github/stars/aziouk/EZmodel?style=social" alt="GitHub stars">
</p>

---

## 📚 Table of Contents
- [Overview](#-overview)
- [Key Features](#-key-features)
- [Recommended Settings](#-recommended-settings)
- [What is ComfyUI?](#-what-is-comfyui)
- [What is Reactor for ComfyUI?](#-what-is-reactor-for-comfyui)
- [How It Works](#-how-it-works)
- [Requirements](#-requirements)
- [Installation](#-installation)
- [Contributing](#-contributing)
- [License](#-license)
- [Support](#-support)

---

## 📦 What's Included

EZmodel comes with three powerful and easy-to-use workflow tools — each designed to make model creation and batch processing a breeze:

---

### 🧠 **EZFaceModelMaker**
> Generate **ReActor-compatible face models** from hundreds (or thousands!) of input images.

- 🔹 Automatically batches datasets into chunks (e.g. `median_0`, `median_1`, etc.)  
- 🔹 Perfect for large-scale dataset handling  
- 🔹 Keeps VRAM and RAM usage manageable with smart batching  

---

### 🧩 **EZReActBatchModelCombiner**
> Combine multiple face model batches into a single unified model.

- 🔹 Supports up to **10 model inputs** (`input_model_0` → `input_model_9`)  
- 🔹 Merges results from multiple batches (e.g. `median_0`–`median_9`)  
- 🔹 Great for finalizing a full composite model after multiple runs  

---

### ⚙️ **EZ-Reactor-Batch-Generator**
> Run your **combined or single model** across an entire image directory for automated face model generation.

- 🔹 Batch-processes a directory of target images  
- 🔹 Ideal for automating **ReActor model applications**  
- 🔹 Excellent for dataset-to-dataset transformations  

---

💡 *Together, these tools create a complete pipeline — from dataset → model → batch generation → final merge.*  



<p align="center">
<img width="1057" height="705" alt="image" src="https://github.com/user-attachments/assets/db6d0628-0861-4ee7-b96e-9ebe3455059a" />
</p>
EZReActBatchModelCombiner: Combines batched generated models into a single model for use


## ⚙️ Key Features

- 🧠 **Face React Model Creation**  
  Seamlessly generate **Reactor-compatible face models** from large image collections.

- 🔢 **Batching Support**  
  Specify a **start index** to resume from a particular image within your dataset.

- 🔄 **Model Merging**  
  Combine multiple model batches into a single unified model with ease.

- 🧮 **Batch Size Control**  
  Set a **maximum image-load cap** to manage memory usage — ideal for low VRAM or RAM setups.

---

## 🧠 Recommended Settings

| System Memory | Recommended Batch Size |
|----------------|------------------------|
| 32 GB          | 20–30 images per batch |
| 64 GB+         | 60+ images per batch   |

These values ensure smooth processing and prevent out-of-memory issues during workflow execution.

---

<img width="1491" height="519" alt="image" src="https://github.com/user-attachments/assets/4093a1c8-c46b-4616-858c-be675090c2cd" />
EZ-Reactor-Batch-Generator: Applie generated combined, or batched ReActor model with an entire directory batch. Useful for Reactor modeling of an entire directory en-mass. Increments +1 in target_dir per run.

## 🧰 What is ComfyUI?

**[ComfyUI](https://github.com/comfyanonymous/ComfyUI)** is a powerful, modular, and node-based user interface for Stable Diffusion and related AI model workflows.  
It allows users to visually construct complex model pipelines, customize every parameter, and chain nodes together for image generation, model training, or fine-tuning tasks — all without needing to code.

EZmodel builds on top of ComfyUI’s node-based architecture to provide ready-to-use, optimized workflows for model creation.

---

## 🔥 What is Reactor for ComfyUI?

**[Reactor](https://github.com/Gourieff/comfyui-reactor-node)** is an advanced ComfyUI node designed for **face swapping and model blending** using AI.  
It enables users to swap, train, and fine-tune face models directly within ComfyUI’s ecosystem.  

EZmodel enhances this process by providing a **batch-optimized workflow** to generate the face models Reactor uses — saving hours of manual setup.

---

## 🧭 How It Works

1. **Prepare your dataset** – organize images of the subject(s) you want to model.  
2. **Load EZmodel workflow** – open it inside ComfyUI.  
3. **Configure your batch parameters** – define start index, batch size, and model name.  
4. **Run workflow** – EZmodel processes the dataset and outputs the model(s).  
5. *(Optional)* **Merge batches** – combine partial models into a single unified Reactor face model.

---

## 🧑‍💻 Requirements

- [ComfyUI](https://github.com/comfyanonymous/ComfyUI)
- [Reactor Node](https://github.com/Gourieff/comfyui-reactor-node)
- [ComfyUI-Inspire-Pack](https://github.com/ltdrdata/ComfyUI-Inspire-Pack)
- Python 3.10+
- Stable Diffusion compatible environment (GPU recommended)

---

## 📦 Installation

1. Clone or download this repository:
   ```bash
   git clone https://github.com/aziouk/EZmodel.git
