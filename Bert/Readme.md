# Brief Description:

- BERT stands for Bidirectional Representation for Transformers and was suggested by Google AI language researchers in 2018.

- BERT uses the concept of bidirectional context to acquire complex and insightful word and phrase representations.

- Lokking in both the directions of the word helps in better capture of the information.

- This comes in two versions of the pre-trained model BERTBASE and BERTLARGE which are trained on a massive dataset.

- BERT also uses many previous NLP algorithms and architectures such as semi-supervised training, OpenAI transformers, ELMo Embeddings, ULMFit, and Transformers

# Working of BERT

- BERT uses encoder stack of transformer architecture.

- A transformer architecture is an encoder-decoder network that uses self-attention on the encoder side and attention on the decoder side.

- BERT is available in two versions BERT_base(12 layer encoder stack, 768 hidden units, 12 attention heads than transformer, has 110M parameters) and BERT_large (24 layer encoder stack, 1024 hidden units, 16 attention units, 340M paremters)

- The first encoder takes a CLS (Classification token) as an input followed a sequence of words. Each layer applies self attention mechanism and passes the result to feedforward network. The encoder output can be then used for any task such as classification, translation. etc.

![Alt text](<elmo-eemmbeddings-(1).jpg>)

# DataSets

- SQuAD v1.1 Dataset Stanford Question Answer Dataset is a collection of 100k crowdsource Question Answer Pairs. A data point contains a question and a passage from Wikipedia that contains the answer.

- SWAG (Situations With Adversarial Generations) SWAG dataset contains 113k sentence completion tasks that evaluate best-fitting answers using a grounded commonsense inference.

# Setup

### Step-1: Create a Virtual Environment

- Linux: python3 -m venv env
- Windows python -m venv env

### Step-2: Activate the venv

- Linux: source env\bin\activate
- Windows: env\Scripts\activate

### Step-3: Install Required Packages

- pip3 install - r requirements.txt

### Step-4: Start the Jupyter Server

- jupyter notebook

### Debug

#### Upgrade pip if necessary

- Linux: python3 -m pip install --upgrade pip
- Windows: python -m pip install --upgrade pip

#### Install wheel

- Linux: pip3 install wheel
- Windows: pip install wheel

#### Install Build tools (Windows)

# Code Description

- Step - 1: Import necessary packages

- Step - 2: Download the dataset

- Step - 3: Load the dataset & Visualise the number of positive and negative reviews

- Step - 4: Basic Text cleanup using beautifulsoup package and regular expressions

- Step - 5: Apply bert tokenizer which handles
  - CLS token, which is used to represent that the entire sequence is for classification
  - SEP token to indicate boundaries of different sentence
  - MASK to hide some tokens
- BERT tokenizer gives their components as outputs:

  - input_ids: The numerical identifiers of the vocabulary tokens
  - token_type_ids: It identifies which segment or sentence each token belongs to.
  - attention_mask: It flags that inform the model which tokens to pay attention to and which to disregard.

- Step - 6: Load the bert base case model

- Step - 7: Add, adam optimizer, loss metric and compile the model

- Step - 8: Fit the model

- Step - 9: Evaluate the model and plot the classifcation error

- Step - 10: Apply the prediction model and save the model

Ref: https://www.geeksforgeeks.org/explanation-of-bert-model-nlp/
