# Named Entity Recognition

Named Entity Recognition deals with finding labels for words in a sentence, such as being names or locations. I used HuggingFace models to fine ture NER to labels sentences with the right tags.

# Dataset

I used the WNUT 17 dataset from the Datasets library which has around 6,000 samples. I used around 3,000 for the training data and 1,000 for testing.

# Model Selection

I used the Mistral 7B Instruct Model as the base for this task. Based on the computational resources I have this was a good fit for my use.

# Training

I went for a efficient tuning method by only focusing on the last 4 layers to speed up the process. I used Cross Entropy Loss in order to compare the predicted labels with the true labels. 

# Evaluation

The model had a loss of 1.58 after a short training which was worse than the BERT model which is a better fit for the task. The best results I could get from the BERT model were

| Accuracy  | Precision  | Recall  |  F1-score |
|---|---|---|---|
|  0.947 |  0.542 |  0.392 |  0.455 |  