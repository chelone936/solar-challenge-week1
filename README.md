# Solar Challenge — Week 1

Overview
--------
This repository contains data cleaning, exploratory analysis notebooks, and helper code for the Solar Challenge Week 1 deliverables. It includes per-site EDA notebooks, cleaned CSV datasets, basic scripts, and CI workflows.

Quickstart
----------
1. Clone the repository:
   ```bash
   git clone https://github.com/chelone936/solar-challenge-week1.git
   cd solar-challenge-week1
   ```
2. Create & activate a Python virtual environment and install dependencies:
   ```bash
   python -m venv venv
   # Windows
   venv\Scripts\activate
   # macOS / Linux
   source venv/bin/activate

   pip install -r requirements.txt
   ```
   See: requirements.txt

3. Run notebooks
   - Start Jupyter and open the notebooks in the notebooks/ folder.
   ```bash
   jupyter notebook
   ```
   Notebooks perform cleaning, EDA and comparison across sites:
   - benin_eda.ipynb
   - sierraleone_eda.ipynb
   - togo_eda.ipynb
   - compare_countries.ipynb

Repository layout
----------------
Top-level:
- .gitignore
- README.md (this file)
- requirements.txt
- ci.yml
- .github/workflows/unittests.yml

Code & helpers:
- app/__init__.py
- src/__init__.py
- scripts/__init__.py
- README.md
- tests/__init__.py

Notebooks:
- README.md
- benin_eda.ipynb
- sierraleone_eda.ipynb
- togo_eda.ipynb
- compare_countries.ipynb

Data (CSV):
- data/benin_clean.csv
- data/benin-malanville.csv
- data/sierraleone_clean.csv
- data/sierraleone-bumbuna.csv
- data/togo_clean.csv
- togo-dapaong_qc.csv

The cleaned versions will be avaliable after executing the respective notebooks.

What you'll find inside
-----------------------
- Notebooks perform:
  - Parsing timestamps, dropping unused columns (e.g., `Comments`)
  - Summary statistics and missing/mask reporting
  - Z-score based outlier detection and basic cleaning
  - Visualizations (histograms, correlation heatmaps, wind-direction summaries)
  - Per-site EDA and a cross-country comparison notebook
  Examples of these steps are implemented in the notebooks like benin_eda.ipynb.

CI / Tests
----------
- GitHub Actions workflow for CI: ci.yml
- Unit test workflow: .github/workflows/unittests.yml
- To run tests locally (if tests are added), a typical command is:
  ```bash
  pytest
  ```

Data notes
----------
- Each CSV contains one year of minute-resolution site data (525,600 rows).
- Typical columns across datasets: Timestamp, GHI, DNI, DHI, ModA, ModB, Tamb, RH, WS, WSgust, WSstdev, WD, WDstdev, BP, Cleaning, Precipitation, TModA, TModB, Comments.
- Example: togo-dapaong_qc.csv

Contributing
------------
- Use the existing notebook templates for new analyses and push changes via PR.
- Keep large binary files and raw data out of the repo (see .gitignore).

Contact / Next steps
--------------------
- Add unit tests under tests/ for any utility functions placed in src/ or scripts/.
- Optionally add a Streamlit app (requirements already include `streamlit`) inside app/ to showcase results.

Files (quick links)
-------------------
- .gitignore
- README.md
- requirements.txt
- ci.yml
- .github/workflows/unittests.yml
- app/__init__.py
- data/benin_clean.csv
- data/benin-malanville.csv
- data/sierraleone_clean.csv
- data/sierraleone-bumbuna.csv
- data/togo_clean.csv
- togo-dapaong_qc.csv
- notebooks/__init__.py
- benin_eda.ipynb
- compare_countries.ipynb
- README.md
- sierraleone_eda.ipynb
- togo_eda.ipynb
- scripts/__init__.py
- README.md
- src/__init__.py
- tests/__init__.py

License
-------
No license file included. Add a LICENSE if you plan to publish or share widely.

