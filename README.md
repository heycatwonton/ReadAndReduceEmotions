# 🧠 Read And Reduce Emotions

## How Algorithms Read and Reduce Emotion: Interrogating Misclassification in Affective Computing

This project examines how modern NLP models recognize and abbreviate emotion. Given the human-annotated GoEmotions dataset, we compare results of a number of classifiers (e.g., Google's GoEmotions model, VADER, TextBlob) on the same richly emotional texts. We aim to find out what emotional signals can be decoded by algorithms, where misclassifications occur, and how models short-circuit complex human affect into discrete categories. By linguistic examination and classification errors, we uncover the affective computing presumptions that get flattened, erased, or blown up. Our research includes a critical perspective, asking: what machines see of our emotions, and what they could possibly overlook? More than model performance, we challenge the emotion as a fixed, classifiable phenomenon. With a six-week timeframe, we will analyze a targeted sample (300–500 cases) to ensure computational and qualitative balance.

- What emotional signals can be decoded by algorithms?
- Where do misclassifications occur?
- How do models short-circuit complex human affect into discrete categories?

By linguistic examination and classification errors, we uncover the affective computing presumptions that get flattened, erased, or blown up. Our research includes a critical perspective, asking: what machines see of our emotions — and what they could possibly overlook?

More than model performance, we challenge the emotion as a fixed, classifiable phenomenon. With a six-week timeframe, we will analyze a targeted sample (300–500 cases) to ensure computational and qualitative balance.


## 🔧 Setup Instructions

This project requires a pre-trained BERT model and the GoEmotions dataset. Some of these files are excluded from version control to keep the repository lightweight. Follow these steps to get everything working locally.

---

### 📦 1. Download the Pre-trained BERT Model

This project uses the [BERT-Base Cased model](https://github.com/google-research/bert#pre-trained-models) from the original BERT release by Google.

**Steps:**

1. Go to: https://github.com/google-research/bert#pre-trained-models
2. Download the `.zip` for the **BERT-Base, Cased** model:    `cased_L-12_H-768_A-12.zip`
3. Unzip the file
4. Place the unzipped contents into this directory: `goemotions/bert/`

After unzipping, the folder should contain the following files:

```
goemotions/bert/cased_L-12_H-768_A-12/
├── bert_config.json
├── vocab.txt
├── bert_model.ckpt.data-00000-of-00001
├── bert_model.ckpt.index
├── bert_model.ckpt.meta
```

> ⚠️ These files are excluded from Git via `.gitignore`. You must download and place them locally.

---

### 📁 2. Project Directory Structure

After setup, your project folder should look like this:

```
ReadAndReduceEmotions/
├── data/
│ └── full_dataset/
│ ├── goemotions_1.csv
│ ├── goemotions_2.csv
│ └── goemotions_3.csv
├── goemotions/
│ └── bert/
│ ├── cased_L-12_H-768_A-12/
│ │ ├── bert_config.json
│ │ ├── vocab.txt
│ │ ├── bert_model.ckpt.data-00000-of-00001
│ │ ├── bert_model.ckpt.index
│ │ └── bert_model.ckpt.meta
│ ├── modeling.py
│ ├── tokenization.py
│ ├── optimization.py
│ └── init.py
├── .gitignore
├── README.md
```

---

### 📦 3. Install Dependencies

Install all required Python libraries:

```bash
pip install -r requirements.txt
```

If a `requirements.txt` file does not exist yet, you can generate one from your current environment:

```bash
pip freeze > requirements.txt
```

---

### 🚫 Files Ignored via `.gitignore`

The following files are excluded from version control:

```
goemotions/bert/cased_L-12_H-768_A-12/
*.ckpt
*.ckpt.*
*.tfrecord
*.h5
data/interim/
data/processed/
```

You must manually download and place these files using the setup instructions above.

---

## ✅ Next Steps

Once setup is complete, you can:

- Fine-tune BERT on the GoEmotions dataset
- Extract BERT `[CLS]` embeddings for analysis
- Compare outputs from VADER, TextBlob, and BERT
- Visualize misclassifications and emotion clustering
- Map raw labels to simplified Ekman emotions

---

## 💡 Contributing Guidelines

- Keep `.gitignore` rules in place to avoid bloating the repo
- Do not commit model checkpoints or large binaries
- Use branches and pull requests for any major changes
- Update this `README.md` if setup or usage changes

---

## 📬 Questions?

If you encounter issues, reach out to the team directly or open an issue in this repository.