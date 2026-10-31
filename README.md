# 🖼️ AI-Based Image Caption Generator Using Deep Learning

An AI-powered Image Caption Generator that automatically generates meaningful natural-language descriptions for uploaded images using **BLIP (Bootstrapping Language-Image Pre-training)**.

The project uses a pretrained BLIP model from Salesforce and provides an interactive interface built with Gradio.

## 🚀 Project Overview

Image Caption Generation is a Deep Learning application that combines Computer Vision and Natural Language Processing (NLP) to understand image content and generate descriptive sentences.

Users can upload an image, and the model analyzes its visual features to generate a relevant textual description.

## ✨ Features

- Upload images in an interactive interface.
- Automatically generate natural-language captions.
- Uses a pretrained BLIP deep learning model.
- Supports different image inputs.
- Interactive web interface using Gradio.
- GPU acceleration through Google Colab.

## 🧠 Deep Learning Architecture

**BLIP – Bootstrapping Language-Image Pre-training**

The project uses the pretrained `Salesforce/blip-image-captioning-base` model.

The architecture combines:

- **Vision Transformer (ViT):** Extracts visual representations from input images.
- **Text Transformer:** Generates natural-language descriptions based on visual information.
- **Image-Text Pretraining:** Enables the model to understand relationships between visual content and language.

### Workflow

1. User uploads an image.
2. Image preprocessing is performed using BLIP Processor.
3. The Vision Transformer extracts image representations.
4. The language decoder generates a caption.
5. The generated caption is displayed through Gradio.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| PyTorch | Deep Learning framework |
| Hugging Face Transformers | Pretrained BLIP model |
| BLIP | Image caption generation |
| PIL (Pillow) | Image processing |
| Gradio | Interactive user interface |
| Google Colab | Model execution |
| T4 GPU | Hardware acceleration |

## 📂 Project Structure

```text
Image-Caption-Generator/
│
├── Image_Caption_Generator.ipynb
└── README.md
```

## ⚙️ Installation and Execution

### 1. Clone the repository

```bash
git clone https://github.com/mirzashanehyder/Image-Caption-Generator.git
```

### 2. Open Google Colab

Upload the notebook or open it directly from the repository.

### 3. Install dependencies

```python
!pip install transformers sentencepiece accelerate gradio
```

### 4. Load the pretrained model

```python
from transformers import BlipProcessor, BlipForConditionalGeneration
import torch

device = "cuda" if torch.cuda.is_available() else "cpu"

processor = BlipProcessor.from_pretrained(
    "Salesforce/blip-image-captioning-base"
)

model = BlipForConditionalGeneration.from_pretrained(
    "Salesforce/blip-image-captioning-base"
).to(device)
```

### 5. Run the application

Execute the remaining notebook cells to launch the Gradio interface.

Upload an image and generate its caption.

## 📸 Expected Output

Example:

**Input:** An image of a dog playing with a ball in a grassy field.

**Generated Caption:**

```text
A dog running in the grass with a ball in its mouth.
```

## 📊 Applications

- Image accessibility for visually impaired individuals.
- Automatic image description.
- Content organization and image indexing.
- Digital asset management.
- Image-based search systems.
- Assistive technologies.

## 🔮 Future Enhancements

- Support for multiple languages.
- More detailed image descriptions.
- Integration with text-to-speech.
- Real-time image caption generation.
- Mobile application integration.

## 👨‍💻 Author

**Mirza Shane Hyder**

B.Tech – Computer Science and Engineering

GitHub: [@mirzashanehyder](https://github.com/mirzashanehyder)

## 📜 Acknowledgements

- [Salesforce BLIP](https://huggingface.co/Salesforce/blip-image-captioning-base)
- [Hugging Face Transformers](https://huggingface.co/docs/transformers)
- [Google Colab](https://colab.research.google.com/)
- [Gradio](https://www.gradio.app/)

---

⭐ If you find this project interesting, consider giving the repository a star!
