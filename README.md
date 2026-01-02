# AI-Powered Question Generation & Automated Grading System 

An intelligent system designed to automate the examination process. It reads educational material (PDF/DOCX), uses Generative AI to create essay questions, and employs Semantic Similarity to grade student answers automatically.

##  Key Features
The project consists of two main phases:

### Phase 1: Question Generation (Generative AI)
* **Input:** Accepts `PDF` or `DOCX` files containing project documentation or study material.
* **Model:** Uses **Mistral-7B-Instruct** (via Hugging Face) to understand the text.
* **Output:** Generates deep essay questions along with model answers and saves them to a JSON file.

### Phase 2: Automated Evaluation (Semantic Analysis)
* **Simulation:** An interactive Q&A session where the user acts as the student.
* **Grading Engine:** Uses **Sentence-Transformers (mpnet-base)** to convert answers into vector embeddings.
* **Scoring:** Calculates **Cosine Similarity** between the student's answer and the model answer to provide a score out of 5 with qualitative feedback.

##  Tech Stack
* **LLM:** Mistral-7B-Instruct-v0.2.
* **NLP & Embeddings:** Sentence-Transformers (`paraphrase-multilingual-mpnet-base-v2`), PyTorch.
* **File Handling:** PyPDF2, python-docx.
* **Platform:** Google Colab (with GPU support).

##  How to Use
1.  **Mount Drive:** Ensure your project files are uploaded to Google Drive.
2.  **Generate Questions:** Run the first part of the notebook to parse the document and generate the `essay_questions_and_answers.json` file.
3.  **Start Defense Simulation:** Run the second part to start the interactive exam. Enter your answers and get instant feedback.

##  Evaluation Logic
The grading is not keyword-based but meaning-based:
* **> 4.5/5:** Excellent (High semantic match).
* **3.5 - 4.4:** Very Good.
* **2.5 - 3.4:** Fair.
* **< 2.5:** Needs Improvement.

---
**Developed by:** [Sherin Shaban]
