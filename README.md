Here's your complete, laptop-ready package. Download videoiq.zip and follow these steps:
Setup (5 minutes):
bash# 1. Unzip and enter the folder
unzip videoiq.zip && cd videoiq

# 2. Add your Anthropic API key
cp .env.example .env
# Edit .env → paste your ANTHROPIC_API_KEY

# 3. Run — installs everything and starts the server
python start.py
Then open http://localhost:8000 in your browser.
What's inside the zip:
FilePurposeapp.pyFastAPI backend — full 7-step pipeline (FFmpeg → Whisper → Claude)static/index.htmlComplete frontend (the full VideoIQ UI, no build step needed)start.pyOne-shot setup script: checks FFmpeg, installs packages, pre-downloads Whisper, launches serverrequirements.txtfastapi, uvicorn, anthropic, openai-whisper, opencv-python.env.exampleTemplate for your API key and Whisper model sizeREADME.mdFull setup + troubleshooting guide

Two prerequisites only:

Python 3.9+ (you likely have it)
FFmpeg — brew install ffmpeg on Mac, sudo apt install ffmpeg on Ubuntu, or the Windows installer from ffmpeg.org

The tool works without an API key (you still get a full Whisper transcript), and AI summaries activate the moment you add your key to .env.
