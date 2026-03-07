# Mental-Health-Support-Chatbot
Empathetic Mental Wellness Chatbot

This project builds an AI-powered empathetic chatbot that provides supportive responses for people experiencing stress, anxiety, or emotional challenges.

The chatbot is fine-tuned using a Large Language Model (DistilGPT2) on the EmpatheticDialogues dataset from Facebook AI to generate emotionally supportive and understanding responses.

The system demonstrates LLM fine-tuning using Hugging Face Trainer API and conversational AI techniques.

Features

AI chatbot trained on real empathetic human conversations

Generates emotion-aware and supportive responses

Uses DistilGPT2 fine-tuned for emotional dialogue

Built with Hugging Face Transformers

Trainer API for efficient LLM fine-tuning

Supports text generation for emotional wellness conversations

Command-line chatbot interface for interactive testing

Technologies Used

Python

Hugging Face Transformers

Hugging Face Datasets

PyTorch

DistilGPT2 (Pretrained LLM)

Kaggle GPU for model training

Dataset

The model is trained on the EmpatheticDialogues dataset created by Facebook AI Research.

The dataset contains human-to-human conversations where one person shares an emotional experience and the other responds empathetically.

Dataset fields include:

Situation – background emotional scenario

Emotion – emotional label

Customer message – user emotional statement

Agent response – empathetic reply

Example training sample:

Customer: I feel really anxious about my exams.
Emotion: anxious
Agent: I'm sorry you're feeling stressed. Exams can be overwhelming, but you're doing your best.

Model Training

The chatbot is created by fine-tuning DistilGPT2 using Hugging Face's Trainer API.

Training pipeline:

Load the Empathetic Dialogues dataset

Clean unnecessary columns

Format conversations into chatbot dialogue format

Tokenize text using DistilGPT2 tokenizer

Train the model using causal language modeling

Save the trained model

Generate empathetic responses using a text-generation pipeline

Training configuration:

Model: DistilGPT2

Epochs: 3

Batch size: 8

Learning rate: 5e-5

Training samples: ~64k dialogues

GPU acceleration used (Kaggle GPU)

Example Chat

User Input

Customer: I feel really anxious about my exams.

Chatbot Response

Agent: I'm sorry you're feeling this way. Exams can be stressful, but remember that you have prepared and you can do your best.

Installation

Clone the repository:

git clone <your-repository-url>
cd empathetic-chatbot

Install required dependencies:

pip install transformers datasets accelerate evaluate torch
Training the Model

Run the training script:

python train_chatbot.py

The model will be trained using the Empathetic Dialogues dataset and saved locally.

Running the Chatbot

After training, start the chatbot interface:

python chatbot.py

Example interaction:

You: I feel lonely today
Bot: I'm really sorry you're feeling lonely. Sometimes talking to someone you trust can really help.

Type quit to exit the chat.

Project Structure
empathetic-chatbot
│
├── dataset
│
├── train_chatbot.py
│
├── chatbot.py
│
├── requirements.txt
│
└── README.md
Skills Demonstrated

This project demonstrates practical experience in:

Large Language Model fine-tuning

Conversational AI development

Natural Language Processing (NLP)

Emotional dialogue modeling

Hugging Face Transformers ecosystem

GPU-based model training

Future Improvements

Deploy chatbot using Streamlit web interface

Fine-tune larger models like Mistral 7B

Add emotion detection before response generation

Implement conversation memory for multi-turn dialogue

Deploy chatbot using Hugging Face Spaces
