# 🤖 Q&A Bot using Groq API and Python

A simple and fast Question & Answer chatbot built using **Python** and the **Groq API**. This project allows users to ask questions in natural language and receive AI-generated responses powered by Groq's high-performance language models.

---

## 🚀 Features

* Ask questions in natural language
* Fast AI-generated responses using Groq
* Simple command-line interface
* Easy to customise and extend
* Beginner-friendly Python project
* Secure API key management using environment variables

---

## 🛠️ Tech Stack

* Python 3.x
* Groq API
* dotenv
* Requests / Groq SDK

---

## 📂 Project Structure

```text
QnA-Bot/
│
├── main.py
├── .env
├── requirements.txt
├── README.md
└── screenshots/
    └── demo.png
```

---

## 📦 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/QnA-Bot.git
cd QnA-Bot
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it:

**Windows**

```bash
venv\Scripts\activate
```

**Mac/Linux**

```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 Setting Up the Groq API Key

Create a `.env` file in the project root directory.

```env
GROQ_API_KEY=your_api_key_here
```

Replace `your_api_key_here` with your actual Groq API key.

---

## ▶️ Running the Bot

```bash
python main.py
```

Example:

```text
You: What is Artificial Intelligence?

Bot: Artificial Intelligence (AI) refers to the simulation of human intelligence in machines that are programmed to think, learn, and solve problems.
```

---

## 💻 Sample Code

```python
from groq import Groq
import os
from dotenv import load_dotenv

load_dotenv()

client = Groq(
    api_key=os.getenv("GROQ_API_KEY")
)

while True:
    question = input("You: ")

    if question.lower() == "exit":
        break

    response = client.chat.completions.create(
        messages=[
            {
                "role": "user",
                "content": question
            }
        ],
        model="llama-3.3-70b-versatile"
    )

    print("Bot:", response.choices[0].message.content)
```

---

## 📸 Demo

Add a screenshot of your chatbot inside the `screenshots` folder and update this section.

```markdown
![Demo](screenshots/demo.png)
```

---

## 🔮 Future Improvements

* Streamlit Web Interface
* Chat History Storage
* Voice Input Support
* Multi-language Support
* PDF Question Answering
* Document-Based Chatbot (RAG)
* User Authentication

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a new branch
3. Make your changes
4. Submit a Pull Request

---

## 📜 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Jasmeen Kaur**

Aspiring AI Developer | Student | Builder

If you found this project useful, consider giving it a ⭐ on GitHub.
