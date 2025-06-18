# Publications Markdown Generator

This directory contains tools to generate publication markdown files from a TSV (Tab-Separated Values) file.

## How to Update Publications

### 1. Edit the TSV File
Edit `publications.tsv` with your publication data. The file should have these columns:

- `pub_date`: Publication date (YYYY-MM-DD format)
- `title`: Paper title
- `venue`: Journal/conference name
- `excerpt`: Brief description of the paper
- `citation`: Full citation in HTML format
- `url_slug`: URL-friendly version of the title (used for permalinks)
- `paper_url`: Link to the paper (optional)
- `slides_url`: Link to slides (optional)

### 2. Generate Markdown Files
Run the Python script to generate markdown files:

```bash
cd markdown_generator
python publications.py
```

This will create markdown files in the `../_publications/` directory.

### 3. Example TSV Format
```
pub_date	title	venue	excerpt	citation	url_slug	paper_url	slides_url
2023-09-01	Your Paper Title	Journal Name	Brief description of your paper	Author, A. (2023). "Your Paper Title." <i>Journal Name</i>.	your-paper-title	https://doi.org/10.1000/paper	https://slides.com/paper
```

### 4. Download/Export TSV
To download the current TSV file:
- Navigate to `markdown_generator/publications.tsv`
- Download or copy the file
- Edit in Excel, Google Sheets, or any text editor
- Save as TSV format

### 5. Import from Other Sources
You can also:
- Export from reference managers (EndNote, Mendeley, Zotero) as TSV
- Convert from BibTeX using online tools
- Create from scratch in a spreadsheet and export as TSV

## Notes
- The script automatically escapes special characters for YAML compatibility
- Each publication gets its own markdown file with proper metadata
- Files are named as `YYYY-MM-DD-url-slug.md`
- Permalinks follow the pattern `/publication/YYYY-MM-DD-url-slug`

# Jupyter notebook markdown generator

These .ipynb files are Jupyter notebook files that convert a TSV containing structured data about talks (`talks.tsv`) or presentations (`presentations.tsv`) into individual markdown files that will be properly formatted for the academicpages template. The notebooks contain a lot of documentation about the process. The .py files are pure python that do the same things if they are executed in a terminal, they just don't have pretty documentation.




