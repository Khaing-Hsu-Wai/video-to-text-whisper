# 🎙️ Whisper Video-to-Text Transcriber

This project uses [OpenAI Whisper](https://github.com/openai/whisper) to transcribe spoken content from video files (e.g., `.mp4`, `.mov`) into readable text and subtitle formats like `.srt` and `.vtt`.

---

## 📌 Features

- 🎞️ Convert audio from videos into text
- 🗣️ Supports multiple spoken languages (e.g., Japanese, English)
- 🧾 Generates multiple output formats: `.txt`, `.srt`, `.vtt`, `.tsv`
- ⚙️ Simple CLI usage with Whisper

---

## Requirements

Before you begin, make sure you have the following installed:

- Python 3.8+
- `ffmpeg` (used to extract audio from video)
- `git` (to install Whisper directly from GitHub)

---

## 🛠️ Step-by-Step Setup Guide

### 1. Clone the Repository (or create your own folder)
```bash
git clone https://github.com/khaing-hsu-wai/video-to-text-whisper.git
cd video-to-text-whisper
```
### 2. Create and Activate Python Virtual Environment
```bash
python3 -m venv whisper-env
source whisper-env/bin/activate
```
### 3. Install Whisper and Dependencies
```bash
pip install git+https://github.com/openai/whisper.git
```
Also, make sure ffmpeg is installed:

macOS:
```bash 
brew install ffmpeg
```

Ubuntu:
```bash
sudo apt update
sudo apt install ffmpeg
```
Windows:
Download from: https://ffmpeg.org/download.html and add it to PATH.

### 4. Move your video file (e.g., 3_Class.mov) into the project folder.

### 5. Run Whisper to Transcribe
```bash
whisper 3_Class.mov --language Japanese --task transcribe
```
You’ll get the following output files:

`.txt` – plain text transcription

`.srt` – subtitles for video

`.vtt` – subtitles (web format)

`.tsv` – detailed timestamps per word

`.json` – structured transcription metadata (timestamps, segments, confidence)
