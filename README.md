# LLMs Post Training
This repo includes the implementation of LLMs' Post-training approaches with TRL library provided by HuggingFace.

What is Post-training?
Post-training of LLMs refers to the stage after a base model has already been pre-trained on large amounts of general data, where the model is further trained to perform more specific tasks, such as answering questions, following instructions, or behaving safely and helpfully for a particular application.

Post-training of LLMs allows us to enable the model to learn responses from curated data. This phase usually uses much smaller datasets, which will be much faster and cheaper.

## Post-training Methods

### Supervised Fine-Tuning (SFT) ![Post-training](https://img.shields.io/badge/post-training-green)

SFT stands for Supervised Fine-Tuning (Imitating example responses) trains a model on labelled prompt-response pairs. This method is effective for introducing new behaviours and making major changes to the model. It is a way to make AI models smarter and more helpful by training them on high-quality examples.

**Best Use case for SFT**

You can use SFT when you want to:

1. **Turn a general AI into a specific type of model**
   - **Instruct models:** Follow instructions better.
   - **Reasoning models:** Solve problems step by step.
   - **Non-reasoning models:** Generate text without complex reasoning.

2. **Teach the model to use tools**
   - The model can use tools or follow processes without you explaining everything in the prompt.

3. **Make smaller models smarter**
   - Train small models on data created by larger, stronger models.
   - This helps smaller models perform better without needing huge amounts of data.



**How to Prepare Data for SFT**

Good data is the key to making SFT work. Here are some common methods:

1. **Generate responses from strong models**
   - Use a powerful AI to create good answers, then train your model on them.

2. **Best-of-K selection**
   - Make the AI generate several answers.
   - Pick the best one for training.

3. **Filtering**
   - Start with a large set of examples.
   - Remove low-quality or repetitive answers to keep only the best.



**Quality vs. Quantity**

- High-quality data matters more than lots of data.
- A smaller set of 100,000 high-quality, diverse examples is better than a million low-quality examples.
- Sometimes, a mix of high and medium-quality data works if chosen carefully.


### Direct Preference Optimisation (DPO) ![Post-training](https://img.shields.io/badge/post-training-green)
Coming Soon :)

### Online Reinforcement Learning (Online RL) ![Post-training](https://img.shields.io/badge/post-training-green)
Coming Soon :)
