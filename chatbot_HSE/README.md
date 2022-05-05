<h1 align="center">Chatbot for MIEM HSE</h1>

## Description
Aim of this project is to develop model that will be able to answer student's questions. Approach presented here is to use sentence embeddings from pretrained BERT models and calculate cosine distance between input question and those we have in [sample](https://github.com/SergeyMaslikhov/DS_projects/blob/main/chatbot_HSE/data/augmented_sample.xlsx). Answer that corresponds to question with max value of cosine distance is given as output.
## Brief overview for each notebook
- [forming_train_sample.ipynb](https://github.com/SergeyMaslikhov/DS_projects/blob/main/chatbot_HSE/forming_train_sample.ipynb) - algorithm to generate training sample that labels cosine distance between two questions (for now it's 0 or 1).
- [sentence_transformer_train.ipynb](https://github.com/SergeyMaslikhov/DS_projects/blob/main/chatbot_HSE/sentence_transformer_train.ipynb) - notebook that implements training models with generated training sample.
- [Test_review.ipynb](https://github.com/SergeyMaslikhov/DS_projects/blob/main/chatbot_HSE/Test_review.ipynb) - comparing pretrained models, trained on new data and ensemble of several models to each other using [testing.xlsx](https://github.com/SergeyMaslikhov/DS_projects/blob/main/chatbot_HSE/data/testing.xlsx)
- [final_model.ipynb](https://github.com/SergeyMaslikhov/DS_projects/blob/main/chatbot_HSE/final_model.ipynb) - implementation of ensemble model that appears to be the best solution

## Requirements
To install necessary packages use:
```shell
pip install -r requirements.txt
```
