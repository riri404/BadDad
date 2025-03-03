# BadDad
Extract and categorize abusive or neglectful language from text, screenshots, and voice notes. Summarize and organize evidence for legal presentation. 

## Steps
1. Transcribes Voice Notes (Speech-to-Text)
2. Processes Text Messages (OCR if needed)
3. Categorizes Information (Emotional tone, abuse, threats, manipulation, etc.)
4. Retrieves Data Efficiently (Search and filter system)
5. Summarizes Content (Key highlights of conversations)


## Tech Stack
### Core Libraries & Tools
- Programming Language: Python
- Speech-to-Text (STT):
  - Whisper (OpenAI) Best for informal Arabic transcription.
  - VOSK (Offline alternative)
  - Google Speech-to-Text (if online is acceptable)
- Natural Language Processing (NLP):
  - transformers (Hugging Face) Arabic models
  - nltk and spacy  Text processing
  - farasa Arabic-specific NLP
- Machine Learning Frameworks:
  - PyTorch or TensorFlow If fine-tuning models
- Database & Retrieval:
  - FAISS Fast search index for text retrieval
  - SQLite or MongoDB Storing categorized data

## Pipeline & Workflow Management:
Airflow or Prefect – To automate and schedule processing tasks
Development Pipeline
Preprocessing Module

Convert voice notes to text (STT)
Normalize informal Arabic (Remove diacritics, expand slang)
Clean text (Remove unnecessary symbols, filler words)
Text Categorization Module

Use NLP to classify messages (e.g., insults, threats, neglect)
Sentiment analysis (Positive, Neutral, Negative)
Named Entity Recognition (NER) (Identify important details like dates, people)
Search & Retrieval Module

Store extracted texts in a vector database (FAISS or Elasticsearch)
Implement keyword-based and semantic search
Summarization Module

Extract key points from long conversations
Use GPT-based or BART models for summarization
User Interface (Optional)

Build a simple Streamlit or Flask web app for interaction
