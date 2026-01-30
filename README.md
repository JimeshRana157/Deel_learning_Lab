
# Fake Reviews Analysis — Notebook

This repository contains a Jupyter notebook `202511061_lab01.ipynb` that demonstrates preprocessing, product category classification, and fake review detection using a GRU-based PyTorch model and spaCy tokenization.

**Repository layout**
- **`202511061_lab01.ipynb`**: Main notebook implementing preprocessing, two classification tasks, and a wordcloud visualization.
- **`fake_reviews_dataset.csv`**: Expected dataset (place in the same folder as the notebook).

**Key Tasks Implemented**
- **Product Category Classification**: Multi-class classification using a GRU model over tokenized reviews.
- **Fake Review Detection**: Binary classification (fake vs genuine) using a similar GRU architecture.
- **Wordcloud**: Visualizes influential words from reviews labeled as fake.

**Environment & Dependencies**
The notebook installs and uses the following packages (see the first notebook cell):

```
spacy
torch (torchvision, torchaudio)
scikit-learn
pandas
numpy
matplotlib
wordcloud
```

You can install these directly (from the notebook or command line):

```powershell
pip install -q spacy torch torchvision torchaudio scikit-learn pandas numpy matplotlib wordcloud
python -m spacy download en_core_web_sm
```

Note: If running the notebook cells in Jupyter, the notebook uses `!pip` at the top cell; in a terminal use the commands above.

**Dataset**
- The notebook expects a CSV named `fake_reviews_dataset.csv` in the same directory. The notebook uses the columns `text_`, `category`, and `label` (where `label` distinguishes fake/genuine).
- If your dataset has different column names, update the notebook cell that reads the CSV and the column references.

**How to run**
1. Open the folder in Jupyter / VS Code.
2. Ensure the dataset `fake_reviews_dataset.csv` is present in the same folder as `202511061_lab01.ipynb`.
3. Start the notebook server and run the cells in order. The first cell installs packages and downloads spaCy models (it may take several minutes).

From PowerShell (optional):

```powershell
jupyter notebook "c:\Users\jimes\Desktop\collge\Sem-2 subject\IT549-Deep Learning-Arpit Rana\Lab\202511061_lab01.ipynb"
```

**What to expect**
- Tokenization and vocabulary creation using spaCy (lemmatization, stopword removal).
- Training of two GRU-based classifiers (category and fake/genuine) for a few epochs.
- Printed classification reports for test splits and a wordcloud image for fake reviews.

**Possible improvements / next steps**
- Create a `requirements.txt` or `environment.yml` for reproducible environments.
- Save trained model weights and add evaluation scripts to load and test saved models.
- Add padding/truncation controls, learning rate schedules, or experiment with transformer embeddings.

**License & Contact**
- This is course/lab code for personal/educational use. Modify and adapt as needed for your assignments.
- For questions, open the notebook or contact the notebook author (local file owner).
