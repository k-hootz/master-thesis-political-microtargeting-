## master-thesis-political-microtargeting-
In this repository I am going to publish the code that I have used to get the figures for my master thesis. 

## Abstract

Political microtargeting (PMT) has become a key instrument in modern election campaigns, enabling political actors to use personal data for individually tailored messages. While this practice can enhance outreach, it also raises serious concerns about privacy, transparency, and the integrity of democratic processes. Therefore, his thesis asks if current EU regulations on political microtargeting are sufficient to prevent unlawful political influence and safeguard democratic integrity.
The study first examines the role of the General Data Protection Regulation (GDPR) as the EU’s most comprehensive framework for data protection, identifying both its strengths and gaps. Additional regulatory instruments are analysed to assess whether they close these gaps or leave room for exploitation. The risks posed by predictive analytics, profiling, and behavioural targeting are then linked to wider democratic concerns such as manipulation, echo chambers, and information asymmetry.
A case study of Die Linke in the 2025 German federal election, based on Meta Ad Library data, demonstrates how even smaller parties can leverage PMT strategically to influence electoral outcomes. Finally, recent CJEU rulings and pending litigation are discussed as corrective mechanisms, though they remain reactive and fragmented.
The thesis concludes that existing regulation is insufficient, and that democracy requires a purpose-driven framework addressing not only data collection but also its political uses.

## Folder structure
```
thesis-graphs/
├─ notebook/                # notebooks
├─ data/                    # input CSVs (committed)
├─ outputs/                 # exports (gitignored)
├─ figures/                 # saved images (gitignored)
├─ requirements.txt
└─ README.md
```

## Quickstart

Using **pip**:
```bash
python -m venv .venv
source .venv/bin/activate  # on Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

Or with **conda**:
```bash
conda create -n thesis-graphs python=3.11
conda activate thesis-graphs
pip install -r requirements.txt
```

## Data

All data used for the analysis is publicly available.

Data on political ads on Facebook and Instagram is available via the Meta Ad Library: https://www.facebook.com/ads/library/

Data on voters results in the 2025 German federal election is available via : https://bundeswahlleiterin.de/bundestagswahlen/2025/ergebnisse.html

- `data/meta-ad-library.csv` — exported from Meta Ad Library.
- `data/election-results.csv` — official election results CSV (contains a few metadata lines at the top which the notebook handles).

These two sample files are included here so the notebook runs out of the box.

## Run the notebook
1. Launch Jupyter:
   ```bash
   python -m jupyter lab
   ```
2. Open `notebook/9a2d2d76-1a07-4fd7-8280-fd12d1e718ff_github_ready_clean.ipynb`.
3. Run all cells.

## Reproducibility notes
- The notebook uses **relative paths** via `DATA_DIR`, `OUT_DIR`, and `FIG_DIR`.
- Outputs (CSVs, figures) are written to `outputs/` or `figures/` and are ignored by git.
- No desktop-specific paths remain.

