
## 🎯 Project Overview

**Focus Area:** RAG Applications  
**LinkedIn Trend:** AI-powered personalization  
**Problem Solved:** Knowledge base integration complexity and personalized information retrieval  
**Created:** December 9, 2025

🧠 PersonalKnowledgeRAG

**AI-Powered Personalized Knowledge Assistant**

A cutting-edge application that combines trending LinkedIn topic (AI-powered personalization) with RAG (Retrieval-Augmented Generation) technology to solve knowledge base integration and document processing challenges.

PersonalKnowledgeRAG is a simple demo app that shows how personalization + Retrieval Augmented Generation (RAG) can work together in a real product.

It lets users:

Build a small knowledge base

Create lightweight user profiles

Ask questions

Get answers that change based on the user’s expertise level and preferred response style

The UI is built with Streamlit, the vector store uses ChromaDB, and the logic is intentionally easy to follow so it’s useful as a learning or prototype repo.

Why this project exists

Most RAG demos stop at “retrieve documents and answer questions”.

This app goes one step further:

It remembers who is asking

It adjusts the query and response based on the user

It tracks interactions so personalization can improve over time

This mirrors how real products think about AI assistants, not as a single prompt, but as a system that adapts per user.

Key features
1. Personalized RAG pipeline

Documents are stored in a vector database with metadata

Queries are modified based on the user’s expertise level

Retrieved context is used to generate user-specific answers

2. User profiles

Each user has:

Expertise level, beginner, intermediate, expert

Response style, professional, casual, technical, creative

Interaction count and history

These signals influence both retrieval and response generation.

3. Interaction tracking

Every question and answer is logged with:

User ID

Timestamp

Query

Generated response

This makes it easy to extend the system later with analytics, feedback loops, or learning preferences.

4. Simple Streamlit interface

Sidebar for user profile setup

Main area for asking questions

Stats panel showing usage

Built-in document management

Tech stack

Python

Streamlit for the web UI

ChromaDB as the vector store

Hashlib for document IDs

OpenAI (placeholder, simulated in this demo)

No heavy setup, no external services required to run the basic version.

How the system works

Documents are added to the knowledge base

A user profile is created or updated

The user asks a question

The system:

Adjusts the query based on expertise level

Retrieves relevant documents from ChromaDB

Builds a personalized prompt

Generates a response aligned with the user’s style

The interaction is saved for future use

Running the app locally
1. Install dependencies
pip install streamlit chromadb pandas openai

2. Run the app
streamlit run app.py


Replace app.py with the actual filename if needed.

Sample data

The app ships with three example documents:

AI basics, beginner level

Machine Learning concepts, intermediate

Advanced neural networks, expert

These help you see how the same question changes based on user settings.

Current limitations

This repo is intentionally simple:

OpenAI responses are mocked, not live API calls

No persistent storage, data resets on refresh

No embeddings tuning or reranking

No auth or multi-session isolation

All of this is easy to extend once the core idea is clear.

Obvious extensions if you want to grow this

Plug in real OpenAI or open-source LLM calls

Persist user profiles and documents in a database

Add feedback thumbs up or down per response

Improve retrieval with metadata filters

Add cost tracking and latency metrics

Who this is for

Product managers exploring personalized AI assistants

Engineers learning RAG with personalization

Anyone who wants a concrete, readable example beyond toy chatbots

License

MIT License.
Use it, fork it, break it, improve it.
