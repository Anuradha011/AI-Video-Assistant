# 🎬 AI Video Assistant

### Transform Long Videos into Searchable, Actionable Knowledge

AI Video Assistant is an AI-powered application that transforms video and audio recordings into meaningful insights. It helps users transcribe content, generate concise summaries, extract action items, identify key decisions, and ask questions about recordings through an intelligent chat interface.

Whether you're reviewing meetings, studying lectures, analyzing interviews, or exploring YouTube videos, AI Video Assistant helps you focus on what matters most.

<p align="center">
  <b>🎙️ Transcribe · 📝 Summarize · 🔍 Analyze · 💬 Chat</b>
</p>

---

## ✨ Features

- 🎥 **Video & Audio Processing** — Process supported local media files and YouTube videos.
- 🎙️ **AI-Powered Transcription** — Convert speech into readable text using the configured speech recognition engine.
- 🌐 **Language-Aware Processing** — Support multilingual transcription or translation when enabled by the configured models.
- 📝 **Smart Summarization** — Generate concise summaries of lengthy recordings.
- 🏷️ **Automatic Title Generation** — Create meaningful titles based on content.
- ✅ **Action Item Extraction** — Identify tasks and follow-up actions discussed in recordings.
- 🔑 **Key Decision Detection** — Highlight important decisions and conclusions.
- ❓ **Open Question Identification** — Find unresolved questions and topics requiring further discussion.
- 💬 **Interactive AI Chat** — Ask questions about a recording and explore its content conversationally.
- 🧠 **Retrieval-Augmented Generation (RAG)** — Retrieve relevant transcript passages to provide context-aware answers.
- 🖥️ **Web Interface & CLI** — Use the Streamlit interface or command-line workflow.

---

## 🧠 How It Works

1. **Input:** Provide a supported media file or YouTube URL.
2. **Audio Processing:** Extract, convert, and prepare audio for transcription.
3. **Transcription:** Convert speech into text.
4. **Content Analysis:** Generate summaries, titles, action items, decisions, and open questions.
5. **Knowledge Indexing:** Convert transcript segments into searchable vector representations.
6. **Interactive Chat:** Retrieve relevant context and answer questions about the recording.

### Architecture Overview

```text
        Video / Audio / YouTube URL
                    |
                    v
            Audio Processing
                    |
                    v
              Transcription
                    |
                    v
               AI Analysis
                    |
          +---------+---------+
          |         |         |
          v         v         v
       Summary   Decisions  Action Items
                    |
                    v
               Vector Store
                    |
                    v
               RAG Pipeline
                    |
                    v
            Interactive AI Chat
```

---

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core application logic |
| Streamlit | Interactive web interface |
| OpenAI Whisper | Speech-to-text transcription, if configured |
| Mistral AI | Language-model-powered analysis, if configured |
| LangChain | LLM orchestration, if configured |
| ChromaDB | Vector storage, if configured |
| Hugging Face Embeddings | Semantic representation of transcript content, if configured |
| yt-dlp | YouTube media downloading, if configured |
| pydub | Audio conversion and processing, if configured |
| FFmpeg | Audio extraction and format conversion, if required |

*Verify the technology list against your actual dependencies and source code.*

---

## 📁 Project Structure

```text
AI-Video-Assistant/
|
├── app.py                     # Streamlit web application
├── main.py                    # Command-line entry point
├── test.py                    # Pipeline testing
├── Requirements.txt           # Python dependencies
|
├── core/
│   ├── transcriber.py         # Speech transcription
│   ├── summarizer.py          # Summary and title generation
│   ├── extractor.py           # Action items, decisions, and questions
│   ├── vector_store.py        # Vector storage and retrieval
│   └── rag_engine.py          # Retrieval-augmented question answering
|
├── utils/
│   └── audio_processor.py     # Audio extraction and processing
|
├── .gitignore                 # Git ignore rules
└── README.md                  # Project documentation
```

*Adjust this structure to match the files and folders that actually exist in your repository.*

---

## 🚀 Getting Started

### Prerequisites

Before running the application, make sure you have:

- Python 3.10 or a version compatible with your dependencies
- Git
- FFmpeg, if required by your audio-processing setup
- API credentials for the external AI services configured in your project

### 1. Clone the Repository

```bash
git clone https://github.com/Anuradha011/AI-Video-Assistant.git
cd AI-Video-Assistant
```

### 2. Create a Virtual Environment

**Windows**

```bash
python -m venv .venv
.venv\Scripts\activate
```

**macOS / Linux**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r Requirements.txt
```

If your requirements file uses a different capitalization, use its exact filename.

### 4. Configure Environment Variables

Create a `.env` file in the project root if your application uses environment variables.

Example:

```env
MISTRAL_API_KEY=your_mistral_api_key
SARVAM_API_KEY=your_sarvam_api_key
```

Only add the variables required by your source code. Replace these example names with the exact variable names expected by your application.

**Security:** Never commit your `.env` file, API keys, or other credentials to a public repository.

### 5. Run the Application

**Launch the Streamlit web interface:**

```bash
streamlit run app.py
```

Open the local URL shown in your terminal. Streamlit commonly uses:

```text
http://localhost:8501
```

**Run the command-line application:**

```bash
python main.py
```

Follow the prompts provided by the application.

---

## 💡 Use Cases

### 🏢 Meetings & Discussions

- Generate concise meeting summaries.
- Capture important decisions.
- Identify action items and follow-up tasks.
- Review discussions without replaying entire recordings.

### 🎓 Education & Learning

- Summarize recorded lectures.
- Extract important concepts.
- Ask questions about learning materials.
- Make long educational videos easier to review.

### 🔬 Research & Analysis

- Explore interviews and presentations.
- Search transcript content semantically.
- Identify key information from long recordings.

### ⚡ Productivity

- Reduce time spent reviewing recordings.
- Find relevant information through conversational queries.
- Turn unstructured media into organized knowledge.

---

## 🔐 Security & Privacy

- Keep API keys and credentials in environment variables.
- Exclude secret files from version control.
- Avoid committing private recordings or sensitive transcripts.
- Review the privacy policies of external AI providers used by the application.
- Process only media you have permission to access and analyze.

---

## 🧪 Testing

If `test.py` is configured as a runnable test script, execute:

```bash
python test.py
```

Ensure dependencies, environment variables, and required external services are configured before running tests.

---

## 🛣️ Future Enhancements

Potential improvements include:

- 📄 Export transcripts to TXT, PDF, or DOCX.
- ⏱️ Add timestamp-based navigation to important moments.
- 👥 Implement speaker identification and diarization.
- 🌍 Expand multilingual support.
- 📚 Maintain a searchable history of processed recordings.
- 📊 Add advanced analytics for meetings and presentations.
- ☁️ Support cloud deployment and scalable processing.

---

## 🤝 Contributing

Suggestions, bug reports, and improvements are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Implement and test your changes.
4. Commit your changes with a descriptive message.
5. Open a pull request describing your contribution.

---

## 📄 License

Refer to the repository's `LICENSE` file for the applicable terms of use, modification, and distribution.

If the repository does not contain a license, clarify the licensing terms before redistributing the project or its code.

---

## 🔗 Repository

**GitHub:** [Anuradha011/AI-Video-Assistant](https://github.com/Anuradha011/AI-Video-Assistant)

---

<p align="center">
  <b>🎬 Making video content easier to understand, search, and act upon.</b>
  <br>
  Built with Python, AI, and a focus on productivity.
</p>
