Startup Pitch Deck Analyzer

This project is a NLP-powered pitch deck analyzer that extracts text from PDF presentations, summarizes the content, performs sentiment analysis, and assigns heuristic scores to key startup evaluation dimensions (team, product, market, traction, and technology moat).

It is designed to help investors, accelerators, and analysts quickly evaluate startup pitch decks.

Features

Extracts text from PDF and PPTX files

Cleans and preprocesses raw text

Summarizes pitch decks using BART-large-cnn

Performs full-text sentiment analysis

Embedding support with SentenceTransformers + FAISS

Heuristic scoring for startup evaluation criteria

Highlights risks and suggests next steps

Outputs structured results in pandas DataFrames

Option to generate a sample positive pitch deck (PDF)

📂 Project Structure
├── StartupPitchDeckAnalyzer.ipynb   # Main notebook (Colab)
├── sample_pitchdeck.pdf             # Example input (negative case)
├── sample_pitchdeck_positive.pdf    # Example input (positive case)
└── (optional) generated_positive.pdf # Auto-created demo pitch deck

Requirements

The code is built to run in Google Colab. Main dependencies:

pdfplumber – extract text from PDFs

python-pptx – extract text from PowerPoint slides

transformers – summarization & sentiment analysis

sentence-transformers – embeddings

faiss – vector search support

pandas – tabular output

reportlab – generate demo PDFs

Install in Colab if needed:

!pip install pdfplumber python-pptx transformers sentence-transformers faiss-cpu reportlab

▶Usage Instructions

Open the notebook in Google Colab
Upload the .ipynb file and run all cells.

Mount Google Drive
The code mounts your Drive to access input files.

Prepare input pitch decks
Place files in your Drive, e.g.:

/content/drive/My Drive/sample_pitchdeck.pdf
/content/drive/My Drive/sample_pitchdeck_positive.pdf


Run the analysis
The script will:

Extract text

Summarize

Analyze sentiment

Score the startup

View Results
Results are shown as pandas tables in Colab:

Summary + sentiment

Heuristic scores

Risks

Suggested next steps
