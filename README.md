# Embedify

## Overview
Embedify is a powerful toolkit for creating self-supervised word embeddings using cutting-edge techniques such as Word2Vec and FastText. This project empowers you to harness the latent semantic meaning within words, providing a foundation for natural language understanding in various applications.

Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------


## Features
- **Word2Vec and FastText Integration:** Choose between two leading algorithms for word embedding generation.
- **Self-Supervised Learning:** Train embeddings without the need for labeled data, allowing for versatility across domains.
- **Customizable Parameters:** Fine-tune hyperparameters to tailor embeddings to your specific use case.
- **Scalability:** Efficiently process large datasets, ensuring scalability for diverse applications.

## Getting Started
1. **Clone the Repository:**
   ```
   git clone https://github.com/smn06/Embedify.git
   cd Embedify
   ```

2. **Install Dependencies:**
   ```
   pip install -r requirements.txt
   ```

3. **Configure Settings:**
   Adjust configuration parameters in `config.yaml` to suit your requirements.

4. **Training:**
   ```
   python train.py
   ```

5. **Evaluate Embeddings:**
   Explore the trained embeddings using provided examples in the `notebooks` directory.

## Example Usage
```python
from embedify import WordEmbeddings

# Load pre-trained embeddings
embeddings_model = WordEmbeddings.load_model("path/to/your/embeddings.model")

# Get the embedding vector for a word
vector = embeddings_model.get_embedding("example")

# Find similar words
similar_words = embeddings_model.most_similar("example_word", topn=5)
print(similar_words)
```


## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

