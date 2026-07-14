# AI Article & Image Generator

A web application that automatically generates comprehensive articles, blog posts, paragraphs, or rewritten text alongside relevant AI-generated images based on your topic.

## Features
- **AI Text Generation:** Uses DeepInfra (Llama-2-70b) to generate high-quality text content in multiple formats:
  - Full Articles
  - Blog Posts
  - Text Rewriting
  - Detailed Paragraphs
- **AI Image Generation:** Automatically generates relevant imagery to match your topic using Hugging Face (Stable Diffusion XL), with a fallback to Replicate.
- **Modern UI:** Built with a clean Flask web interface.

## Prerequisites
- Python 3.8+
- API Keys for:
  - [DeepInfra](https://deepinfra.com/) (for text generation)
  - [Hugging Face](https://huggingface.co/) (for primary image generation)
  - [Replicate](https://replicate.com/) (for fallback image generation)

## Installation

1. Clone this repository (or navigate to the directory):
   ```bash
   git clone <repository_url>
   cd Image_Article_Generator
   ```

2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. Install required dependencies:
   ```bash
   pip install flask requests Pillow
   ```

4. Configure your API Keys:
   Open `app.py` and replace the placeholder API keys with your actual keys:
   ```python
   DEEPINFRA_API_KEY = "your_key"
   HF_API_KEY = "your_key"
   REPLICATE_API_KEY = "your_key" # Inside generate_image_replicate function
   ```

## Usage

Run the Flask application:
```bash
python app.py
```
Open your browser and navigate to `http://127.0.0.1:5000/`.

## Note
Ensure your `.gitignore` file includes `venv/` to prevent committing your local environment to version control.
