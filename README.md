# Text-to-Image Diffusion

A Generative AI project for **text-to-image generation** using modern diffusion models with Hugging Face Diffusers.

## Models Used

- **SDXL Turbo** — fast text-to-image generation
- **Stable Diffusion XL + Refiner** — two-stage image generation and refinement
- **FLUX.1 Schnell** — fast, high-quality text-to-image generation

The project is designed for GPU-based inference using PyTorch and CUDA.

## Project Structure

```text
Text-to-Image-Diffusion/
├── text_to_image.py
├── requirements.txt
├── README.md
├── .gitignore
├── .env.example
└── examples/
```

## Requirements

- Python 3.10+
- NVIDIA GPU with CUDA support
- CUDA-enabled PyTorch
- Hugging Face Diffusers
- Sufficient GPU VRAM for the selected model

> These models are computationally intensive, so GPU execution is recommended.

## Installation

Clone the repository:

```bash
git clone https://github.com/chetan0722/Text-to-Image-Diffusion.git
cd Text-to-Image-Diffusion
```

Create a virtual environment:

```bash
python -m venv .venv
```

### Windows

```bash
.venv\Scripts\activate
```

### Linux/macOS

```bash
source .venv/bin/activate
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

For CUDA-enabled PyTorch, install the version appropriate for your NVIDIA GPU and CUDA environment from the official PyTorch installation instructions.

## Usage

### FLUX.1 Schnell

```bash
python text_to_image.py --model flux --prompt "A futuristic AI laboratory at night"
```

### SDXL Turbo

```bash
python text_to_image.py --model sdxl-turbo --prompt "A futuristic city with flying cars"
```

### SDXL + Refiner

```bash
python text_to_image.py --model sdxl-refiner --prompt "A majestic lion jumping from a stone at night"
```

The generated image is saved to:

```text
examples/generated_image.png
```

## Hugging Face Authentication

The project does **not** store a Hugging Face access token in the source code.

If a model requires authentication, set the `HF_TOKEN` environment variable:

### Windows PowerShell

```powershell
$env:HF_TOKEN="your_huggingface_token"
```

### Linux/macOS

```bash
export HF_TOKEN="your_huggingface_token"
```

Never commit a real token, password, or API key to GitHub.

## Concepts Demonstrated

- Generative AI
- Diffusion Models
- Text-to-Image Generation
- Hugging Face Diffusers
- Stable Diffusion XL
- SDXL Refiner
- FLUX.1 Schnell
- Prompt Engineering
- PyTorch
- CUDA GPU Inference

## Example Prompt

```text
A class of data scientists learning AI engineering in a vibrant high-energy pop-art style
```

## Future Improvements

- Add a Streamlit web interface
- Add image-to-image generation
- Add negative-prompt support where supported
- Add configurable image resolution
- Add batch image generation
- Add model comparison and inference-time benchmarking

## License

This repository contains code for educational and portfolio purposes.

The downloaded model weights are subject to the licenses and terms of their respective model repositories.
