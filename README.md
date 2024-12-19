# Fake News Detection LIAR Dataset

## Introduction
This project is about detecting fake news using the LIAR dataset. The LIAR dataset is a dataset that contains statements from politicians and their truthfulness. The dataset contains 12.8k labeled statements. The labels are: True, Mostly-True, Half-True, Barely-True, False, and Pants-on-Fire. The dataset also contains metadata about the statements such as the subject, speaker, speaker's job title, state, party, and the context of the statement. The dataset is available at https://www.cs.ucsb.edu/~william/data/liar_dataset.zip

## Plans for us
There are 6 labels, initially we can try binary classsification and develop a simple baseline model with NB.

Even in the literature, 6-way F1 score is ~0.3, which may be discouraging for us. So it is better to start with 


https://aclanthology.org/W18-5513.pdf

https://arxiv.org/pdf/1705.00648v1