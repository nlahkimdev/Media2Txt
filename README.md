# Transcribe Audio and Video to text - Language autodeteced

```bash

New-Item main.py, transcribe.py, .env

python -m pip install — user virtualenv

python -m venv venv

venv/Scripts/activate

pip install streamlit requests python-dotenv assemblyai

streamlit run main.py
```

## Get your Assemblyai API TOKEN

[https://www.assemblyai.com/dashboard/activation](https://www.assemblyai.com/dashboard/activation)

> in file `.env` add this line of code

```python
API_TOKEN = “Your API Key”.
```

## Sample Code

```python
# `pip install assemblyai` (Windows)

import assemblyai as aai

aai.settings.api_key = "API_TOKEN"
transcriber = aai.Transcriber()

transcript = transcriber.transcribe("https://storage.googleapis.com/aai-web-samples/news.mp4")
# transcript = transcriber.transcribe("./my-local-audio-file.wav")

print(transcript.text)
```
