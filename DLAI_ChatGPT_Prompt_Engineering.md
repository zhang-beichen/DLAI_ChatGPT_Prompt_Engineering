# Notes from ChatGPT Prompt Engineering for Developers

## Introduction

Introducing the general background of natural language process (NLP) with deep learning (DL). 

- Large language models (LLMs) [I think here the term refers to GPT-like LLMs] were categorized into two types.

- Base LLM

- - Predicts the next word based on the training data

- Instruction Tuned LLM

- - - Tries to follow instructions (Fine-tuning based on instructions and making good attempts at following those instructions)
    - RLHF: Reinforcement Learning with Human Feedback ([arXiv paper](https://arxiv.org/abs/2203.02155))

  - Helpful, Honest, Harmless [at least we hope so]

- This short course comes with examples and practices on Jupyter Notebooks. I don't think we can download them. So I organized and kept them in my GitHub repository.

## Guidelines

Introducing two prompting principles and how to write effective prompts.

- **Principle 1:** Write clear and specific instructions

- - As clear and specific as possible.
  - You don't have to write short prompts. In many cases, longer prompts can provide more details to general, more relevant outputs.
  - **Skill 1:** **Use delimiters to clearly indicate distinct parts of the input** (there is no limitation of delimiters, any punctuations that can separate the sentences will work). This can effectively reduce constructive instructions in the prompts.
  - **Skill 2: Ask for structured output** (like HTML, JSON, etc.)
  - **Skill 3: Check whether conditions are satisfied. Check the assumptions required to do the task.** (adding prompts to improve the consistency of outputs)
  - **Few shot prompting**. Give successful examples of completing tasks. Then ask the model to perform the task.

- **Principle 2**: Give the model time to "think."

- - **Skill 1: Specify the steps to complete a task.** [step by step instructing] 
  - **Skill 2: Instruct the model to work out its own solution before rushing to a conclusion.** [ask the model to do step-by-step outputs.]

- **Model Limitations**: Hallucination: make statements that sound plausible but are not true. To address it, the suggestion is to find relevant information and then answer the question based on the relevant information. [However, personally, I think this might be too vague sometimes.]

- **Iterative**: This is originally the third class. However, I think it is more like a trick or concept that can be applied to any use case. In plain language, we can continue updating and refining the prompts/instructions based on the outputs from the model. In the end, we can build prompts to let the model generate outputs closest to our expectations. 

## Applications

- **Summarizing**: summarize text (with multiple objects) with a focus on specific topics. Similarly, you can "**extract**" information (named entity recognition) of multiple objects from the input text.

- **Inferring**: infer sentiment and topics from product reviews and news articles, such as sentiment of the text, what types of emotions are reflected from the text, and extraction of objects ( similar to "extract" above).

- **Transforming**: language transformation tasks, such as language translation, spelling and grammar checking, tone adjustment, and format conversion.

- **Expanding**: generate text based on prompts specifying the requirement.

- **Chatbot**: utilize the chat format to have extended conversations with chatbots personalized or specialized for specific tasks or behaviors.

- - 'system' role (high-level) can send 'content' to set the behavior of the assistant (chat model) to provide answers to the user (you) based on the prompts. System messages provide developers with a way to frame the conversation without making the requests a part of the conversation.

## Conclusion

LLMs are very powerful. Please use them responsibly. Please only build things that will have a positive impact.