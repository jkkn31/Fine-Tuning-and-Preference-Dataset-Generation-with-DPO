# Fine-Tuning LLM and Preference Dataset Generation with DPO

**Author**: Krishnakanth Naik Jarapala  

## Overview

In this project, we will generate a preference dataset using PairRM and fine-tune a model with Direct Preference Optimization (DPO). This training recipe has proven to be effective for some of the top models, as noted in Alpaca Eval. The steps involved include generating a preference dataset, fine-tuning the model, and evaluating the results.

## Steps and Instructions

### 1. Generate a Preference Dataset

**Objective**: Extract the Lima dataset’s instructions, sample 50 instructions, generate 5 responses for each instruction using the `mistralai/Mistral-7B-Instruct-v0.2` model, and create a preference dataset using PairRM.

**Procedure**:
1. **Extract Instructions**:
    - Extract 50 instructions from the Lima dataset.
2. **Generate Responses**:
    - Use the `mistralai/Mistral-7B-Instruct-v0.2` model to generate 5 responses for each instruction.
    - Ensure the appropriate chat template for the `mistralai/Mistral-7B-Instruct-v0.2` model is used.
3. **Create Preference Dataset**:
    - Utilize PairRM to create a preference dataset from the generated responses.
4. **Push to Hugging Face**:
    - Upload the generated dataset to Hugging Face.

**Links**:
- [Hugging Face Dataset](https://huggingface.co/datasets/jkkn/Mistral-7B-Instruct-v2.0-Lima-PairRM-DPO-Dataset)
- [Colab Notebook](https://colab.research.google.com/drive/1fElMWhDq187Ud_9oPQ3vjKtN3CNeGbhs?usp=sharing)

### 2. Fine-Tune the Model with DPO

**Objective**: Fine-tune the `mistralai/Mistral-7B-Instruct-v0.2` model using DPO and evaluate the results with unseen instructions.

**Procedure**:
1. **Fine-Tuning**:
    - Fine-tune the `mistralai/Mistral-7B-Instruct-v0.2` model using DPO.
2. **Evaluation**:
    - Sample 10 instructions not seen during training.
    - Generate completions using both the original model and the DPO fine-tuned model.
    - Compare the results.
3. **Display Results**:
    - Create a pandas DataFrame to display the instruction, original model completion, and DPO fine-tuned model completion.
    - Print the DataFrame to stdout.
4. **Push to Hugging Face**:
    - Upload the PEFT adapter to Hugging Face.

**Links**:
- [Hugging Face Model](https://huggingface.co/jkkn/Mistral-7B-Instruct-DPO-lima-finetuned)
- [Kaggle Notebook](https://www.kaggle.com/code/krishnakanth7/assignment4-dpo-finetuning)

### 3. Bonus: Implement Iterative DPO

**Objective**: Implement Iterative DPO as discussed in the paper “Self Rewarding Language Models”. This combines the idea of LLM-as-a-Judge with DPO trained in an iterative manner.

**Procedure**:
- Implement the algorithm as described in the paper.
- Train the model iteratively with DPO.
- Evaluate the results and document the findings.

## Conclusion

This assignment involved the creation of a preference dataset using PairRM, fine-tuning a model with DPO, and evaluating the performance of the fine-tuned model. The additional challenge was to implement Iterative DPO, which is an advanced technique achieving strong empirical results.

By following the detailed steps and utilizing the provided links, you can replicate the process and verify the results. The use of Hugging Face and Colab/Kaggle notebooks ensures that the models and datasets are accessible and can be reused for further research and development.

---

If you have any questions or need further clarification, please feel free to contact me.

**Krishnakanth Naik Jarapala**  
Email: [jkkn.iitkgp@outlook.com]  
GitHub: [jkkn31]
