# HateXplain Analysis

An exploratory analysis of hate speech, offensive language, and normal-language comments using a processed version of the [HateXplain dataset](https://github.com/hate-alert/HateXplain). This project examines label balance, demographic target distributions, comment length, and emoji usage across 20,109 comments.

> **Content warning:** The dataset and analysis contain examples and aggregate statistics related to hateful and offensive language.

## Project overview

The analysis focuses on three questions:

1. How are `hatespeech`, `offensive`, and `normal` comments distributed?
2. Which demographic groups are identified as targets, and how do label proportions vary across those groups?
3. Do basic linguistic features, such as comment length and emoji presence, differ by label?

Target categories include race, religion, gender, sexual orientation, and miscellaneous groups.

## Dataset

The processed dataset contains 20,109 rows and seven columns:

| Column | Description |
| --- | --- |
| `comment` | Comment text |
| `label` | `hatespeech`, `offensive`, or `normal` |
| `Race` | Racial or ethnic target category |
| `Religion` | Religious target category |
| `Gender` | Gender target category |
| `Sexual Orientation` | Sexual-orientation target category |
| `Miscellaneous` | Other target categories |

The dataset is derived from HateXplain. See the [original repository](https://github.com/hate-alert/HateXplain) for the source dataset, documentation, and citation information.

## Analysis

The notebook covers:

- Dataset structure and missing-value checks
- Demographic target frequencies
- Comments with no specific demographic target
- Label distributions among targeted comments
- Label proportions within each target subgroup
- Comment-length statistics by label
- Emoji-presence statistics by label

Selected observations from the notebook:

- 7,629 comments (37.94%) have no specific target across race, religion, gender, and sexual orientation.
- Among the 12,480 comments with a specific target, 6,234 are labeled hate speech, 4,301 offensive, and 1,945 normal.
- Hate-speech comments have the highest average character length among the three labels in this processed dataset.

## Repository contents

| File | Description |
| --- | --- |
| [`detection.ipynb`](detection.ipynb) | Main Jupyter notebook with analysis, tables, and visualizations |
| [`final_hateXplain.csv`](final_hateXplain.csv) | Processed dataset used by the notebook |
| [`1_dataset_info.txt`](1_dataset_info.txt) | Dataset dimensions, column types, and missing-value summary |
| [`Jiyoo_Lee_Honors_Project_DAT301.pdf`](Jiyoo_Lee_Honors_Project_DAT301.pdf) | Final project report |

## Running the notebook

Python 3 and Jupyter are required. Install the analysis dependencies:

```bash
python3 -m pip install pandas matplotlib seaborn jupyter
```

Then launch Jupyter from the repository directory:

```bash
jupyter notebook detection.ipynb
```

The notebook reads `final_hateXplain.csv` using a relative path, so keep the CSV and notebook in the same directory.

## Tools

- Python
- pandas
- Matplotlib
- seaborn
- Jupyter Notebook

## Author

Jiyoo Lee  
DAT 301 Honors Project
