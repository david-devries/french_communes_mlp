# French Communes MLP

A character-level multilayer perceptron that generates plausible French commune names, built with PyTorch.

Based on the [makemore](https://github.com/karpathy/makemore) series by Andrej Karpathy.

## Dataset

French commune names from [data.gouv.fr](https://www.data.gouv.fr/api/1/datasets/r/f5df602b-3800-44d7-b2df-fa40a0350325). Download `communes-france-2025.csv` and place it in the project root.

## Setup

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## Usage

Open and run `french_villages.ipynb` in Jupyter.

## Model

A simple bigram MLP with learnable character embeddings, one hidden layer (128 units, tanh), and a softmax output layer. The model is trained to predict the next character given a context of previous characters.

Best validation loss: **2.03** (`context_length=8`, `n_embed=64`, `n_hidden=128`) after trying a few configs.

## Sample outputs

Chandans, Etilaiv, Lépantfais, Nouville-en-Payele, Saint-Jroné
