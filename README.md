## master-thesis-political-microtargeting
In this repository I am going to publish the code that I have used to get the figures for my master thesis. 

## Abstract

Political microtargeting (PMT) has become a key instrument in modern election campaigns, enabling political actors to use personal data for individually tailored messages. While this practice can enhance outreach, it also raises serious concerns about privacy, transparency, and the integrity of democratic processes. Therefore, his thesis asks if current EU regulations on political microtargeting are sufficient to prevent unlawful political influence and safeguard democratic integrity.
The study first examines the role of the General Data Protection Regulation (GDPR) as the EU’s most comprehensive framework for data protection, identifying both its strengths and gaps. Additional regulatory instruments are analysed to assess whether they close these gaps or leave room for exploitation. The risks posed by predictive analytics, profiling, and behavioural targeting are then linked to wider democratic concerns such as manipulation, echo chambers, and information asymmetry.
A case study of Die Linke in the 2025 German federal election, based on Meta Ad Library data, demonstrates how even smaller parties can leverage PMT strategically to influence electoral outcomes. Finally, recent CJEU rulings and pending litigation are discussed as corrective mechanisms, though they remain reactive and fragmented.
The thesis concludes that existing regulation is insufficient, and that democracy requires a purpose-driven framework addressing not only data collection but also its political uses.

## Folder structure
```
thesis-graphs/
├─ notebook/
│  └─ meta_ad_library_research_clean.ipynb  # main notebook
├─ outputs/      # created automatically when you run the notebook (not in repo)
├─ requirements.txt
└─ README.md
```
- notebook/ → contains the Jupyter Notebook with all analysis and plots
- outputs/ → created automatically when the notebook runs; contains all exported CSVs and figures (you can open CSVs in Excel)

## Setup (optional for advanced users)

If you want to run the notebook in a Python environment yourself:
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

All data used for the analysis is publicly available:

Meta Ad Library (Facebook/Instagram ads):
https://www.facebook.com/ads/library/

Official election results (2025 German federal election):
https://bundeswahlleiterin.de/bundestagswahlen/2025/ergebnisse.html

# How to prepare
Download the two CSV files from the links above.
meta_ad_library.csv
election_results.csv

Save them anywhere on your computer (e.g. Downloads folder).

Open the notebook and paste the full paths into the two boxes at the top.

Example:

META_ADS_PATH = r"C:\Users\Name\Downloads\meta_ad_library.csv"

ELECTIONS_PATH = r"/Users/name/Downloads/election_results.csv"

## Run the notebook
1. Launch Jupyter:

   jupyter lab
   (or jupyter notebook)

3. Open:

   notebook/meta_ad_library_research_clean.ipynb

5. In the very first cell, paste the full paths to the two downloaded CSV files.

6. Run all cells (Kernel → Restart & Run All).

7. You’ll see:

   Figures and statistics directly in the notebook
   CSVs and plots saved under the outputs/ folder (next to the notebook).

## Reproducibility notes
- No desktop-specific paths remain.
- The notebook works entirely with the two input files provided by the user.
- Outputs are automatically placed into the outputs/ folder for clarity.

