# Sentence_Simplification
Sentence Simplification Model using BART, extension includes pre-processing Bi-LSTM lexical simplification model to find and substitute complex words for simple words, as well as using length and paraphrasing control token for final output

The baseline could be run by clicking through "Runtime -> Run all". The requred packages will be first installed and the imported. The pre-defined data preprocessing will clean, sample, and save the data. The number of samples used for training, development, and test data can be adjusted by changing the number of variables **train_size**, **dev_size**, and **test_size**. In addition, for the CWI model, there is a list of POS tags. The model will only replace the words that fall in the POS categories in the list. The list could be found in **class CWI** --> **def \_\_init\_\_** --> **self.POS_TAG**. For a quick fine-tuning, no hyperparameter is needed and by default, for example, the batch size is 8 and number of epoch is 3. With Tesla P100 GPU on Google Colab Pro, it could take up to 10 hours to complete the fine-tuning. 

Evaluation is based on SARI score for a set of human simplified sentences
