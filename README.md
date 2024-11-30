# LangChain for GenAI & NLP

Welcome to my project! This repository showcases my journey and learnings as I explore **LangChain**, **Generative AI**, and **Natural Language Processing (NLP)**. Through this repository, I will share my work on building powerful chains, prompt templates, embeddings, and more, as I continue to delve into the world of modern AI. Follow me as I continue to explore new tools, algorithms, and techniques!

---

## 🚀 Starting My Chain Here

I’m excited to start creating a variety of chains using LangChain, an open-source framework designed to make it easier to work with large language models (LLMs) and connect them with external data sources. Here's what I've learned so far:

### Key Topics I've Explored:
- **Prompt Templates**: Using LangChain’s `ChatPromptTemplate` and other prompt tools to create dynamic, reusable templates for interacting with LLMs.
- **Output Parsers**: Parsing outputs from language models to make them more structured and useful for downstream tasks.
- **Document Loaders**: Efficiently loading and handling external documents for processing with LLMs.
- **Text Splitters**: Breaking text into smaller, manageable chunks using `CharacterTextSplitter` and `RecursiveTextSplitter` to improve processing speed and accuracy.
- **Embeddings**: Integrating embeddings from HuggingFace, Google Generative GenAI, and other sources for powerful document retrieval and search capabilities.

---

## 🔧 Technologies & Tools Used:

- **LangChain**: A framework for developing applications powered by LLMs.
- **HuggingFace Embeddings**: Pre-trained models for converting text into embeddings for document retrieval.
- **Google Generative GenAI**: Leveraging Google's advanced generative models for high-quality text generation and understanding.
- **Text Splitters**: Using advanced text splitting techniques to break down long documents into more digestible chunks.
- **Prompt Templates**: Dynamically creating prompts to interact with LLMs in specific ways.

---

## 📝 Key Features & Learnings

### 1. **Prompt Templates**
- Templates define how the input data is structured and guide the language model's behavior.
- Example: Using a **chat-based prompt** to build a dynamic conversation flow.
  
### 2. **Output Parsers**
- After generating a response, it's important to parse and structure the output.
- Example: Parsing text for specific pieces of information such as names, dates, or key concepts.

### 3. **Document Loaders**
- Load documents from various sources (e.g., PDFs, CSVs) and make them ready for processing by the model.
- Example: Using document loaders to bring in knowledge from multiple sources for retrieval and generation.

### 4. **Text Splitters**
- **CharacterTextSplitter**: Splits large documents into smaller text blocks by a specific number of characters.
- **RecursiveTextSplitter**: Splits documents in a more recursive manner based on semantic boundaries like paragraphs and headings.

### 5. **Embeddings**
- **HuggingFace Embeddings**: Transform text data into vector embeddings for search and retrieval tasks.
- **Google Generative GenAI Embeddings**: Integrating Google's GenAI embeddings to enhance text generation and retrieval capabilities.

---

## 🧑‍💻 Code Snippets & Examples

### Example 1: **Creating a Prompt Template**
```python
from langchain.prompts import ChatPromptTemplate

# Define a simple chat-based prompt template
chat_prompt = ChatPromptTemplate.from_messages([
    ("ai", "You are a helpful assistant. Based on the user's question '{question}', you will provide an answer."),
    ("user", "{question}")
])

formatted_prompt = chat_prompt.format_messages(question="Who is Elon Musk?")
```

### Example 2: **Loading Documents and Embeddings**
```python
from langchain_huggingface.embeddings import HuggingFaceEmbeddings

def embeddings(data):
    if not isinstance(data, str):
        data = str(data)
    embeddings = HuggingFaceEmbeddings()
    vector = embeddings.embed_query(data)
    return vector

# Example data and embeddings
data = "Information about Elon Musk"
result_vectors = embeddings(data)
```

### Example 3: **Using a Text Splitter**
```python
from langchain.text_splitter import CharacterTextSplitter, RecursiveCharacterTextSplitter

# Split a long document into smaller chunks
text = "This is a very long document that needs to be split into smaller chunks."

splitter = CharacterTextSplitter(chunk_size=100, chunk_overlap=20)
chunks = splitter.split_text(text)

print(chunks)
```

---

## 📈 What’s Coming Next

This is just the beginning of my journey with LangChain, and there's much more to explore! Some exciting topics I plan to cover next include:

- **Advanced document retrieval techniques**
- **Building multi-step chains for more complex workflows**
- **Integrating with external APIs for real-time data access**
- **Fine-tuning language models on custom datasets**

---

## 🌟 Follow Me on GitHub!

If you find this project interesting and want to stay updated with my progress, feel free to follow me on GitHub! I’ll be pushing more code, tutorials, and ideas as I continue exploring LangChain and its potential.

👉 [Follow me on GitHub](https://github.com/warishayat)

---

## 🤝 Contribute

If you have any suggestions, ideas, or improvements, feel free to open an issue or create a pull request. Let’s learn together!

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
