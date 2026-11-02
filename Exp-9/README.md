# Transformer-Based LLM Chatbot Using Gradio

## EXPERIMENT NO: 9

### Aim
To develop an interactive chatbot using a pre-trained Transformer-based Large Language Model (LLM) and deploy it using Gradio.

### Project Description
This project implements an interactive chatbot using Microsoft's pre-trained DialoGPT-small model. The model is loaded using the Hugging Face Transformers library and PyTorch. Gradio is used to create a user-friendly chat interface that accepts user prompts and generates responses.

### Objectives
- Understand the working of Transformer-based Large Language Models.
- Load and configure a pre-trained LLM.
- Tokenize user prompts using a tokenizer.
- Generate responses using text-generation parameters.
- Maintain conversation history.
- Develop an interactive chatbot using Gradio.
- Test and prepare the chatbot for online deployment.

### Technologies Used
- Python
- PyTorch
- Hugging Face Transformers
- Microsoft DialoGPT-small
- Gradio
- Google Colab
- GitHub
- Hugging Face Spaces

### Model Information
- **Model:** `microsoft/DialoGPT-small`
- **Model Type:** Conversational Language Model
- **Framework:** PyTorch
- **Tokenizer:** Hugging Face AutoTokenizer
- **Interface:** Gradio ChatInterface

### Working Procedure
1. Load the pre-trained DialoGPT-small model.
2. Load the corresponding tokenizer.
3. Convert user prompts into token IDs.
4. Pass the tokenized input to the model.
5. Generate responses using the model's text-generation function.
6. Decode generated tokens into readable text.
7. Maintain previous conversation messages as context.
8. Display responses through the Gradio chat interface.

### Text Generation Parameters

| Parameter | Value | Purpose |
|---|---:|---|
| Temperature | 0.7 | Controls response randomness |
| Maximum new tokens | 80 | Limits generated response length |
| Top-p | 0.9 | Controls nucleus sampling |
| Sampling | True | Enables sampled text generation |

### Testing
The chatbot was tested using the following sample queries:

- Hello!
- What is artificial intelligence?
- What is machine learning?
- What is deep learning?

The chatbot successfully accepted user queries and generated conversational responses.

### Deployment
The application is prepared for deployment using Hugging Face Spaces.

Deployment procedure:
1. Create a new Space on Hugging Face.
2. Select Gradio as the SDK.
3. Upload `app.py` and `requirements.txt`.
4. Allow the application to build.
5. Open the deployed application and test the chatbot.

### Limitations
- The model may generate irrelevant or repetitive responses.
- It may not provide accurate answers to technical questions.
- Response time depends on available computing resources.
- The model has limited conversational context and knowledge compared with larger instruction-tuned LLMs.

### Result
A Transformer-based chatbot was successfully developed using the pre-trained Microsoft DialoGPT-small model. An interactive Gradio interface was created, and the application was prepared for deployment using Hugging Face Spaces.

### Conclusion
This experiment demonstrates how a pre-trained Transformer-based language model can be integrated with a Python application to create an interactive chatbot. It provides practical experience in model loading, tokenization, text generation, conversation history management, interface development, testing, and deployment.
