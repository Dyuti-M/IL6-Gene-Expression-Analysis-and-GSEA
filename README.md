# IL6-Gene-Expression-Analysis-and-GSEA
This project analyzes gene expression datasets from the Gene Expression Omnibus (GEO) database to identify and quantify Interleukin-6 (IL-6) expression. It then uses this data to perform Gene Set Enrichment Analysis (GSEA) on samples with the highest and lowest IL-6 expression levels to discover associated biological pathways.

Key Features
Automated Data Fetching: Automatically downloads and processes multiple GEO datasets (.tar.gz files).

IL-6 Expression Extraction: Identifies and extracts IL-6 expression data from different platforms and datasets.

Robust Data Cleaning: Handles missing values, performs numeric validation, and standardizes data across various studies.

Gender Inference: Infers the sex of samples where metadata is unavailable based on XIST and KDM5D gene expression (for specific datasets like GSE2164).

IL-6 Extremes Analysis: Identifies samples in the top and bottom quartiles of IL-6 expression.

GSEA Integration: Runs GSEA using the gseapy library to find pathways correlated with high vs. low IL-6 expression.

Automated Visualization: Generates and saves plots showing IL-6 expression distribution and values across datasets.

Prerequisites
To run this analysis, you need to have Python installed along with the following packages. You can install them using pip:

pip install pandas gseapy tqdm Biopython geosketch numpy seaborn matplotlib


How to Run the Analysis
Save the Code: Save the IL6Analyzer class code into a Python file (e.g., run_analysis.py).

Run the Script: Simply execute the file from your terminal. The script will automatically download the required data and perform the analysis.

python run_analysis.py


Output Structure
The script will create a new directory named il6_analysis_results in the same location as the script. This directory will contain all of the output files.

il6_analysis_results/
├── gsea_results/
│   ├── GSE28146/
│   │   ├── gsea.reports.geneset.high_il6.na.run1.html
│   │   └── ... (GSEA reports for high and low IL-6 groups)
│   └── GSE2164/
│       ├── gsea.reports.geneset.high_il6.na.run1.html
│       └── ...
├── il6_expression_distribution.png
└── il6_expression_by_dataset.png


Contact
For questions or feedback, please contact Dyuti at dyutim80@gmail.com.

License
This project is licensed under the MIT License - see the LICENSE file for details.
