# Smart-ATS
This is a Streamlit web application named "Smart ATS" that serves as an Application Tracking System (ATS). The ATS evaluates resumes based on a given job description and provides feedback, including a percentage match, missing keywords, and other relevant information.

Required Libraries
streamlit: The main library for creating the web application.
google.generativeai: A library for interacting with the Gemini Pro model from Google Generative AI.
os: Provides a way to interact with the operating system, used for setting up API keys.
PyPDF2: Library for reading PDF files, used for extracting text from resumes.
dotenv: Loads environment variables from a file.
json: Used for working with JSON data.
Setting Up Environment
The application uses environment variables, loaded from a .env file.
The Google API key is required for accessing the Gemini Pro model.
python
Copy code
load_dotenv()  # Load environment variables
genai.configure(api_key=os.getenv("GOOGLE_API_KEY"))  # Configure Google Generative AI with API key
Gemini Pro Response
The function get_gemini_response is responsible for generating content using the Gemini Pro model.
Resume Text Extraction
The function input_pdf_text extracts text from a provided PDF file using PyPDF2.
Prompt Template
The input_prompt variable holds a template for the prompt to be given to the Gemini Pro model. It includes placeholders for the resume text and job description.
Streamlit App
The Streamlit application consists of a title, text area for pasting job descriptions, and a file uploader for uploading resumes in PDF format.
The main functionality is triggered when the user clicks the "Submit" button.
If a resume is uploaded, the application extracts text from the PDF, sends the prompt to the Gemini Pro model, and displays the response as a subheader.
Usage
Run the Streamlit app.
Paste the job description into the text area.
Upload a resume in PDF format.
Click the "Submit" button to receive the ATS evaluation.
Note
The application assumes that the Gemini Pro model is available and properly configured with a valid API key.
Ensure that the required libraries are installed before running the application.




