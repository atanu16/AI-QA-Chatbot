# 🤖 AI Interview Chatbot

An interactive AI-powered mock interview chatbot built with **Streamlit** and **OpenAI GPT-4o**. It simulates a realistic HR interview experience tailored to the user's background, target role, and company — then provides detailed feedback and a performance score.

---

## ✨ Features

- 🧑‍💼 **Personalized Interviews** — Adapts questions based on your name, experience, skills, level, position, and company
- 🏢 **Multiple Companies & Roles** — Choose from Amazon, Meta, Udemy, Nestle, LinkedIn, Spotify and positions like Data Scientist, ML Engineer, BI Analyst, and more
- 💬 **Real-time AI Responses** — Streamed GPT-4o responses for a natural conversation feel
- 📊 **Automatic Feedback & Scoring** — After 5 responses, get a score (1–10) and detailed feedback on your performance
- 🔄 **Restart Anytime** — One-click interview restart without refreshing the page

---

## 📸 Demo

> Fill in your details → Start Interview → Answer 5 questions → Get Feedback & Score

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| [Streamlit](https://streamlit.io/) | Web UI framework |
| [OpenAI GPT-4o](https://openai.com/) | AI interviewer & feedback engine |
| [streamlit-js-eval](https://github.com/aghasemi/streamlit_js_eval) | JavaScript evaluation for page reload |
| Python 3.10+ | Backend language |

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/ai-interview-chatbot.git
cd ai-interview-chatbot
```

### 2. Install Dependencies

```bash
pip install streamlit openai streamlit-js-eval
```

### 3. Set Up Your OpenAI API Key

Create a `.streamlit/secrets.toml` file in the project root:

```toml
OPENAI_API_KEY = "your-openai-api-key-here"
```

> ⚠️ **Never commit your API key to GitHub!** The `.streamlit/` folder is already in `.gitignore`.

### 4. Run the App

```bash
streamlit run app.py
```

Then open **http://localhost:8501** in your browser.

---

## 📁 Project Structure

```
ai-interview-chatbot/
│
├── app.py                  # Main Streamlit application
├── .streamlit/
│   └── secrets.toml        # API keys (not committed to Git)
├── requirements.txt        # Python dependencies
└── README.md               # You are here
```

---

## 📦 Requirements

Create a `requirements.txt` with:

```
streamlit
openai
streamlit-js-eval
```

---

## 🎯 How It Works

1. **Setup Stage** — Enter your name, experience, and skills. Choose your target level, position, and company.
2. **Interview Stage** — The AI acts as an HR executive and asks relevant interview questions (up to 5 exchanges).
3. **Feedback Stage** — After the interview, click **Get Feedback** to receive a score and detailed performance review.
4. **Restart** — Click **Restart Interview** to begin a fresh session.

---

## ⚙️ Configuration

You can customize the following in `app.py`:

| Variable | Default | Description |
|----------|---------|-------------|
| `openai_model` | `gpt-4o` | OpenAI model used for chat and feedback |
| `user_message_count` limit | `5` | Number of interview exchanges |
| Companies list | Amazon, Meta, etc. | Edit the `selectbox` options |
| Positions list | Data Scientist, etc. | Edit the `selectbox` options |

---

## 🔒 Security Notes

- Add `.streamlit/secrets.toml` to your `.gitignore` before pushing to GitHub
- Never hardcode your API key directly in `app.py`

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🙌 Acknowledgements

- [Streamlit](https://streamlit.io/) for making Python web apps incredibly simple
- [OpenAI](https://openai.com/) for the GPT-4o API
