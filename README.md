# Text-Summarization

## Explanation of the Code:

This project utilises code that transcribes an audio file and then uses the transcript to generate a summary using PaLM. Here's a gist:

1. **Installation:**
   - It installs libraries for audio processing (`whisper`), text generation (`google-generativeai`), and dependency management (`pip`).
   - It updates and installs `ffmpeg` for audio manipulation (likely on a Linux system).

2. **Transcription:**
   - It loads the "base" model from Whisper for speech recognition.
   - It loads the audio file (`Limetown1.mp3`) and ensures it's within a 30-second window.
   - It converts the audio into a format suitable for the model and transfers it to the same device as the model (CPU or GPU).
   - It detects the spoken language. If it's not English, it translates the audio during transcription. Otherwise, it transcribes directly.
   - Finally, it stores the transcribed text (`text`).

3. **PaLM Configuration:**
   - It configures the PaLM API using an API key.
   - It sets default parameters for text generation, including model selection, temperature (creativity), number of candidates, and stopping sequences (phrases to end generation).
   - It prints the number of available CPUs.

4. **PaLM Summary Generation (Commented Out):**
   - This section is currently commented out (`#@title`). 
   - It defines a prompt that asks PaLM to summarize the transcribed text (`text`).
   - It generates text using PaLM based on the prompt and prints the response (`Summary`).

## Summary:

This code utilizes Whisper, a speech recognition model, to transcribe audio and PaLM, a large language model, to summarize the transcribed text.
The outcome is an automatic speech summarization system.
