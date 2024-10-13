# 🎙️ GPT4o Real-Time Audio Processing

This project demonstrates real-time audio processing using the GPT4o Real-Time Audio SDK. It includes features such as resampling audio, sending audio chunks for processing, receiving transcription and response messages, and saving results to files. The project uses Azure or OpenAI's models to handle audio data and provide corresponding output.

## 🚀 Features
- **Audio Resampling**: Converts audio to a target sample rate to ensure compatibility.
- **Real-Time Audio Transmission**: Sends audio chunks asynchronously for real-time processing.
- **Receive and Handle Responses**: Handles audio transcription, response texts, and tool call arguments, and saves the outputs.
- **Supports Multiple Providers**: Works with Azure or OpenAI models for audio processing.

## 🛠️ Installation

To create a virtual environment and install the dependencies:

1. Create a virtual environment:
   ```sh
   python -m venv venv
   ```

2. Activate the virtual environment:
   - On Windows:
     ```sh
     venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```sh
     source venv/bin/activate
     ```

To get started, follow these steps to set up the environment:

1. Clone the repository:
   ```sh
   git clone https://github.com/your_username/gpt4o-realtime.git
   cd gpt4o-realtime
   ```

2. Install the required dependencies:
   ```sh
   pip install -r requirements.txt
   ```

3. Install the GPT4o Real-Time Audio SDK:
   ```sh
   pip install rtclient-0.4.4-py3-none-any.whl
   ```

## ▶️ Usage

After installing the dependencies, you can start the client by running:

```sh
python client_sample_custom.py
```

This script will:
- Load the configuration from `config.json`.
- Connect to the audio processing service using the specified provider (`azure` or `openai`).
- Send audio data for processing and save the responses to the output directory.

Make sure you have a valid audio file in the `input/` directory, and the `config.json` file is properly set up with your API key and model name.

### Example Configuration (`config.json`)
```json
{
    "model_name": "gpt-4o-realtime-preview-2024-10-01",
    "key": "YOUR_AZURE_KEY_HERE"
}
```

## 📂 Directory Structure
- **input/**: Directory containing input audio files.
- **output/**: Directory where output files (e.g., transcriptions, audio responses) are saved.

## ⚠️ Important Notes
- Ensure your Azure/OpenAI credentials are correctly configured in `config.json`.
- The sample rate for audio files should be 24 kHz for optimal performance.
- This project currently supports `.wav` files, and may require adjustments for other formats.
- The sample in wav with 256kbps is best, and use the input/convert.py for preprocess.

## 🔄 Updates
- **v1.0**: Initial release, featuring support for audio resampling, sending chunks, receiving responses, and handling Azure/OpenAI models.

## 🙏 Acknowledgements
This project is built on top of the [Azure Real-Time Audio SDK](https://github.com/Azure-Samples/aoai-realtime-audio-sdk/tree/main), and we thank Microsoft for providing the tools to enable seamless real-time audio processing.

## 📜 License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 🤝 Contributing
We welcome contributions! Feel free to submit a pull request or open an issue for any bugs or feature requests.

## 📧 Contact
For any questions, feel free to contact us at [fjiangai@gmail.com].

