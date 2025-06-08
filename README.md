# Smart ATS Resume Evaluator

This is a Streamlit web application that uses **Google Gemini (Generative AI)** to evaluate your resume against a provided job description. It gives insights into how well your resume matches the job and suggests improvements for better visibility in **ATS (Applicant Tracking Systems)**.

## Features

* ✅ Upload your resume as a **PDF**
* ✅ Paste a **Job Description**
* ✅ Automatically extract and analyze resume content
* ✅ Uses **Gemini 1.5 Pro** model to:

  * Calculate **percentage match**
  * Highlight **missing important keywords**
  * Provide a **short profile summary**

## Setup Instructions

1. **Clone the repository:**

   ```cmd
   git clone https://github.com/your-username/ats-resume-evaluator.git
   cd ats-resume-evaluator
   ```

2. **Install the required packages:**

   ```cmd
   pip install -r requirements.txt
   ```

3. **Create a `.env` file and add your Google API key:**

   ```
   GOOGLE_API_KEY=your_api_key_here
   ```

4. **Run the app:**

   ```cmd
   streamlit run app.py
   ```

## Output Format

Gemini returns a JSON string like:

```json
{
  "JD Match": "87%",
  "MissingKeywords": ["SQL", "Kubernetes", "Data Pipeline"],
  "Profile Summary": "The resume shows strong experience in data analysis but lacks DevOps tools mentioned in the JD."
}
```