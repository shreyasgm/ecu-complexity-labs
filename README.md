# ECU Summer School of Economic Complexity: Applied Labs

Notebooks for the afternoon applied sessions of the ECU Summer School of Economic Complexity (UM6P Rabat, 6 to 10 July 2026).

## Working in Google Colab

Open a notebook from the table below and save your own copy right away (File menu, then "Save a copy in Drive"), because Colab discards its session when it closes and your work would go with it. Each notebook downloads the data it needs on its first run.

| Notebook | What it is | Open |
|---|---|---|
| Day 1 workbook | The notebook you fill in during the Day 1 session | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyasgm/ecu-complexity-labs/blob/main/day1/day1_workbook.ipynb) |
| Day 1 reference, student edition | The same analysis with the figures shown and the answer code blanked, in case you fall behind during the session | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyasgm/ecu-complexity-labs/blob/main/day1/day1_reference_student.ipynb) |
| Day 1 reference, full | The worked answers, posted once the session is over | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyasgm/ecu-complexity-labs/blob/main/day1/day1_reference.ipynb) |
| Day 2 workbook | The notebook you fill in during the Day 2 session | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyasgm/ecu-complexity-labs/blob/main/day2/day2_workbook.ipynb) |
| Day 2 reference, student edition | The Day 2 analysis with the figures shown and the answer code blanked | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyasgm/ecu-complexity-labs/blob/main/day2/day2_reference_student.ipynb) |
| Day 3 workbook | The notebook you fill in during the Day 3 session | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyasgm/ecu-complexity-labs/blob/main/day3/day3_workbook.ipynb) |
| Day 3 reference, student edition | The Day 3 analysis with the figures and tables shown and the answer code blanked | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyasgm/ecu-complexity-labs/blob/main/day3/day3_reference_student.ipynb) |
| Day 1 in R | The Day 1 analysis in R with the economiccomplexity package, already executed with all results shown | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyasgm/ecu-complexity-labs/blob/main/day1/day1_reference_r.ipynb) |
| Day 2 in R | The Day 2 analysis in R, already executed with all results shown | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyasgm/ecu-complexity-labs/blob/main/day2/day2_reference_r.ipynb) |
| Day 3 in R | The Day 3 analysis in R, already executed with all results shown | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyasgm/ecu-complexity-labs/blob/main/day3/day3_reference_r.ipynb) |
| Python warm-up | A short primer on the pandas basics the labs rely on | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyasgm/ecu-complexity-labs/blob/main/primers/primer_python.ipynb) |
| R warm-up | A short primer on the tidyverse basics | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyasgm/ecu-complexity-labs/blob/main/primers/primer_r.ipynb) |

The R warm-up opens in Colab's R runtime, which already has the tidyverse installed.

## The R companions

The "in R" notebooks in the table repeat each day's analysis with the economiccomplexity package (Day 3 adds fixest for the regressions and modelsummary for the tables), so R users can check that the packages reproduce the same numbers. They open in Colab's R runtime already executed, with every output and figure in place, so you can read them without running anything. If you do want to run one, its first cell installs the missing packages from Posit's prebuilt binary mirror (about a minute, instead of the very slow compile-from-source that plain `install.packages()` triggers on Colab) and downloads the data from the release, the same way the Python notebooks do. Each day's folder also carries an `.html` copy that opens in any browser with no setup at all.

## The data

The notebooks fetch their data from this repository's [data release](https://github.com/shreyasgm/ecu-complexity-labs/releases/tag/data-v1). To get the files yourself, download the zips from that release and unzip them into a folder named `morocco_data_packet` next to the notebook. Days 1 to 3 use `exports.zip` and `reference.zip`, and the remaining archives come up later in the week. The product-space layout files were added to `reference.zip` on the morning of 7 July, so a packet downloaded before then should be deleted and fetched again. The Moroccan regional employment data (CNSS) is not public and reaches participants separately within the program.

The country-level data comes from the Innovation Capabilities Outlook 2026 Dataset, published by the World Intellectual Property Organization under a CC BY 4.0 license: WIPO (2026), Innovation Capabilities Outlook 2026 Dataset, https://doi.org/10.34667/tind.59177. The exports dimension builds on the Growth Lab at Harvard University's International Trade Data (HS92), https://doi.org/10.7910/DVN/T4CHWJ. Every folder in each packet carries a `CITATION.txt` with the full attribution for its source.

## Running locally instead

Clone this repository and run `uv sync` ([install uv](https://docs.astral.sh/uv/getting-started/installation/) first if you do not have it). That builds a virtual environment in `.venv/` with every package the course uses, pinned to the versions in `uv.lock`, including the development branch of the Growth Lab's [py-ecomplexity](https://github.com/harvard-growth-lab/py-ecomplexity) that the Day 2 notebook relies on. Add `--extra geo` for the geospatial packages used later in the week. Then `uv run jupyter lab` opens the notebooks. The data downloads work the same way on a local machine, and the `.html` reference copies open in any browser with no setup at all.
