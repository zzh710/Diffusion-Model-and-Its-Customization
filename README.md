# Subject-Driven Text-to-Image Customization with Diffusion Models

An end-to-end repository for exploring generative diffusion architectures, text-to-image synthesis, and subject-driven customization using Custom Diffusion and BLIP-Diffusion. This project demonstrates fine-tuning pre-trained diffusion models to maintain subject consistency across novel prompts and contexts.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/zzh710/Diffusion-Model-and-Its-Customization/blob/main/My_Diffusion_Model_Project.ipynb)
![Python 3.10+](https://img.shields.io/badge/Python-3.10%2B-blue.svg)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-red.svg)
![Hugging Face Diffusers](https://img.shields.io/badge/HuggingFace-Diffusers-yellow.svg)

---

## Key Features & Highlights

- **Subject-Driven Customization:** Fine-tuned latent diffusion models using custom subject images to generate high-fidelity, context-aware images while preserving subject identity.
- **Multimodal Pipeline Integration:** Implemented inference workflows featuring Stable Diffusion and BLIP-Diffusion for controlled text-to-image generation.
- **Efficient Fine-Tuning:** Optimized training parameters over 300 steps with a learning rate of \(4 \times 10^{-5}\), achieving a training loss of approximately 0.16 under constrained computing resources using Google Colab GPUs.
- **Reproducible Workflow:** Developed an end-to-end Jupyter Notebook integrating environment setup, model checkpoint management, fine-tuning, inference, and visual evaluation.

---

## Qualitative Comparison

**Reference Subject Image:**

![Input Subject](https://github.com/user-attachments/assets/100e9963-0af9-4459-9184-320abbfe7997)

**Comparative Generation Results:**

| Method / Approach | Prompt / Context | Generated Output |
| :--- | :--- | :---: |
| **Custom Diffusion** (Fine-tuned, 300 steps) | *A photo of [subject] wearing sunglasses on a beach* | ![Custom Diffusion](https://github.com/user-attachments/assets/69250eb3-8fc8-4158-b575-a506eae8ea14) |
| **BLIP-Diffusion** (Zero-shot subject-driven) | *A photo of [subject] wearing sunglasses on a beach* | ![BLIP-Diffusion](https://github.com/user-attachments/assets/a1e49c7a-2e04-4b7f-a543-1baeafd6ed7e) |


## Tech Stack & Frameworks

- **Core Framework:** PyTorch
- **Generative AI Ecosystem:** Hugging Face Diffusers, Transformers, Accelerate
- **Model Architectures:** Latent Diffusion Models (LDM), Stable Diffusion, BLIP-Diffusion
- **Compute Environment:** Google Colab with GPU acceleration

---

## Repository Layout

```text
.
├── My_Diffusion_Model_Project.ipynb  # Training, fine-tuning, and inference pipeline
├── README.md                         # Project documentation
└── images/                           # Input and generated images (optional)
```

---

## Quick Start

### Run in Google Colab

1. Open the notebook using the Colab badge above.
2. Select a GPU runtime under **Runtime > Change runtime type**.
3. Run the notebook cells in order.

### Local Setup

Clone the repository:

```bash
git clone https://github.com/zzh710/Diffusion-Model-and-Its-Customization.git
cd Diffusion-Model-and-Its-Customization
```

Install the dependencies:

```bash
pip install torch torchvision torchaudio
pip install diffusers transformers accelerate ftfy peft
```

Open `My_Diffusion_Model_Project.ipynb` in Jupyter Notebook or VS Code and follow the notebook instructions.

**Note:** The required PyTorch version and CUDA configuration depend on your hardware and environment. Refer to the [official PyTorch installation guide](https://pytorch.org/get-started/locally/) for compatible installation commands.

---

## Citation & Acknowledgments

- [Hugging Face Diffusers](https://github.com/huggingface/diffusers) for pre-trained diffusion pipelines and generative model tools.
- Research papers on [Custom Diffusion](https://arxiv.org/abs/2212.04488) and [BLIP-Diffusion](https://arxiv.org/abs/2305.14720) for foundational concepts in subject-driven image generation.

