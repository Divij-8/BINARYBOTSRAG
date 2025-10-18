AI Vehicle Service Knowledge Assistant

Project Overview
The AI Vehicle Service Knowledge Assistant is an AI-powered tool designed to drastically reduce vehicle diagnostic time by using Retrieval-Augmented Generation (RAG) technology combined with visual and textual data from vehicle service manuals. This system integrates document retrieval with Google's Gemini language models to provide accurate, context-aware answers for vehicle repair and troubleshooting, all with cited manual references and safety instructions.

Features
Visual Diagnostic Mode: Upload photos of dashboard error codes for instant analysis using GPT-4V multimodal capabilities.
Interactive Troubleshooting Tree: Engages users in a stepwise decision-making process for repairs, with dynamic branching and learning from successful fixes.
Time/Cost Estimator: Provides estimated repair times and parts costs to help service advisors deliver accurate quotes.
Manual Citation & Safety Warnings: Every answer cites specific manual sections and highlights safety warnings to ensure reliable guidance.

Technology Stack
Frontend: React with Tailwind CSS for a fast, professional UI.

Backend: Python FastAPI for efficient API development.

Vector Database: Chroma for storing and retrieving document embeddings locally with no external dependencies.

Language Model: Google Gemini models (e.g., gemini-2.0-flash) integrated via API for text generation.

Embeddings: OpenAI text-embedding-3-small for generating vector representations of manual text chunks.

Installation & Setup
Clone the repository:

bash
git clone https://github.com/yourusername/vehicle-service-knowledge-assistant.git
cd vehicle-service-knowledge-assistant
Set up Python virtual environment and install dependencies:

bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
Prepare your vehicle service manuals as PDFs and load them using the provided scripts to generate embeddings and set up the Chroma vector database.

Configure the Gemini API key and run the FastAPI backend.

Start the React frontend and interact with the system.

Complete Retrieval-Augmented Generation (RAG) Pipeline Explanation
1. Data Preparation
Extract text from vehicle service manuals (PDFs).

Split text into coherent chunks (500-800 tokens with overlaps).

Convert text chunks into embeddings using an embedding model (e.g., Gemini embedding).

Store these embeddings with metadata in a vector database like Chroma.

2. Query Processing & Retrieval
Convert user queries (text or visual error code inputs) into embeddings.

Retrieve the top relevant document chunks by comparing query embeddings with stored vectors.

3. Contextual AI Generation
Combine retrieved document chunks with the user query to form an augmented prompt.

Use the Gemini language model to generate precise, context-aware, and cited responses.

Include clear safety information, stepwise repair instructions, estimates for time and cost, and direct citations from the manuals.

4. Continuous Updates
Regularly update the vector database with new manuals or updated data to keep knowledge fresh and accurate.

Usage
Upload dashboard error photos or enter troubleshooting queries via the chat interface.

Receive instant, grounded answers with references to the service manuals.

Follow interactive repair workflows enhanced by AI.



Roadmap & Future Enhancements
Voice command support and multilingual capabilities.

Offline operation mode.

Augmented reality overlays for guided repairs.

Expanded vehicle manual databases.

Acknowledgments
Powered by Google Gemini API embeddings.

Built using Chroma, FastAPI, React, and Tailwind CSS.

Inspired by modern RAG architectures and best industry practices.
