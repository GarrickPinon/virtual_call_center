# Real-Time AI Sales Agent (Voice) 🎙️

A production-grade voice AI agent capable of holding natural sales conversations with <500ms latency.

**Tech Stack:**
- **Inference**: [Cerebras](https://cerebras.ai) (LLaMA 3.3 70B) - Instant token generation.
- **Transport**: [LiveKit](https://livekit.io) - Real-time WebRTC infrastructure.
- **STT**: [Deepgram](https://deepgram.com) - Nova-2 Speech-to-Text.
- **TTS**: [Cartesia](https://cartesia.ai) - Sonic Low-latency Text-to-Speech.
- **VAD**: Silero Voice Activity Detection.

## Architecture
The agent runs a continuous loop:
1.  **Listen**: Ingest audio stream via LiveKit/Deepgram.
2.  **Think**: Process query with LLaMA 3.3 on Cerebras Wafer-Scale Engine.
3.  **Speak**: Stream text to Cartesia for instant audio synthesis.

## Usage
This project is designed to run in Google Colab or a local Python environment.

1.  Install dependencies:
    ```bash
    pip install livekit-agents livekit-plugins-openai livekit-plugins-deepgram livekit-plugins-silero
    ```
2.  Set API Keys:
    - `CEREBRAS_API_KEY`
    - `LIVEKIT_API_KEY`
    - `DEEPGRAM_API_KEY`
    - `CARTESIA_API_KEY`

3.  Run the notebook `virtual_sales_agent.ipynb`.


---
> **Built with [Antigravity](https://deepmind.google)** 
