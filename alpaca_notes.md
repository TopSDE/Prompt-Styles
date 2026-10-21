*** IMP ***
- Best understood as a simple instruction-tuning template.
- You prepare thousands of instruction-and-answer examples to fine-tune a model to explain programming concepts.

<!-- ------------------------------ -->

#### With Input
    Below is an instruction that describes a task, 
    paired with an input that provides further context. 
    Write a response that appropriately completes the request.

    ### Instruction:
    {instruction text}

    ### Input:
    {optional input text}

    ### Response:
    ```

#### Without Input (No-Input Variant):
    ```text
    Below is an instruction that describes a task. 
    Write a response that appropriately completes the request.

    ### Instruction:
    {instruction text}

    ### Response:
    ```

<!-- ------------------------------ -->

### Key Components

* **Instruction:** A clear sentence or command describing what the model needs to do (e.g., *"Summarize the following text"* or *"Write a poem"*).
* **Input:** Supplementary data or context needed to complete the instruction (optional; omitted if the task is self-contained).
* **Response:** The targeted output for training, or the stopping point where the model begins generating its answer during inference.

<!-- ------------------------------ -->

### Why It Matters

* **Task Boundaries:** The `###` delimiters prevent the model from confusing instructions with context or output data.
* **Consistency:** Standardizing data format across thousands of training examples helps models generalize better across diverse tasks.
* **Open-Source Standard:** Introduced via the [Stanford Alpaca GitHub Repository](https://github.com/tatsu-lab/stanford_alpaca), it became a baseline formatting standard for instruction tuning across many local LLM ecosystems and tools like `llama.cpp`.

<FollowUp>
Are you looking to **format training data in JSONL**, or do you need help **writing a custom prompt** for a specific local model?
</FollowUp>
