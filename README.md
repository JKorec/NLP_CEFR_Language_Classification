# CEFR Classification of English Language Sentences

This repository contains the code and data used for an NLP project that classifies English sentences according to CEFR proficiency levels.

The project compares simple linguistic baselines with a BERT-based classifier for two related tasks:

1. **3-class classification:** A, B, C  

2. **6-class classification:** A1, A2, B1, B2, C1, C2

**Authors**

Bruno Cassani, Jan Korec, Colin Norstad, Max Zhang

**Course**

CSCI3349: Natural Language Processing offered by the Boston College Department of Computer Science

## Project Overview

The Common European Framework of Reference for Languages (CEFR) is a standardized system for describing language proficiency. This project explores whether NLP models can automatically classify English sentences by CEFR level and provide the foundation for real-time learner feedback.

The main research goal is to evaluate whether contextual language models such as BERT outperform simpler linguistic baselines like word length, type-token ratio, and parser-based features.

## Repository Structure

├── data/                          # Processed and augmented datasets
├── combined.txt                   # GitHub CEFR sentence dataset
├── cefr_leveled_texts.csv         # Kaggle CEFR paragraph dataset
├── Enhanced Setup.ipynb           # Data preprocessing and train/test splits
├── NLP StatsGen.ipynb             # Dataset statistics
├── NLP Experiments.ipynb          # Initial baseline experiments
├── Experiments Parser.ipynb       # Parser-based baseline
├── BERT_Non_Simplified.ipynb      # BERT on original dataset
├── ExperimentsBert.ipynb          # BERT on simplified dataset
└── NLP_Slide_Deck.pptx            # Final presentation slides

## Data

The project uses two datasets:

* An open-source GitHub dataset based on CEFR-labeled English sentences. The data was obtained from the following [link](https://github.com/yukiar/CEFR-SP). The data has also been copied into this repository.  View: [Combined sentences](combined.txt) 

  
* A Kaggle dataset containing CEFR-labeled English paragraphs. The data was obtained from the following [link](https://www.kaggle.com/datasets/amontgomerie/cefr-levelled-english-texts). The data has also been copied into this repository. View: [CEFR dataset](cefr_leveled_texts.csv)

The datasets were cleaned and combined for model training. The Kaggle data required additional preprocessing because paragraph-level labels do not always apply cleanly to every sentence within the paragraph.

The full dataset with augmented data and training/testing splits can be viewed [here](data)

## Code Overview

[Enhanced Setup](Enhanced%20Setup.ipynb) contains all of the data preprocessing and class partitions.

[NLP StatsGen](NLP%20StatsGen.ipynb) contains code that displays the number of sentences corresponding to each category.

[NLP Experiments](NLP%20Experiments.ipynb) contains the code for the initial baselines.

[Experiments Parser](Experiments%20Parser.ipynb) contains the code for the parser baseline.

[BERT Non Simplified](BERT_Non_Simplified.ipynb) contains the code for the BERT model on the non-simplified dataset.

[Experiments BERT](ExperimentsBert.ipynb) contains the code for the BERT model on the simplified dataset.

Note: If you would like to run this code, please run it in the order that it appears in this section


## External Libraries and Models

This project uses several non-standard NLP libraries:

- Hugging Face Transformers  
  https://huggingface.co/docs/transformers/index

- Hugging Face Datasets  
  https://huggingface.co/docs/datasets/index

- Hugging Face Evaluate  
  https://huggingface.co/docs/evaluate/index

- Benepar (Berkeley Neural Parser)  
  https://github.com/nikitakit/self-attentive-parser

- NLTK  
  https://www.nltk.org/

Additional Python standard libraries used include:
- pickle
- collections

## Model Used

The pretrained transformer model used in this project was:

- distilbert-base-uncased  
  https://huggingface.co/distilbert/distilbert-base-uncased
## Slide Deck

The slide deck that was used to present this project can be viewed [here](NLP_Slide_Deck.pptx). The presentation took place on Tuesday, April 28th, 2026.


## Note
No external notebooks or tutorials beyond official library documentation were used.
