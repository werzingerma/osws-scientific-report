# PRECISION Scientific Reports

Automated workflow for scientific reports with Quarto and GitHub Pages.

## Features

- **Jupyter Notebooks** → automatic conversion to HTML/PDF/LaTeX/Word
- **GitHub Actions** - Fully automated deployment
- **Journal Profiles** for Springer, Elsevier, Nature, Lancet
- **Zotero Integration** for reference management
- **Responsive Design** with custom PRECISION theme
- **Automatic Downloads Generation**

## Quick Start

```bash
# 1. Clone repository
git clone https://github.com/werzingerma/osws-scientific-report.git
cd osws-scientific-report

# 2. Set up Python environment
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt

# 3. Create notebook
# - Create a Jupyter Notebook in notebooks/
# - Run all cells
# - Add YAML header in raw cell

# 4. Push - done!
git add .
git commit -m "Add: New report"
git push
```

GitHub Actions automatically generates all formats (HTML, PDF, LaTeX, Word) and deploys the website.

## Project Structure

```
osws-scientific-report/
├── notebooks/           # Jupyter Notebooks
├── reports/            # Generated Reports
├── assets/
│   ├── css/           # Custom Styles
│   ├── csl/           # Citation Styles
│   └── images/        # Logos and Graphics
├── downloads/          # PDF/LaTeX/Word Downloads
├── scripts/           # Helper Scripts
├── _quarto-profiles/  # Journal-specific Formats
├── .github/workflows/ # GitHub Actions
└── references.bib     # Bibliography
```

## Technologies

- **Quarto** - Publishing System
- **Python** - Data Analysis
- **GitHub Actions** - CI/CD
- **TinyTeX** - LaTeX/PDF Generation

## Documentation

- [Guide](https://werzingerma.github.io/osws-scientific-report/guide.html) - Setup & Usage
- [Workflow](https://werzingerma.github.io/osws-scientific-report/workflow.html) - Process Overview
- [Reports](https://werzingerma.github.io/osws-scientific-report/reports/) - All Reports
