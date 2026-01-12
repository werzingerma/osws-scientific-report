# PRECISION Scientific Reports

Automated workflow for scientific reports with Quarto and GitHub Pages.

## Features

- **Jupyter Notebooks** → automatic conversion to HTML/PDF/LaTeX/Word
- **GitHub Actions** - Fully automated deployment
- **Journal Profiles** for Springer, Elsevier, Nature, Lancet
- **Citation Management** with BibTeX and multiple CSL styles
- **Zotero Integration** for reference management
- **Responsive Design** with custom PRECISION theme
- **Automatic Downloads Generation** (PDF, LaTeX+images ZIP, Word)

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
│   ├── latex/         # LaTeX Templates
│   └── images/        # Logos and Graphics
├── downloads/          # PDF/LaTeX/Word Downloads
├── scripts/           # Helper Scripts
├── _quarto-profiles/  # Journal-specific Formats
├── .github/workflows/ # GitHub Actions
└── references.bib     # Central Bibliography
```

## Journal Profiles

Pre-configured PDF formats for scientific journals. Use with:

```bash
quarto render notebooks/my-analysis.ipynb --profile springer
```

| Profile | Command | Features |
|---------|---------|----------|
| Springer | `--profile springer` | 1.5x line spacing, numbered sections |
| Elsevier | `--profile elsevier` | Double spacing, line numbers |
| Nature | `--profile nature` | Sans-serif font, no section numbers |
| Lancet | `--profile lancet` | Times font, line numbers, Vancouver style |

**Sources:**
- Springer Author Guidelines: [springer.com/gp/authors-editors](https://www.springer.com/gp/authors-editors/journal-author/journal-author-helpdesk/manuscript-preparation/1260)
- Elsevier Author Guidelines: [elsevier.com/authors](https://www.elsevier.com/authors/policies-and-guidelines)
- Nature Formatting Guide: [nature.com/nature/for-authors](https://www.nature.com/nature/for-authors/formatting-guide)
- Lancet Information for Authors: [thelancet.com/for-authors](https://www.thelancet.com/pb/assets/raw/Lancet/authors/tl-info-for-authors.pdf)

## Citations

Use `@citekey` syntax in Markdown cells to cite references from `references.bib`:

```markdown
The method was validated by @smith2020.
Multiple studies confirm this [@jones2019; @miller2021].
```

Available citation styles (CSL files from [Zotero Style Repository](https://www.zotero.org/styles)):

| Style | File | Use Case |
|-------|------|----------|
| APA 7th | `apa-7th-edition.csl` | Psychology, Social Sciences |
| Vancouver | `vancouver.csl` | Medicine, Biomedicine |
| Nature | `nature.csl` | Nature journals |
| Springer | `springer-basic-author-date.csl` | Springer Nature |
| Elsevier Harvard | `elsevier-harvard.csl` | Elsevier journals |
| Lancet | `the-lancet.csl` | Lancet journals |

**Documentation:** [Quarto Citations](https://quarto.org/docs/authoring/citations.html)

## Technologies

- **[Quarto](https://quarto.org/)** - Publishing System
- **[Python](https://www.python.org/)** - Data Analysis
- **[GitHub Actions](https://github.com/features/actions)** - CI/CD
- **[TinyTeX](https://yihui.org/tinytex/)** - LaTeX/PDF Generation

## Documentation

- [Guide](https://werzingerma.github.io/osws-scientific-report/guide.html) - Setup & Usage
- [Workflow](https://werzingerma.github.io/osws-scientific-report/workflow.html) - Process Overview
- [Reports](https://werzingerma.github.io/osws-scientific-report/reports/) - All Reports
- [Downloads](https://werzingerma.github.io/osws-scientific-report/reports/downloads.html) - PDF/LaTeX/Word

## License

MIT License - see [LICENSE](LICENSE) for details.
