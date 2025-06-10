
#  Stock Market 2024 RAG Chatbot

This is an AI chatbot that answers your questions about stock market performance in 2024.  
It reads a PDF document, breaks it into pieces, stores the data smartly, and uses a powerful LLM to give you accurate, document-based answers.

---

##  System Overview

- **PDF Reader**: Loads and reads the "Stock_Market_Performance_2024.pdf" file.
- **Text Splitter**: Breaks the PDF into small, searchable chunks.
- **Vector Store (ChromaDB)**: Saves those chunks in a way the AI can understand.
- **Retriever**: Finds the most relevant chunks based on your question.
- **LLM (GPT-4o)**: Generates answers using both its intelligence and the PDF data.
- **LangGraph Agent**: Controls the flow — loops through LLM and tool until the best answer is ready.

---

## ⚙️ Setup Instructions

1. **Clone the repo**  
   git clone https://github.com/ZainAli879/Rag_Agent.git
   
   cd your-repo

3. **Place your PDF**
   Make sure the file `Stock_Market_Performance_2024.pdf` is in the root folder.

4. **Create a `.env` file**
   Add your OpenAI API key:

   ```env
   OPENAI_API_KEY=your_openai_key_here
   ```

5. **Install dependencies**
   Run:

   ```bash
   pip install -r requirements.txt
   ```

6. **Run the bot**

   ```bash
   python Rag_Agent.py
   ```

---

## 💬 Usage Example

```bash
What is your question: What was the best performing sector in 2024?
```

Bot will respond by reading the document and pulling out the exact data you need.

---

## 🧰 Tech Stack

* Python 🐍
* LangChain + LangGraph
* GPT-4o (via OpenAI)
* Chroma for vector storage
* HuggingFace Embeddings
* PDF Parsing with PyPDF

---

## 🚪 Exit

To exit the chatbot, simply type:

```bash
exit
```

---

## 📂 Folder Structure

```
.
├── chroma_db/                 # Stores the document embeddings
├── Stock_Market_Performance_2024.pdf  # Your data source
├── .env
├── requirements.txt
└── Rag_Agent.py        # Main script
```

---

## 📝 Notes

* If the Chroma DB already exists, it won't rebuild it.
* You can add more tools later to make it smarter.
* Works locally without internet once the embeddings are built.

---

## Final Thoughts

This chatbot is a smart document reader — ask anything related to stock market performance in 2024, and it’ll pull the answers straight from the PDF for you.

Enjoy the insights! 📈
