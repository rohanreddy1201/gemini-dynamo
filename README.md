
# Gemini Dynamo

Gemini Dynamo is an AI-powered platform for processing and analyzing video content from YouTube. It uses advanced natural language processing techniques to extract key concepts and summarize the content, leveraging Google Cloud's Vertex AI for its machine learning models.

## Features

- **YouTube Video Processing**: Extracts and processes transcripts from YouTube videos.
- **Key Concepts Extraction**: Identifies and defines key concepts and terms from the video transcripts.
- **Summarization**: Generates concise summaries of video content.
- **FastAPI Integration**: Provides an API endpoint for analyzing YouTube videos.

## Installation

To install and run this project locally, follow these steps:

### Prerequisites

- Python 3.8 or higher
- Google Cloud account and Vertex AI setup
- FastAPI
- Node.js and npm (for frontend)

### Clone the Repository

```sh
git clone https://github.com/rohanreddy1201/gemini-dynamo.git
cd gemini-dynamo
```

### Backend Setup

1. **Create a Virtual Environment**

```sh
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

2. **Install Backend Dependencies**

```sh
pip install -r requirements.txt
```

3. **Set Up Google Cloud Credentials**

Ensure your Google Cloud credentials are set up properly and the `authenticate.json` file is securely managed and not included in version control.

4. **Run the FastAPI Server**

```sh
uvicorn main:app --reload
```

### Frontend Setup

1. **Navigate to Frontend Directory**

```sh
cd frontend/dynamocards
```

2. **Install Frontend Dependencies**

```sh
npm install
```

3. **Run the Frontend Server**

```sh
npm run dev
```

## Usage

### Analyzing a YouTube Video

To analyze a YouTube video, send a POST request to the `/analyze_video` endpoint with the video URL:

```sh
curl -X POST "http://127.0.0.1:8000/analyze_video" -H "Content-Type: application/json" -d '{"youtube_link": "https://www.youtube.com/watch?v=example"}'
```

### Project Structure

```
gemini-dynamo/
├── backend/
│   ├── authenticate.json    # Google Cloud credentials (should be ignored in .gitignore)
│   ├── main.py              # FastAPI entry point
│   ├── services/
│   │   └── genai.py         # Core logic for video processing and AI integration
│   └── requirements.txt     # Python dependencies
├── frontend/
│   ├── dynamocards/
│   │   ├── src/             # Frontend application source code
│   │   ├── public/          # Static files
│   │   ├── package.json     # npm dependencies
│   │   └── README.md        # Frontend specific README
└── README.md                # Project README
```

### Contributing

Contributions are welcome! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Create a Pull Request.

### License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

### Contact Information

For any questions or feedback, please contact:

- **Rohan Reddy**
- [GitHub Profile](https://github.com/rohanreddy1201)
- [LinkedIn](https://www.linkedin.com/in/rohan-reddy-964019146/)
