# Markdown to Google Docs Converter

This project was developed as part of a software engineering assessment.  
It provides a Python script and Colab notebook that automatically convert meeting notes written in **Markdown** into a well-formatted **Google Docs** document, applying styles (headings, lists, checkboxes, mentions, footer) using the Google Docs API.

---

## Features
- Converts Markdown meeting notes to Google Docs.
- Applies proper styles:
  - Title → Heading 1
  - Section headers → Heading 2
  - Sub-sections → Heading 3
  - Nested bullet hierarchy preserved
  - Markdown checkboxes → Google Docs checkboxes
  - `@mentions` styled in **bold**
  - Footer styled distinctly
- Runs on Google Colab with Google OAuth authentication.

---

## Setup Instructions

### Option 1: Run in Google Colab (recommended)
1. Open the Colab notebook: [Open in Colab](https://colab.research.google.com/github/USERNAME/REPO/blob/main/Markdown_to_google_docs.ipynb)  
2. Upload your `credentials.json` file in the left-side file panel.  
3. Run the notebook cells in order:
   - Install dependencies
   - Authenticate with your Google account
   - Execute the converter script
4. A link to the generated Google Doc will be printed at the end.

### Option 2: Run locally
1. Clone the repository:
```bash
git clone https://github.com/USERNAME/REPO.git
cd REPO
```
2. Create a virtual environment and install dependencies:
```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```
3. Place your `credentials.json` file in the project root.  
4. Run the script:
```bash
python markdown_to_gdocs.py
```

---

## Required Dependencies

```bash
google-api-python-client
google-auth-httplib2
google-auth-oauthlib
```

These are installed automatically in the first Colab cell.

---

## Example Usage

```python
from converter import convert_markdown_to_gdoc

markdown_text = """
# Product Team Sync
## Agenda
- [ ] @mike: Prepare slides
- [ ] @anna: Update designs
"""

convert_markdown_to_gdoc(markdown_text)
```

Output: A new Google Doc with proper headings, checkboxes, and mentions.

---

## Deliverables
- [GitHub Repository](https://github.com/USERNAME/REPO)
- [Colab Notebook](https://colab.research.google.com/github/USERNAME/REPO/blob/main/Markdown_to_google_docs.ipynb)

---

## Author
Developed by Hernán Agudelo as part of the Software Engineer Assessment Task.
