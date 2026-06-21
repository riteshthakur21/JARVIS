# J.A.R.V.I.S 🤖

An AI-powered offline personal assistant developed by **Ritesh Raj**.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python 3.10](https://img.shields.io/badge/Python-3.10-blue.svg)](https://www.python.org/)
[![Ollama](https://img.shields.io/badge/Ollama-Local%20LLM-orange.svg)](https://ollama.com/)

JARVIS is a Python-based offline AI assistant designed to provide voice interaction, local LLM integration, computer vision capabilities, automation features, speech-to-text processing, and text-to-speech responses. Everything runs locally on your machine, prioritizing privacy and offline functionality.

---

## 📸 Sneak Peek (WIP UI)
You can view a preview of the desktop UI (still in active development) in the [koki/README.md](JARVIS/koki/README.md) file.

---

## 🌟 Features

* **Voice Commands & Interaction** — Hands-free interaction using offline wake word and command recognition.
* **Speech-to-Text (STT)** — Offline voice transcription support.
* **Text-to-Speech (TTS)** — Offline text-to-speech with natural voice response using LuxTTS/Kokoro.
* **Local LLM Integration** — Fully powered by local Ollama models (fine-tuned LLama-2 models or customizable ones).
* **Computer Vision Support** — Uses OpenCV and Llava to "see" and describe environments/objects from your camera.
* **YouTube Search & Playback** — Easily search and play your favorite music or videos hands-free.
* **Browser Automation** — Open pages and search the web using voice actions.
* **Date & Time Assistance** — Keep track of schedules, current dates, and times.
* **Offline Processing** — 100% private; no data leaves your machine.
* **Environment-Based Configuration** — Easily configure API keys, voices, models, and third-party details using `.env`.

### 💡 Example Commands to Try
* **Time/Date:** `"What time is it?"` or `"What is the date today?"`
* **Web Search:** `"Hey Jarvis, help me search for the best recipe for pancakes."`
* **YouTube:** `"Hey Jarvis, play Girls like you by Maroon 5 on YouTube."`
* **Vision:** `"What is this?"`, `"Look at this"`, or `"Describe what you see."` (Uses webcam + Llava).
* **Shutdown:** `"Go to sleep"`, `"Goodbye"`, or `"Shutdown"`.

---

## 🛠️ Tech Stack

* **Language:** Python
* **LLM Engine:** Ollama
* **Computer Vision:** OpenCV
* **Local Models:** Llama-2-7b-chat-jarvis (fine-tuned on custom Stark-Jarvis dialog datasets) / Llava (Vision)
* **Concurrency:** AsyncIO

---

## 📂 Project Structure

| Directory/File | Purpose |
| -------------- | ------- |
| [`modules/`](JARVIS/modules) | Core assistant functionality (vision, speech, command execution, NLP) |
| [`config/`](JARVIS/config) | Configuration files and initialization scripts |
| [`dataset/`](JARVIS/dataset) | Training dataset resources and model preparation notebooks |
| [`ollama/`](JARVIS/ollama) | Local model integration, custom model configurations, and Modelfiles |
| [`koki/`](JARVIS/koki) | UI and frontend desktop application resources (React + TypeScript + Electron) |
| [`assets/`](JARVIS/assets) | Static assets, saved image captures, and local resources |

---

## 🚀 Installation & Setup

### 1. Prerequisites (Ollama Setup)
You need Ollama installed to run the local LLM and vision model.
1. Download and install Ollama from [ollama.com](https://ollama.com/).
2. Pull/run the custom Jarvis model:
   ```bash
   ollama run fotiecodes/jarvis
   ```
3. Pull the vision model for computer vision features:
   ```bash
   ollama run llava
   ```

### 2. Clone Repository
```bash
git clone https://github.com/riteshthakur21/JARVIS.git
cd JARVIS
```

### 3. Create & Activate Virtual Environment
```bash
# Create virtual environment
python -m venv venv

# Activate environment (Windows)
venv\Scripts\activate

# Activate environment (macOS/Linux)
source venv/bin/activate
```

### 4. Install Dependencies
```bash
pip install -r requirements.txt
```
*Note: To recursively install all requirements from subdirectories (if needed):*
```bash
find . -name "requirements.txt" | while read req; do echo "Installing from $req..."; pip install -r "$req"; done
```

### 5. Configure Environment Variables
Copy `.env.example` to `.env` and fill in the required variables (API keys, custom model names, TTS voice settings, etc.):
```bash
cp .env.example .env
```

---

## 🏃 Running Jarvis

Run the main application script:
```bash
python main.py
```

---

## 🗺️ Roadmap

* [ ] **Advanced Voice Cloning** — Seamless, ultra-realistic voice cloning to match JARVIS's movie tone.
* [ ] **Better Memory System** — Long-term recall of user preferences, previous chats, and context.
* [ ] **Desktop Dashboard** — Beautiful HUD widgets and real-time visualization of the environment.
* [ ] **Smart Home Integration** — Control smart switches, lights, and appliances (e.g., Tapo integration).
* [ ] **Multi-Agent Support** — Delegating sub-tasks to other specialized AI agents.
* [ ] **Personal Productivity Tools** — Calendar management, automated email drafting, and file organization.

---

## 🤝 Contributing & Development
Please refer to [CONTRIBUTOR.md](JARVIS/CONTRIBUTOR.md) for local development setup, model quantization, and contribution guidelines.

---

## 📈 Star History

<a href="https://star-history.com/#riteshthakur21/JARVIS&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=riteshthakur21/JARVIS&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=riteshthakur21/JARVIS&type=Date" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=riteshthakur21/JARVIS&type=Date" />
 </picture>
</a>

---

## 👤 Developer
**Ritesh Raj** - [GitHub Profile](https://github.com/riteshthakur21)

---

## 📄 License
This project is licensed under the MIT License. See the [LICENSE](JARVIS/LICENSE) file for details.

---

## ⚠️ Disclaimer
AI responses may be inaccurate. Always verify important information before making decisions.
