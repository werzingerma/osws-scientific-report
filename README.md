# PRECISION Scientific Reports

Automatisierter Workflow für wissenschaftliche Berichte mit Quarto und GitHub Pages.

## Features

- 📊 **Jupyter Notebooks** → automatische Konvertierung zu HTML/PDF/LaTeX/Word
- 🚀 **GitHub Actions** - Vollautomatisches Deployment
- 📚 **Journal-Profile** für Springer, Elsevier, Nature, Lancet
- 📖 **Zotero-Integration** für Literaturverwaltung
- 🎨 **Responsive Design** mit Custom PRECISION Theme
- 🔄 **Automatische Downloads-Generierung**

## Quick Start

```bash
# 1. Repository klonen
git clone https://github.com/werzingerma/osws-scientific-report.git
cd osws-scientific-report

# 2. Python-Umgebung einrichten
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt

# 3. Notebook erstellen
# - Erstelle ein Jupyter Notebook in notebooks/
# - Führe alle Zellen aus
# - Füge YAML-Header in Raw-Zelle hinzu

# 4. Pushen - fertig!
git add .
git commit -m "Add: Neuer Bericht"
git push
```

GitHub Actions generiert automatisch alle Formate (HTML, PDF, LaTeX, Word) und deployed die Website.

## Projekt-Struktur

```
osws-scientific-report/
├── notebooks/           # Jupyter Notebooks
├── reports/            # Generierte Reports
├── assets/             
│   ├── css/           # Custom Styles
│   ├── csl/           # Citation Styles
│   └── images/        # Logos und Grafiken
├── downloads/          # PDF/LaTeX/Word Downloads
├── scripts/           # Helper Scripts
├── _quarto-profiles/  # Journal-spezifische Formate
├── .github/workflows/ # GitHub Actions
└── references.bib     # Bibliographie
```

## Technologien

- **Quarto** - Publishing System
- **Python** - Data Analysis
- **GitHub Actions** - CI/CD
- **TinyTeX** - LaTeX/PDF Generation
- **Bootstrap** - UI Framework

## Dokumentation

- [Anleitung](https://werzingerma.github.io/osws-scientific-report/guide.html) - Setup & Nutzung
- [Workflow](https://werzingerma.github.io/osws-scientific-report/workflow.html) - Prozess-Übersicht
- [Berichte](https://werzingerma.github.io/osws-scientific-report/reports/) - Alle Reports

## Lizenz

MIT License - Siehe LICENSE Datei
