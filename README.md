# PDF-VoiceMate
  PDF VoiceMate is a Python project that converts PDF files into text and then transforms the text into speech using Google Cloud's Text-to-Speech API. The output is an MP3 file that allows users to listen to the content of their PDF files.

## Features
- Extracts text from PDF files.
- Converts extracted text into an audio file (MP3 format).
- Leverages Google Cloud's Text-to-Speech API for high-quality audio synthesis.

## Prerequisites
- Python 3.7 or higher.
- A valid Google Cloud Text-to-Speech service account file.
- Installed Python libraries:
  - PyPDF2
  - google-cloud-texttospeech
  - python-dotenv

## Installation
1. Clone the repository:
```
  git clone <repository-url>
  cd <repository-directory>
```

2. Install the required dependencies:
```
  pip install -r requirements.txt
```
3. Set up your Google Cloud Service Account:
```
  Generate a service account key in Google Cloud Console.
  Save the JSON file and set its path in an .env file using the variable file_path.
```
4. Create a .env file:
```
    file_path=path/to/your/service_account.json
```

## Usage
1. Place your PDF file in the project directory.
2. Update the pdf_path variable in the script to point to your PDF file:
```
  pdf_path = 'your-pdf-file.pdf'
```
3. Run the script:
```
  python main.py
```
4. After execution:
- The text content will be extracted from the PDF and saved as output.mp3.
- You can listen to the audio file.

## Example
Given a PDF file named test-1.pdf, running the script will:
1. Extract text from the PDF.
2. Generate an audio file output.mp3 in the current directory.
3. Print success messages to indicate progress.

## Project Structure
```
  .
  ├── main.py                # The main script
  ├── requirements.txt       # Required Python libraries
  ├── .env                   # Environment variables for API key
  └── README.md              # Project documentation
```
## Notes
- Ensure your Google Cloud project is set up with Text-to-Speech API enabled.
- Use PDFs with selectable text. Scanned images within PDFs may not extract properly without OCR.
- For long PDF files, consider breaking the text into smaller chunks for better audio synthesis.

## License
This project is open-source and available under the MIT License.
