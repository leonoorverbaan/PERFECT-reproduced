# Reproducibility Project
## PERFECT: Prompt-free and Efficient Few-shot Learning with Language Models

### Authors: Tim Rood, Leonoor Verbaan, Mustafa Wahid

### Summary
**PERFECT** is an approach to few-shot learning that doesn't require manual prompts or task-specific instructions. Instead, it uses the power of large pre-trained language models such as GPT-3 to learn new tasks from just a few examples. So PERFECT works by fine-tuning a **pre-trained language model** on **a small amount of labeled data** from a new task. The key innovation is to use a meta-learning algorithm that optimizes the fine-tuning process across multiple tasks, allowing the model to quickly adapt to new tasks with minimal training data.

![PERFECT figure](https://images.deepai.org/converted-papers/2204.01172/x3.png)

The algorithm works by first e**ncoding a support set of examples into a representation that can be fed into the language model.** This representation is then used to generate a set of synthetic examples by conditioning the language model on a few-shot learning task description. The synthetic examples are used along with the support set to train a classifier.

During testing, the algorithm generates a set of **synthetic examples** for the test query, and these synthetic examples are used to make predictions. This approach has several advantages over traditional few-shot learning approaches. First, it is prompt-free, meaning that it does not require explicit instructions or prompts to be provided to the model. Second, it is highly efficient, as it leverages the pre-trained language model's ability to quickly generate synthetic examples.

**paper** : ![PERFECT: Prompt-free and Efficient Few-shot Learning with Language Models](https://aclanthology.org/2022.acl-long.254.pdf "PERFECT: Prompt-free and Efficient Few-shot Learning with Language Models")

### Dataset
**Small dataset** : Reddit corpus (https://huggingface.co/datasets/USC-MOLA-Lab/MFRC "Dataset")

**Bigger dataset**: Twitter dataset (https://github.com/adondera/transferability-of-values/tree/master/nlp/data)

### Reproducibility plan
The following presents a general approach on reproducing the results from PERFECT: Prompt-free and Efficient Few-shot Learning with Language Models. 

- Use one of the original datasets to reproduce the results in the paper using average/worst-case accuracy/standard deviation (table 1) 

- Different (smaller, reddit corpus) dataset and comparison of the original results using average/worst-case accuracy/standard deviation (table 1).

- Different (bigger, Twitter dataset) dataset and comparison of the original results using average/worst-case accuracy/standard deviation (table 1).

**Further reproduction results** : Testing performance on label variety or research on the minimum amount of shots in few-shot learning on a morale-based Reddit classification task
