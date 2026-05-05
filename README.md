# AI-Image-Generator-FP16-Optimized-Stable-Diffusion-XL
Generate high-resolution AI images from text prompts using Stable Diffusion XL with FP16 acceleration for faster GPU performance. Built with Flask, PyTorch, and Diffusers, featuring real-time generation, prompt suggestions, and an interactive UI.

Features
🧠 Stable Diffusion XL (SDXL) for high-quality image generation
⚡ Fast GPU-based inference
🎯 Prompt-based image creation
💡 AI-powered prompt suggestions
🖼️ Multiple styles (Anime, Photorealistic, Fantasy, etc.)
📐 Adjustable resolution & layout
📜 Generation history preview
🏗️ Architecture
Frontend (Flask UI)
User prompt input
Style & resolution selection
Image preview
Backend (AI Server)
SDXL model for image generation
GPT model for prompt suggestions

Workflow

Prompt → CLIP Encoder → Latent Noise → U-Net Denoising → VAE Decode → Image
🖥️ Tech Stack
Python 🐍
Flask 🌐
Stable Diffusion XL 🤖
HuggingFace Diffusers
PyTorch 🔥
Transformers (GPT2)
Ngrok (API tunneling)
⚙️ Installation
1️⃣ Clone Repo
git clone https://github.com/your-username/sdxl-studio.git
cd sdxl-studio
2️⃣ Install Dependencies
pip install -r requirements.txt
3️⃣ Run Backend (Colab / GPU)
Start SDXL API server
Copy Ngrok URL
4️⃣ Update API URLs
GENERATE_API = "YOUR_NGROK_URL/api/generate"
RECOMMEND_API = "YOUR_NGROK_URL/api/recommend"
5️⃣ Run Frontend
python app.py
🧪 API Endpoints
🔹 Generate Image
POST /api/generate

Request:

{
  "prompt": "A futuristic city at sunset"
}

Response:

{
  "image": "base64_string"
}
🔹 Prompt Recommendations
POST /api/recommend
📂 Project Structure
sdxl-studio/
│
├── app.py                # Flask frontend
├── templates/
│   ├── index.html
│   ├── generate.html
│   ├── about.html
│   ├── architecture.html
│
├── static/
│   ├── css/
│   ├── js/
│   ├── images/
│
├── assets/
│   └── demo.gif         # Demo GIF
│
└── README.md
