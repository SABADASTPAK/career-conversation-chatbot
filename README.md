# AI Career Assistant Chatbot

An AI-powered career assistant built with Python, Gradio, OpenRouter, and function calling.

This chatbot acts as a digital representation of my professional profile. It can answer questions about my background, skills, education, projects, and work experience by using information extracted from my CV and professional summary.

## Features

* Conversational AI chatbot powered by OpenRouter
* Reads and understands information from a PDF resume
* Uses a professional summary as additional context
* Function calling for lead capture
* Records user contact information
* Records unanswered questions for future improvements
* Sends notifications through Pushover
* Simple Gradio web interface

## Project Structure

```text
.
├── app.py
├── .env
├── requirements.txt
└── me/
    ├── signed_CV_Saba_Dastpak.pdf
    └── summary.txt
```

## Requirements

* Python 3.10+
* OpenRouter API key
* Pushover account (optional but recommended)

## Installation

Clone the repository:

```bash
git clone <your-repository-url>
cd <repository-name>
```

Create and activate a virtual environment:

### Windows

```bash
python -m venv .venv
.venv\Scripts\activate
```


Install dependencies:

```bash
pip install -r requirements.txt
```

## Environment Variables

Create a `.env` file in the project root:

```env
OPENROUTER_API_KEY=your_openrouter_api_key

PUSHOVER_TOKEN=your_pushover_token
PUSHOVER_USER=your_pushover_user
```

## Running the Application

Start the chatbot:

```bash
python app.py
```

After launching, Gradio will provide a local URL similar to:

```text
http://127.0.0.1:7860
```

Open the URL in your browser and begin chatting.

## How It Works

1. The application loads a PDF resume.
2. It loads an additional professional summary.
3. A system prompt is generated using this information.
4. User questions are sent to an LLM through OpenRouter.
5. Function calling is used to:

   * Record contact details from interested visitors.
   * Record unanswered questions.
6. Notifications are delivered through Pushover.

## Technologies Used

* Python
* OpenRouter
* OpenAI SDK
* Gradio
* PyPDF
* Python Dotenv
* Requests


