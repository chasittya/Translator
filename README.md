# Multilingual Translator Application

A Python-based multilingual translation project that translates English text into Hindi, Spanish, French, Arabic, and Portuguese using Hugging Face MarianMT models.

## Overview
This project explores multilingual neural machine translation using pretrained and fine-tuned sequence-to-sequence models. It includes preprocessing, translation generation, post-processing, and BLEU-based evaluation.

## Features
- Translates English into 5 target languages:
  - Hindi (`hi`)
  - Spanish (`es`)
  - French (`fr`)
  - Arabic (`ar`)
  - Portuguese (`pt`)
- Uses Hugging Face MarianMT / seq2seq translation models
- Applies text normalization and post-processing
- Evaluates translations with BLEU scores
- Visualizes BLEU score performance by language

## Tech Stack
- Python
- TensorFlow
- Hugging Face Transformers
- Hugging Face Datasets
- Evaluate
- Pandas
- Matplotlib

## Dataset
This project uses the `CohereForAI/aya_collection` dataset for multilingual translation experiments.

## Model Checkpoints
The project uses the following MarianMT checkpoints:
- `Helsinki-NLP/opus-mt-en-hi`
- `Helsinki-NLP/opus-mt-en-es`
- `Helsinki-NLP/opus-mt-en-fr`
- `Helsinki-NLP/opus-mt-en-ar`
- `Helsinki-NLP/opus-mt-tc-big-en-pt`

## Project Structure
```text
translator-app/
├── main.py
├── requirements.txt
├── translation_variations.json
└── README.md

## How to Run

1. Clone the repository:
```bash
git clone https://github.com/chasittya/Translator.git
cd Translator

## Install dependencies
pip install -r requirements.txt

## Run application
python main.py


##Example
Input:
How are you?
Target Language:
es
Output:
Hola, ¿cómo estás?

## Results:
The model was evaluated using BLEU scores across five languages.
Spanish, French, and Portuguese achieved higher accuracy due to linguistic similarity to English
Hindi and Arabic showed lower performance due to differences in script and grammar structure
These results highlight the importance of preprocessing and dataset quality in multilingual translation systems.

##Challenges
Handling morphologically rich languages (Arabic, Hindi)
Dataset inconsistencies and alignment issues
High computational cost during model training
BLEU score limitations for semantic accuracy

##Future Improvements
Separate training and inference into modular components
Add a web interface for user interaction
Improve evaluation with metrics like METEOR or BLEURT
Expand support to additional languages
