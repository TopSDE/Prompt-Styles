# ChatML Schema: OpenAI's Structured Prompting Style
*** IMP ***
- Best understood as a structured conversation format.


<!-- ------------------------------ -->

messages = [
    {
        "role": "user" | "system" | "assistant",
        "content": "string"
    }
]

*** IMP ***
One important detail: In Python, we typically call this a dictionary. 
In JSON, the equivalent structure is called an object.

So, the same structure is a Python dictionary and a JSON object, 
depending on the format you're talking about.

*** IMP ***
Where are .md files used?
- GitHub: To explain a project in a README.md file.
- Documentation: To write technical guides and tutorials.
- AI projects: To store instructions, notes, and documentation for an LLM project.

.md → the file extension, which stands for Markdown.

<!-- ------------------------------ -->

Boilerplate template
<|im_start|>system
You are a helpful AI assistant.
Follow the user's instructions carefully.
<|im_end|>
<|im_start|>user
{your_question}
<|im_end|>
<|im_start|>assistant

Example:
<|im_start|>system
You are a helpful Python tutor.
Explain concepts in simple terms.
<|im_end|>
<|im_start|>user
Explain a Python dictionary with an example.
<|im_end|>
<|im_start|>assistant

Understanding the tokens
Token	          Purpose
<\|im_start\|>	  Starts a message.
system	          Specifies the role of the message.
user	          Identifies the user message.
assistant	      Identifies the AI's message.
<\|im_end\|>	  Ends a message.


One subtle point: <|im_end|> marks the end of a message, but it doesn't necessarily mean the entire conversation is finished. Some formats use a separate end-of-turn marker, such as <|fim_suffix|>, for that purpose.
Also, when you see system, user, and assistant in the template, those are role names, while the bracketed markers are special tokens in a model's vocabulary.