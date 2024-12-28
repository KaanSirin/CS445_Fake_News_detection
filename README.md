# Fake News Detection LIAR Dataset

## Introduction
This project is about detecting fake news using the LIAR dataset. The LIAR dataset is a dataset that contains statements from politicians and their truthfulness. The dataset contains 12.8k labeled statements. The labels are: True, Mostly-True, Half-True, Barely-True, False, and Pants-on-Fire. The dataset also contains metadata about the statements such as the subject, speaker, speaker's job title, state, party, and the context of the statement. The dataset is available at https://www.cs.ucsb.edu/~william/data/liar_dataset.zip

## Plans for us
There are 6 labels, initially we can try binary classsification and develop a simple baseline model with NB.

Even in the literature, 6-way F1 score is ~0.3, which may be discouraging for us. So it is better to start with 

This follows what we want to do very closely, Table 2 shows classification performances off different approaches including LR, SVM, BiLSTM for binary and 6-way classification:

1. https://aclanthology.org/W18-5513.pdf

This is the original paper, Table 2 shows the results for using metadata on top of the text in hybrid CNN models:

2. https://arxiv.org/pdf/1705.00648v1

Following these would be a good start. We may want look at other papers as well that are nor LIAR specific in the future.

This is an example that uses BERT and RoBERTa models on LIAR fake news detection

3. https://github.com/SindhuMadi/FakeNewsDetection/blob/main/BERT_ROBERT_V1_2Epochs_32batch.ipynb
   
==Modern BERT, this came out on 19.12.2024 ***5 days ago*** modernizing the BERT (2018) with current architecture and scaling== it would be nice if we could incorporate it

**4. https://huggingface.co/blog/modernbert**

Fine tuning Modern Bert for classification task, blog

5. https://www.philschmid.de/fine-tune-modern-bert-in-2025

## Weirdness
For binary classification done in the first paper (from EMNLP) we achieve the same performance with no meta-data, just statement tf-idf vectorized
- Acc:	0.613
- F1:	0.696

6-way classification result is much more realistic, this could be our baseline

- Acc:	0.199
- F1:	0.184

I think we should mainly focus on 6-way, as the binary one is trivial, we can follow the 2nd paper which is the original dataset, and use metadata in the baseline model to see performance improvements
