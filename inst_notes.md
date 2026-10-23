The format you're asking about is commonly associated with Meta's Llama 2 Chat models and some Mistral-family instruction-tuned models. The exact format depends on the model checkpoint.
*** IMP ***
- [INST] Format is Best understood as a model-specific instruction format.

<!-- ------------------------------ -->

Boilerplate template
"""
For a Llama 2 Chat-style prompt:
<s>[INST] <<SYS>>
You are a helpful AI assistant.
Follow the user's instructions carefully.
<</SYS>>

{user_instruction} [/INST]

Here's an example with an actual instruction:
<s>[INST] <<SYS>>
You are a helpful Python tutor.
Explain concepts in simple terms.
<</SYS>>

Explain what a Python dictionary is. [/INST]
"""

<!-- ------------------------------ -->

- The model generates its answer after [/INST].
- This is the general Llama 2-style structure documented by Hugging Face. 

What does each part mean?
Token or section	             Purpose
<s>	                             Marks the beginning of a sequence.
[INST]	                         Marks the start of a user instruction.
<<SYS>>	                         Introduces the system instructions in this format.
You are a helpful AI assistant.	 Defines the assistant's behavior.
<</SYS>>	                     Marks the end of the system instructions.
{user_instruction}	             The actual question or task.
[/INST]	                         Marks the end of the instruction and the start of the model's response.

For an ongoing conversation, previous user messages and assistant answers must also be included in the model's expected format. The model's response may end with </s>, depending on the conversation structure.