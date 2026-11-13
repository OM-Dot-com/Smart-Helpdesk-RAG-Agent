# Smart Helpdesk RAG Agent with n8n

An AI-powered college helpdesk chatbot built using **n8n, Google Gemini, Retrieval-Augmented Generation (RAG), Google Sheets, and Discord**.

## Project Overview

The Smart Helpdesk RAG Agent is an automated chatbot designed for a fictional college called **Sunrise College**.

Students can ask questions about:
- College fee structure
- Examination rules
- Hostel rules
- General college-related queries
- Complaints and support requests

The chatbot retrieves information from uploaded college documents and generates answers using Google Gemini. It uses RAG (Retrieval-Augmented Generation) to answer based on the available documents rather than simply guessing.

## Key Features

- **AI-powered chatbot:** Uses Google Gemini to respond to student queries.
- **Document-based answers:** Retrieves information from uploaded documents using a vector store.
- **Conversation memory:** Supports follow-up questions using Simple Memory.
- **Smart routing:** Routes greetings, complaints and questions.
- **Google Sheets integration:** Automatically logs conversations.
- **Discord alerts:** Notifies a human when the chatbot cannot answer or receives a complaint.
- **Error handling:** Sends alerts when a workflow execution fails.

## System Architecture

The project consists of four interconnected n8n workflows:

| Workflow | Description |
|---|---|
| A - Load Knowledge Base | Uploads documents, splits text into chunks and stores embeddings in a vector store. |
| B - Helpdesk Chatbot | Handles student messages, routes queries and generates AI responses. |
| C - Log Chat to Sheet | Saves conversation details in Google Sheets. |
| D - Error Alert | Handles workflow errors and sends notifications. |

## Technologies Used

- n8n – Workflow automation
- Google Gemini – AI language model
- Gemini Embeddings – Text embeddings
- Simple Vector Store – Document retrieval
- Google Sheets – Conversation logging
- Discord Webhook – Notifications
- RAG – Retrieval-Augmented Generation

## How RAG Works

1. Upload college documents.
2. Split the documents into smaller text chunks.
3. Convert the chunks into vector embeddings.
4. Store the embeddings in a vector store.
5. Retrieve relevant information when a student asks a question.
6. Generate an answer using Google Gemini.

## Project Files

```text
Smart-Helpdesk-RAG-Agent/
│
├── A - Load Knowledge Base.json
├── B - Helpdesk Chatbot.json
├── C - Log Chat to Sheet.json
├── D - Error Alert.json
│
├── A-Load-Knowledge-Base Workflow.png
├── B-Helpdesk-Chatbot Workflow.png
├── C-Log-Chat-to-Sheet Workflow.png
├── D-Error-Alert Workflow.png
│
├── Helpdesk Chat Log.docx
├── OmChaurasia_Writeup.pdf
└── README.md
```

## Setup Instructions

1. Create an account on n8n.
2. Import the four workflow JSON files.
3. Configure your Google Gemini credentials.
4. Connect your Google Sheets account.
5. Configure your Discord webhook URL.
6. Upload the college knowledge-base documents.
7. Publish and test the chatbot workflow.

**Note:** Credentials, document IDs and webhook URLs must be configured with your own accounts before running the workflows.

## Project Documentation

- Project write-up: `OmChaurasia_Writeup.pdf`
- Workflow diagrams: PNG files included in this repository.
- Chat log documentation: `Helpdesk Chat Log.docx`

## Demo Video

**Google Drive Demo:** [Add your Google Drive video folder link here]

## Learning Outcomes

Through this project, I learned:

- How to build AI-powered automation workflows using n8n.
- How RAG works with document retrieval and vector embeddings.
- How to integrate Google Gemini with automation workflows.
- How to connect Google Sheets and Discord using APIs.
- How to implement workflow routing, memory and error handling.

## Author

**Om Rajesh Chaurasia**  
Shree L.R. Tiwari College of Engineering  
Roll No: 07

---

*Developed as part of the edQuest Internship Project.*
