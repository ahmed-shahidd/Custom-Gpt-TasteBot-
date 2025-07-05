# TasteBot: Your AI Cooking Assistant

![TasteBot Banner](screenshots/tastebot_banner.png)

TasteBot is a custom fine-tuned GPT-based conversational assistant designed to answer cooking questions, generate recipes, and provide culinary guidance for users of all skill levels. Powered by state-of-the-art language models and a user-friendly Gradio interface, TasteBot brings the power of AI to your kitchen.

---

## Table of Contents

- [Features](#features)
- [Demo](#demo)
- [Screenshots](#screenshots)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Datasets & Model Training](#datasets--model-training)
- [Customization](#customization)
- [Troubleshooting](#troubleshooting)
- [License](#license)
- [Acknowledgements](#acknowledgements)

---

## Features

- **Conversational Cooking Assistant:** Ask any cooking-related question and get instant, AI-generated answers.
- **Recipe Generation:** Generate recipes based on ingredients, cuisine, or dietary preferences.
- **PDF Upload:** Extract and process recipes or cooking notes from PDF files.
- **Multiple User Types:** Tailored responses for Professional Chefs, Home Cooks, Beginners, and Food Enthusiasts.
- **Fine-Tuned Models:** Utilizes multiple fine-tuned GPT-2 models for enhanced culinary knowledge.
- **Modern UI:** Clean, responsive Gradio interface for seamless interaction.

---

## Demo

> **Note:** You can run TasteBot locally or deploy it on a cloud platform.  
> [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

---

## Screenshots

### Main Interface

![TasteBot Main Interface](/Screenshots/main%20interface.png)


### PDF Upload

![TasteBot PDF Upload](/Screenshots/pdf%20upload%20.png)

---

## Installation

### 1. Clone the Repository

```sh
git clone https://github.com/Muhamad-Ahmed/Custom-Gpt-TasteBot-.git
cd Custom-Gpt-TasteBot-/Code
```

### 2. Install Dependencies

Install the required Python packages:

```sh
pip install -r ../Requirements/requirements.txt.txt
```

> **Note:** If you encounter missing package errors, install them manually as suggested in [guide.txt](../Requirements/guide.txt).

### 3. Prepare Configuration

- Add your `config.json` file with your Hugging Face token:
    ```json
    {
      "HF_TOKEN": "your_huggingface_token"
    }
    ```
- Place your datasets (PDF, CSV, TXT, JSON) in the appropriate paths and update the file paths in the code.

---

## Usage

### 1. Launch the Application

You can run the Gradio interface using:

```sh
python main.py
```
or, if using Jupyter/Colab:

```sh
jupyter notebook main.ipynb
```

### 2. Access the Interface

- Open the provided local URL in your browser (e.g., http://localhost:7860).
- Choose your user type, select a model, enter your cooking question, or upload a PDF file.
- Click **Get Response** to interact with TasteBot.

---

## Project Structure

```
Code/
    main.ipynb         # Jupyter Notebook version
    main.py            # Main Python script
Requirements/
    guide.txt          # Setup and troubleshooting guide
    requirements.txt.txt # List of required Python packages
```

---

## Datasets & Model Training

- **Custom Datasets:** You must provide your own datasets for training (PDF, CSV, TXT, JSON).
- **Model Training:** The code supports fine-tuning GPT-2 models using Hugging Face Transformers and Datasets libraries.
- **Model Export:** Fine-tuned models are saved locally and can be uploaded to Hugging Face Hub for sharing or deployment.

---

## Customization

- **Add More Models:** Fine-tune additional models and add their paths to the `model_dirs` list in the code.
- **UI Customization:** Modify the Gradio Blocks section for a personalized look and feel.
- **Prompt Templates:** Adjust the prompt templates for different user types in the `get_response` function.

---

## Troubleshooting

- **Missing Packages:** Install any missing packages as indicated by error messages.
- **CUDA/CPU Issues:** The code automatically falls back to CPU if CUDA is unavailable.
- **Model Loading Errors:** Ensure your Hugging Face token is valid and models are accessible.

For more help, refer to [guide.txt](../Requirements/guide.txt).

---

## License

This project is licensed under the MIT License. 

---

## Acknowledgements

- [Hugging Face Transformers](https://huggingface.co/transformers/)
- [Gradio](https://gradio.app/)
- [PyTorch](https://pytorch.org/)
- [Datasets](https://huggingface.co/docs/datasets/)

---

*For questions or contributions, please open an issue or submit a pull request.*
