# Are home buyers inattentive towards energy efficiency?

**An empirical project conducted as part of a Master's thesis in Applied Economics and Data Science.**


[![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![R](https://img.shields.io/badge/R-4.x-276DC3?style=for-the-badge&logo=r&logoColor=white)](https://www.r-project.org/)
[![Quarto](https://img.shields.io/badge/Quarto-1.x-39729E?style=for-the-badge&logo=quarto&logoColor=white)](https://quarto.org/)

<br>

<!-- button to the sitee -->
<p align="center">
  <a href="https://valdikaldi.github.io/Website_Modelling_HousingPrice_EnergyEfficiency/">
    <img src="https://img.shields.io/badge/View_Site-2f6f5e?style=for-the-badge&labelColor=1f4d40&logo=readthedocs&logoColor=white" alt="View Site" width="200">
  </a>
</p>
 
## Overview

This project examines whether Danish private property buyers are price-sensitive to the energy class of a property and to specific energy-related components.

To answer this question, a new dataset is constructed by:

- **Web scraping** 2,295,344 property transactions and characteristics of Danish properties.
- **Extracting information** from 776,108 PDF documents from Energy Performance Certificates (EPC), using binary text classification models alongside NLP and OCR techniques.

The extracted data cover prices, energy efficiency, and other property characteristics. The analysis is presented on a website built with Quarto.

---

## Website

The full analysis, data pipeline, and thesis chapters are available on the project site:

**[valdikaldi.github.io/Website_Modelling_HousingPrice_EnergyEfficiency](https://valdikaldi.github.io/Website_Modelling_HousingPrice_EnergyEfficiency/)**

The site is organised as a Quarto book and includes:

| Section | Description |
|---|---|
| **Welcome** | Project overview, research context, contributions, and thesis roadmap. |
| **1. Introduction** | Motivation, research question, and contributions of the thesis. |
| **2. EPBD and the Danish EPC scheme** | Policy background and structure of the EPC reports. |
| **3. Literature review** | Related literature on energy efficiency and property prices. |
| **4. Data** | Data sources, scraping pipeline, PDF extraction, and geo-data. |
| **5. Empirical strategy** | Hedonic model and estimation strategy. |
| **6. Results** | Main results, market segments, policy effects, and robustness tests. |
| **7. Discussion** | Interpretation, limitations, and policy implications. |
| **Appendix & References** | Supporting material and bibliography. |

---

## Project structure

```
.
├── _quarto.yml             # -> Quarto book configuration
├── index.qmd               # -> Front page
├── quarto_files/           # -> Thesis chapters
├── styles/                 # -> Stylesheets (site-wide and front page)
├── data/tables/appendix/   # -> CSV sources for appendix tables
├── assets/                 # ->  Branding, icons, cover image
├── references.bib          # -> Bibliography 
├── apa.csl                 # -> APA citation style
├── renv.lock               # -> Pinned R package versions
└── docs/                   # ->  Rendered site (GitHub Pages output)
```

---

## Methods and tools

### Languages

| Language | Purpose |
|---|---|
| **Python** | Data cleaning and pre-processing, web scraping, PDF parsing, NLP text classification, OCR, geographical data extraction. |
| **R** | Data visualisation and regression modelling. |

### Libraries

**Python** — `Requests`, `Concurrent.futures`, `pdfplumber`, `PyMuPDF`, `NLTK`, `spaCy`, `scikit-learn`, `imbalanced-learn`, `gensim`, `FastText`, `Pillow`, `pytesseract`, and Python's built-in `re` module.

**Geospatial** — `Valhalla` routing engine (Docker), `Geofabrik` (Denmark extract).

**R** — `fixest`, `sandwich`, `modelsummary`.

---

## Reproducing the site

### Requirements

- [Quarto](https://quarto.org/) ≥ 1.4
- Python 3.x (only if re-running the data pipeline)
- R 4.x with the packages listed above (only if re-running the regression analysis)

### Build locally

```bash
git clone https://github.com/valdikaldi/Empirical_Project-are_home_buyers_inattentive_towards_energy_efficiency.git
cd Empirical_Project-are_home_buyers_inattentive_towards_energy_efficiency
quarto render
```

The rendered site is written to `docs/`. To preview with live reload:

```bash
quarto preview
```

### Publish

The site is published via GitHub Pages from the `gh-pages` branch. 
---

## Author

**Valdimar Einarsson**
Master's thesis, Applied Economics and Data Science

---

## License

© Valdimar Einarsson, 2024. Distributed under a CC-BY license unless otherwise stated.

---

## Acknowledgements

Built with [Quarto](https://quarto.org/). Data obtained from [boliga.dk](https://www.boliga.dk/) and [boligejer.dk](https://boligejer.dk/). Geospatial data from [Geofabrik](https://download.geofabrik.de/europe/denmark.html).
