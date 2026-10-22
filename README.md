<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=250&section=header&text=Ridhima&fontSize=80&fontAlignY=35&animation=twinkling&desc=GenAI%20%26%20Speech%20AI%20%7C%20LLMs%20%E2%80%A2%20RAG%20%E2%80%A2%20FastAPI&descAlignY=55&descAlign=50" />
</div>

## 🧠 About Me

I build LLM and speech AI applications with Python and FastAPI backends: speech-to-text pipelines, LLM-generated study material, and retrieval over user data.
From June to September 2026 I was a research intern at the MISN Lab, IIT Delhi, studying hallucination and grounding in vision-language models that write disaster reports from satellite imagery.
I am a B.Tech CSE (AI) student at KIET, graduating in 2028.

---

## 🚀 Featured Projects

### 1. 🎙️ [VoicePilot](https://github.com/Ridhima028/voiceassistant/tree/main/voicepilot-ai)

**Turns recorded lectures into transcripts, notes, quizzes and flashcards.**

**Stack:** FastAPI · Celery · Redis · PostgreSQL · faster-whisper · Gemini API · MinIO (S3) · Docker Compose

- Uploads return `202` right away; a Celery worker pulls the job from Redis, transcribes it with faster-whisper (`small`, INT8 on CPU) and writes the status to PostgreSQL, retrying with backoff and jitter.
- Regroups Whisper's pause-based segments into topic chunks using pause length plus cosine similarity of Gemini embeddings, with a 25-second cap per chunk.
- Generates a summary, notes, quiz, flashcards, key concepts, mind map and chapters through Gemini's JSON mode (Qwen via OpenRouter as an alternative), and exports the study pack as HTML. JWT auth; audio stored in MinIO.

### 2. 📻 [iTantra](https://github.com/tensorbytes0202/Agni_team_Itantra)

**Offline speech-to-speech messaging in 10 Indian languages over weak links. Smart India Hackathon 2026 (PS 26173), Team Agni, selected at institutional level.**

**Stack:** Python · Vosk · AI4Bharat IndicConformer (sherpa-onnx) · Piper · Meta MMS · UDP · Streamlit · Tkinter

- Runs STT and TTS fully offline: Vosk and IndicConformer INT8 for STT (9 of the 10 languages so far), Piper and MMS for TTS (all 10). STT on an English test sentence took 113 ms on a laptop CPU (RTF 0.03).
- Picks a link from live packet-loss and round-trip probes and shapes the message to fit it: full text on Wi-Fi, zlib on weak Wi-Fi, and a 2-byte alert summary with Hamming(7,4) FEC on an emulated 600 bps radio link. Failover from Wi-Fi to radio takes about 4 s.
- CRC-checked packets with ACK and retry, plus an on-disk store-and-forward queue that sends alerts first when a link returns. CI runs the test suite on Python 3.10 and 3.11.

<!-- TODO: CALPT. No repo found under Ridhima028; fill in the description, stack, bullets and link, then uncomment.
### 3. 🧮 CALPT

**TODO: one-line description**

**Stack:** TODO

- TODO
- TODO
-->

---

## 🗂️ Other Projects

- **[ai-calendar-assistant](https://github.com/Ridhima028/ai-calendar-assistant):** manage Google Calendar in natural language; Gemini for intent detection, LangChain, and RAG over a FAISS vector store (Flask).
- **visual-assistant:** visual question answering with a FastAPI backend and a Streamlit UI.
- **[gender-age-detector](https://github.com/Ridhima028/gender-age-detector):** CNN (MobileNetV2) trained on UTKFace for gender and age-bucket prediction, served through FastAPI and Streamlit.

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| **LLMs & GenAI** | Gemini API, LangChain, RAG (FAISS), embeddings, OpenRouter |
| **Speech** | faster-whisper, Vosk, IndicConformer (sherpa-onnx), Piper, Meta MMS |
| **Backend** | FastAPI, Flask, REST, Celery, Redis, PostgreSQL, Docker |
| **ML** | TensorFlow/Keras, scikit-learn, NumPy, OpenCV |
| **Languages** | Python, JavaScript |

---

## 📊 GitHub Stats

<div align="center">
  <img height="160em" src="https://github-readme-stats.vercel.app/api?username=Ridhima028&show_icons=true&theme=radical&hide_border=true" alt="GitHub Stats" />
  <img height="160em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Ridhima028&layout=compact&theme=radical&hide_border=true" alt="Top Languages" />
</div>

---

## 📬 Contact

Looking for internships in GenAI, AI backend and speech AI.

<div align="center">
  <a href="https://www.linkedin.com/in/ridhima-goyal-623b07337"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge"/></a>
  <a href="mailto:ridsgoyal08@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email Badge"/></a>
  <a href="https://github.com/Ridhima028"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Badge"/></a>
</div>
