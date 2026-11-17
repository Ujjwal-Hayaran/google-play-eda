# App Insights Unlocked: Google Play Store EDA

> What makes an Android app successful? A Python exploratory data analysis of **9,659 unique Google Play apps** and **35,929 user reviews**, answering 25 business questions and ending in stakeholder recommendations.

**Tools:** Python, pandas, NumPy, SciPy, Matplotlib, Seaborn, scikit-learn, Jupyter

## Headline findings
| Finding | Evidence |
|---|---|
| Typical quality bar is high | Mean rating **4.17**, median 4.3; 77% of rated apps are 4.0+ |
| Popularity and rating are different things | Installs vs rating Spearman **0.03**; yet rating spread shrinks from std 0.86 (<1K installs) to 0.19 (100M+) |
| Fresh apps win | Updated within 30 days: median **1M** installs vs **10K** for apps untouched >1 year |
| Demand is concentrated | 5 categories hold **59%** of installs: Game, Communication, Tools, Family, Productivity |
| Users punish unreliability | Bugs/crashes 1.6x and login/sync issues 2.0x more frequent in low-rated apps' reviews |
| Paid apps rate higher, but price hurts within paid | Paid 4.26 vs free 4.17; within paid Spearman -0.10 |

## Deliverables
| # | File | Contents |
|---|---|---|
| 1 | [`deliverables/1_Case_Study_Document.docx`](deliverables/1_Case_Study_Document.docx) | Problem statement, stakeholders, data dictionary, 25 questions |
| 2 | [`deliverables/2_Solution_Guide.docx`](deliverables/2_Solution_Guide.docx) | Worked answers, code, charts, recommendations |
| 3 | [`deliverables/3_Additional_Resources.docx`](deliverables/3_Additional_Resources.docx) / [`.md`](deliverables/3_Additional_Resources.md) | References for further exploration |
| + | [`notebooks/App_Insights_EDA.ipynb`](notebooks/App_Insights_EDA.ipynb) | Executed end-to-end notebook ([HTML export](reports/App_Insights_EDA.html)) |

## Data cleaning highlights
- Dropped 1 column-shifted corrupt row, 483 exact duplicates and 698 repeated app listings (kept the row with most reviews): 10,841 -> 9,659 apps.
- Converted Installs / Price / Size / dates; **did not impute** missing ratings (they belong to tiny apps).
- Documented limits: installs are buckets, one update date per app (so true update intervals are not computable), single mid-2018 snapshot.

## Repository structure
```
data/raw/            original CSVs + licence
data/processed/      cleaned dataset
notebooks/           executed, beginner-style Jupyter notebook (the main analysis)
src/                 notebook source, generate_report_numbers.py + Word document builders
reports/figures/     25 charts (PNG)     reports/tables/   result tables (CSV)
reports/results.json every number quoted in the documents
deliverables/        the three Word deliverables
```

## Reproduce
```bash
pip install -r requirements.txt
python src/make_notebook.py src/notebook_source.py notebooks/App_Insights_EDA.ipynb   # optional: rebuild notebook from its source
jupyter nbconvert --to notebook --execute --inplace notebooks/App_Insights_EDA.ipynb
python src/generate_report_numbers.py   # numbers + charts used by the Word documents
python src/build_case_study.py && python src/build_solution_guide.py && python src/build_resources.py
```

## Attribution
Data: *Google Play Store Apps* by Lavanya Gupta on Kaggle, licensed [CC BY 3.0](http://creativecommons.org/licenses/by/3.0/) (see `DATA_LICENSE.txt`). Add a code licence of your choice (e.g. MIT).
