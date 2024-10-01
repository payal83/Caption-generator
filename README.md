# Image Caption Generator with TTS

This project is a web application that allows users to upload images and generate captions using a pre-trained model. The generated captions can also be converted to speech using Google Text-to-Speech (gTTS), which can be played or downloaded directly from the webpage.

## Features
- Upload an image file and generate a caption using the `Salesforce/blip-image-captioning-base` model.
- Converts the generated caption into audio using Google Text-to-Speech (gTTS).
- Displays the uploaded image along with the generated caption and an audio player to listen to the caption.


## Project Structure

```
project/
│
├── app.py                     # Main Flask app
├── static/                     # Static files (uploads and audio)
│   ├── uploads/                # Folder for uploaded images
│   └── audio/                  # Folder for audio files generated by gTTS
├── templates/
│   └── index.html              # HTML file for rendering the webpage
├── requirements.txt            # Python dependencies
└── README.md                   # Project documentation
```

## Installation and Setup

1. **Clone the repository:**

   ```bash
   git clone https://github.com/ninja-whale/image-caption-generator.git
   cd image-caption-generator
   ```

2. **Create a virtual environment:**

   ```bash
   python3 -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Flask application:**

   ```bash
   python app.py
   ```

5. **Open your browser and navigate to:**

   ```
   http://127.0.0.1:5000/
   ```

## Dependencies

This project relies on the following libraries:

- **Flask**: Web framework used to create the application.
- **Pillow**: For image processing.
- **transformers**: Hugging Face transformers library for loading the image captioning model.
- **gTTS**: Google Text-to-Speech library for converting text into audio.
- **Werkzeug**: Used for securing file uploads.

To install the dependencies, use:

```bash
pip install -r requirements.txt
```

## Usage

1. **Upload an Image**: 
   Upload any image file (e.g., `.jpg`, `.png`) through the web interface.
   
2. **Generate Caption**: 
   Once uploaded, the model will generate a caption based on the content of the image.

3. **Play Caption as Audio**: 
   The caption will also be converted to speech using Google Text-to-Speech (gTTS). An audio player will appear, allowing you to listen to the caption.


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

