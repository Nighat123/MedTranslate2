
# MedTranslate - Healthcare Translator

**MedTranslate** is a web-based healthcare translation application that enables secure, real-time translation of medical conversations. It supports speech-to-text, text enhancement for medical terminology, translation across multiple languages, and text-to-speech playback.

---

## Features

- **Real-Time Speech Recognition:** Capture spoken input and convert it to text.
- **Medical-Aware Text Enhancement:** Automatically improves grammar and medical terminology (English source only).
- **Multi-Language Translation:** Translate text to and from over 20 languages.
- **Text-to-Speech Playback:** Listen to the translated output in the target language.
- **Privacy-Focused:** Text is processed securely without storing sensitive data.

---

## Tech Stack

- **Backend:** Flask, Python 3
- **Frontend:** HTML, CSS, JavaScript
- **AI Models:**  
  - MarianMT (Helsinki-NLP) for translation  
  - Optional T5-based model for grammar correction/enhancement
- **APIs & Libraries:**  
  - `transformers`, `torch`, `flask-cors`

---

## Project Structure

```

MedTranslation/
│
├─ app.py               # Main Flask backend
├─ requirements.txt     # Python dependencies
├─ static/
│   ├─ home.html        # Landing page
│   ├─ index.html       # Translation interface
│   └─ app.js           # Frontend JS for interaction
└─ README.md            # Project documentation

````

---

## Installation

1. **Clone the repository**
```bash
git clone https://github.com/Nighat123/MedTranslation.git
cd MedTranslation
````

2. **Create a virtual environment**

```bash
python -m venv venv
source venv/bin/activate      # Linux/Mac
venv\Scripts\activate         # Windows
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```

4. **Setup environment variables**

Create a `.env` file in the project root with placeholder values:

```bash
OPENAI_API_KEY=your_api_key_here
CORS_ALLOW_ORIGINS=*
```

> **Note:** Do **not** commit your real API key to the repository. Only provide placeholders.

5. **Run the app**

```bash
python app.py
```

6. **Access the app**

Open your browser and go to:

```
http://127.0.0.1:5000/
```

---

## Usage

* Click **Start Translating** on the home page to access the translation interface.
* Select your source and target languages.
* Click 🎤 **Start Speaking** to record your voice.
* Click ⏹️ **Stop** to process the text.
* Click 🔊 **Speak Translation** to hear the translated output.

---

## Supported Languages

* Arabic, German, Spanish, French, Hindi, Indonesian, Italian, Japanese, Korean, Dutch, Polish, Russian, Swedish, Thai, Turkish, Ukrainian, Urdu, Vietnamese, Chinese, English

---

## Security & Privacy

* Sensitive data like API keys are stored locally in `.env` and never pushed to the repository.
* Speech and text data are processed in-memory and not logged or stored.

---

## References

* [Helsinki-NLP MarianMT Models](https://huggingface.co/Helsinki-NLP)
* [T5 Grammar Correction Model](https://huggingface.co/vennify/t5-base-grammar-correction)
* [Flask Documentation](https://flask.palletsprojects.com/)

---

## License

This project is licensed under the MIT License.

```




