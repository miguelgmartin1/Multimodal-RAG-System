# Multimodal RAG System for Personalized Restaurant Recommendations

## Overview
This project implements a **Multimodal Retrieval-Augmented Generation (RAG) system** designed for a restaurant aggregator application.  
Its goal is to deliver **highly personalized food recommendations** by combining textual and visual information from restaurant menus, taking into account user preferences, dietary restrictions, and nutritional needs.

By leveraging multimodal embeddings, vector similarity search, and large language models, the system enables **context-aware, accurate, and explainable recommendations** through an interactive user interface.

---

## Problem Statement
Traditional recommendation systems often rely solely on structured or textual data, limiting their ability to fully understand food items and user preferences.

This project addresses that limitation by:
- Combining **textual menu data** and **food images**
- Encoding both modalities into vector representations
- Using a RAG pipeline to generate natural-language recommendations grounded in retrieved evidence

---

## Solution Architecture
The system follows a modular, cloud-based architecture:

1. **Data Storage**
   - Menu metadata stored as structured CSV files
   - Food images stored in Amazon S3

2. **Multimodal Processing**
   - Image summarization and understanding via Amazon Bedrock multimodal models
   - Text and image embeddings generated using AWS Titan Embeddings

3. **Vector Search**
   - Embeddings indexed using FAISS for fast and scalable similarity search

4. **Retrieval-Augmented Generation**
   - Relevant menu items retrieved based on user queries
   - Context injected into an LLM to generate grounded, personalized responses

5. **User Interface**
   - Streamlit-based UI for interactive querying and real-time recommendations

---

## Data Description
The dataset consists of:

- **CSV file** containing:
  - Menu item ID
  - Item name
  - Restaurant and cuisine type
  - Nutritional values
  - Dietary warnings (allergens, intolerances)
  - Vegetarian status
  - Ratings
  - Serving size
  - Price
  - Image path reference

- **Image folder**
  - One image per menu item
  - Used to enrich recommendations through visual understanding

This multimodal setup allows the system to reason beyond text-only descriptions.

---

## Tech Stack

### Language
- Python 3.10.4

### Libraries & Frameworks
- boto3
- awscli
- pandas
- langchain
- langchain-community
- faiss-cpu
- streamlit
- streamlit-chat

### Models
- Claude Sonnet (Multimodal)
- AWS Titan Embeddings (via Amazon Bedrock)

### Cloud Platform
- Amazon Web Services (AWS)

---

## Key Features
- Multimodal retrieval combining text and images
- Semantic similarity search with FAISS
- Retrieval-Augmented Generation for grounded responses
- Cloud-native architecture using AWS services
- Interactive and user-friendly Streamlit interface
- Designed for scalability and extensibility

---

## How to Run the Project

1. Clone the repository
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
