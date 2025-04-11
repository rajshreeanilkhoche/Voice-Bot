
# Voice-Bot

real_time_voice_bot/
├── backend/
│   ├── __init__.py
│   ├── server/
│   │   ├── __init__.py
│   │   ├── live_ws_server.py      # WebSocket server for real-time voice bot
│   │   ├── ws_consumer.py         # Handles audio chunk receiving logic
│   │   ├── config.py              # Config vars (model paths, thresholds, etc.)
│   │   └── utils.py               # Audio helper functions
│   ├── core/
│   │   ├── __init__.py
│   │   ├── stt.py                 # Speech-to-Text (faster-whisper)
│   │   ├── llm.py                 # Text generation (llama3, Zephyr via Ollama)
│   │   ├── tts.py                 # Text-to-Speech (XTTSv2 from Coqui)
│   │   └── voice_streamer.py      # Streams audio from TTS output in real time
├── frontend/
│   └── (optional React/static)    # For mic input, UI avatar later
├── recordings/
│   └── audio_chunk_*.wav          # Temporary audio chunks
├── voices/
│   └── output_*.wav               # Generated TTS chunks (can stream them)
├── requirements.txt
└── README.md                      