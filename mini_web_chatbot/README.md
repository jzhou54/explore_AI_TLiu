# Instruction

## Steps

### 1. Run `mlx_lm.server` 

Run 

```bash
mlx_lm.server --model mlx-community/Meta-Llama-3-8B-Instruct-4bit

```

If you have an adaptor, do this (supposing the adaptor is in the
directory of "lora_adaptor_llama3"):

```bash
mlx_lm.server --adapter-path lora_adaptor_llama3 --model mlx-community/Meta-Llama-3-8B-Instruct-4bit
```

The server will be running and accessible at http://localhost:8080 .
   
### 2. Run the Flask application

Run `python app.py`. The web interface can be  accessible at
http://127.0.0.1:5000/.

### 3. Use the interface

Enter the instruction input and click "Generate". Please note, the
history will be 'memorized' by being reused as input for communicating
with the LLM.

Click the "Reset" button to clear the conversation history. Or click
the "Save" button to download the conversation history as a plain text
file.