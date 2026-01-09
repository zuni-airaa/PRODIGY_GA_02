# PRODIGY_GA_02 – Image Generation with Stable Diffusion

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1u6qigQb-k0Q4CRnphkJjVcrCfaBjCI4e#scrollTo=YOmwqjSJiO03)

---

##  Project Overview
This project demonstrates text‑to‑image generation using **Stable Diffusion** and **DALL‑E‑mini**, two state‑of‑the‑art generative models.  
By providing descriptive prompts, the models generate unique and creative visuals, showcasing the potential of diffusion models in AI‑driven art and design.

---

##  Features
- Image generation from natural language prompts  
- Comparison between Stable Diffusion and DALL‑E‑mini outputs  
- Curated `prompts.txt` dataset for testing  
- Example outputs showcasing generated images  

---

##  Requirements
Install dependencies using the requirements file:

```bash
pip install -r requirements/requirements.txt

```

##  References
- HuggingFace Diffusers: [Stable Diffusion documentation](https://huggingface.co/docs/diffusers/index)  
- Colab Notebook: [Text‑to‑Image tutorial](https://colab.research.google.com/github/huggingface/notebooks/blob/main/diffusers/stable_diffusion.ipynb)  

##  Example Usage
```python
from diffusers import StableDiffusionPipeline
import torch

pipe = StableDiffusionPipeline.from_pretrained("runwayml/stable-diffusion-v1-5")
pipe = pipe.to("cuda")

prompt = "A futuristic cityscape at sunset, highly detailed, digital art"
image = pipe(prompt).images[0]

image.save("results/sample_output.png")
```

##  Results

Here are some example outputs generated using Stable Diffusion:

**Prompt:**  
`A futuristic cityscape at sunset, highly detailed, digital art`

**Generated Output:**  
*(Image stored in `results/sample_output.png`)*

---

**Prompt:**  
`A watercolor painting of mountains and lakes`

**Generated Output:**  
*(Image stored in `results/sample_output2.png`)*

---

Sample outputs are stored in the `results/` folder for reference.

##  Repository Structure

```
PRODIGY_GA_02/
├── notebooks/
│   └── PRODIGY_GA_02.ipynb
├── data/
│   └── prompts.txt
├── results/
│   └── samples/
│       ├── output_1.png
│       ├── output_2.png
│       ├── output_3.png
│       ├── output_4.png
│       └── output_5.png
├── requirements/
│   └── requirements.txt
└── README.md


