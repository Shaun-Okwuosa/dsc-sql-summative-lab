# SQL Summative Lab

A two-part SQL assessment: guided querying and visualization of a wholesale
customer/sales database, followed by an open-ended exploratory analysis of
an IMDb movie dataset.

## Contents

| File / Folder              | Description                                                                                                     |
| -------------------------- | --------------------------------------------------------------------------------------------------------------- |
| `SQLSummativeLab.ipynb`    | Main notebook — all SQL queries, visualizations, and written reflections for Parts 1 and 2                      |
| `Presentation Slides.pptx` | Short slide deck summarizing the Part 2 exploratory analysis (findings, business question, data cleaning tasks) |
| `data.sqlite`              | Customer/sales database used in Part 1                                                                          |
| `im.db.zip`                | Zipped IMDb movie database used in Part 2                                                                       |
| `images/`                  | ERD diagrams and supporting images referenced in the notebook                                                   |

## Part 1: Customer Database

Guided SQL queries against `data.sqlite` covering customer segmentation,
credit limit analysis by state, top customers by payment volume, product
purchase thresholds, product line performance, and remote office staffing —
each paired with the relevant business context and, where required, a
matplotlib/seaborn visualization.

## Part 2: Exploratory Analysis (IMDb)

Open-ended exploration of a separate movie database (`im.db`), covering
initial trends across genres, ratings, and release years; a business
question investigating whether creative team size (directors/writers)
relates to average rating; and a list of data cleaning tasks identified
along the way. Findings are summarized in `Presentation Slides.pptx`.

## A Note on the Part 2 Database

`im.db` (the unzipped SQLite database used in Part 2) is **not** committed
to this repo — it's too large to push. Only the zipped version,
`im.db.zip`, is tracked.

The notebook handles this automatically: the first code cell in Part 2
unzips `im.db.zip` into `im.db` in the working directory before connecting
to it. As long as `im.db.zip` stays in the same folder as the notebook,
running the notebook top to bottom will regenerate `im.db` locally — no
manual extraction needed.

`im.db` is listed in `.gitignore` so it won't accidentally get committed
after that extraction happens.

## Setup

1. Clone the repo.
2. Install dependencies:
   ```
   pip install pandas numpy matplotlib seaborn
   ```
   (`sqlite3` ships with the Python standard library.)
3. Open `SQLSummativeLab.ipynb` and run all cells in order. `data.sqlite`
   connects directly; `im.db.zip` is extracted to `im.db` automatically
   partway through Part 2.
