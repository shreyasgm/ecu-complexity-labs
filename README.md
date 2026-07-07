# ECU Summer School of Economic Complexity: Applied Labs

Notebooks for the afternoon applied sessions of the ECU Summer School of Economic Complexity (UM6P Rabat, 6 to 10 July 2026).

## Work in Google Colab

Open a notebook with its badge below, then save your own copy right away: open the File menu and choose "Save a copy in Drive". Colab discards its session when it closes, and without your own copy your work goes with it. The notebooks download the data they need on first run, so there is nothing to install or upload.

| Notebook | What it is | Open |
|---|---|---|
| Day 1 workbook | The hands-on copy you fill in during the session | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyasgm/ecu-complexity-labs/blob/main/day1/day1_workbook.ipynb) |
| Day 1 reference, student edition | Shows what each step produces, with the answer code blanked | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyasgm/ecu-complexity-labs/blob/main/day1/day1_reference_student.ipynb) |
| Day 1 reference, full | Every answer worked, shared after the session | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyasgm/ecu-complexity-labs/blob/main/day1/day1_reference.ipynb) |
| Python warm-up | Pre-session primer on the pandas basics the labs use | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyasgm/ecu-complexity-labs/blob/main/primers/primer_python.ipynb) |
| R warm-up | Pre-session primer on the tidyverse basics | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyasgm/ecu-complexity-labs/blob/main/primers/primer_r.ipynb) |

The R warm-up opens in Colab's R runtime, which already has the tidyverse installed.

## The R companion for Day 1

`day1/day1_reference_r.ipynb` repeats the Day 1 analysis in R with the economiccomplexity package, so R users can see that the package reproduces the hand-rolled numbers. It is a read-along companion: view it here on GitHub or through the `.html` copy rather than running it on Colab, since it expects the packages and data paths of a local setup.

## The data

The Day 1 notebook downloads its data automatically from this repository's [data release](https://github.com/shreyasgm/ecu-complexity-labs/releases/tag/data-v1). To get the files yourself, download `exports.zip` and `reference.zip` from that release and unzip them into a folder named `morocco_data_packet` next to the notebook.

The data comes from the Innovation Capabilities Outlook 2026 Dataset, published by the World Intellectual Property Organization under a CC BY 4.0 license: WIPO (2026), Innovation Capabilities Outlook 2026 Dataset, https://doi.org/10.34667/tind.59177. The exports dimension builds on the Growth Lab at Harvard University's International Trade Data (HS92), https://doi.org/10.7910/DVN/T4CHWJ. Every folder in the packet carries a `CITATION.txt` with the full attribution for its dimension.

## Running locally instead

Clone this repository and open the notebooks in Jupyter with Python 3.12 or later and the packages pandas, numpy, scipy, matplotlib, and plotly installed. The data download works the same way on a local machine, and the `.html` copies of the reference notebooks open in any browser with no setup at all.
