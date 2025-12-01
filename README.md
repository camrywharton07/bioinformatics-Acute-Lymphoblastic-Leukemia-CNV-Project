## bioinformatics-Acute-Lymphoblastic-Leukemia-CNV-Project

## Genomic and Sequence Analysis of CNVs in Acute Lymphoblastic Leukemia:
This repository contains the analysis, documentation, and reproducibility materials for my bioinformatics project analyzing recurrent copy-number variations (CNVs) in acute lymphoblastic leukemia (ALL). The aim of this project is to determine whether recurrent CNVs exhibit preferential disruption of evolutionarily conserved coding regions within essential leukemia driver genes. The entire analyses were performed in Python using Google Colab.

## Project Overview:
This project explores the research question: Do recurrent copy-number variations (CNVs) in acute lymphoblastic leukemia (ALL) disproportionately disrupt evolutionarily conserved coding regions? To address this question, CNV segment files from the TARGET-ALL Phase II dataset were processed and mapped to RefSeq coding exons for five major ALL genes (IKZF1, PAX5, CDKN2A, CDKN2B, and ETV6). Statistical tests including Fisher’s exact test, the Mann–Whitney U test, and binomial recurrence testing—were performed to assess subtype-specific CNV losses, CNV load among patients, and recurrence rate. The purpose is to assess whether these recurrent CNVs selectively compromise conserved coding regions, indicating disruption of essential functional domains involved in leukemogenesis.

## Data Sources:
• TARGET-ALL Phase II CNV data and clinical metadata (cBioPortal for Cancer Genomics, 2024). 
• UCSC Genome Browser: RefSeq CDS coordinates, phyloP100way conservation tracks (UCSC Genome Browser, 2024).
• National Cancer Institute (NCI): background information on acute lymphoblastic leukemia (National Cancer Institute, 2024).

## Methods:
This project was implemented in Python using Google Colab. CNV segment files from cBioPortal were loaded, merged, and converted into gain/loss/neutral calls using pandas and numpy. CNVs were mapped to RefSeq coding exons obtained from the UCSC Genome Browser, and subtype labels were integrated using clinical metadata. Statistical analyses were performed using SciPy (Fisher’s exact test, Mann–Whitney U, and binomial recurrence tests), and all figures were generated using matplotlib. The complete workflow is documented in the notebooks/ directory.


## Reproducibility Instructions:
Install the required Python packages listed in environment.txt and environment.yml
Open the analysis notebook located in the notebooks folder.
Run each section of the workflow in order:
– CNV loading and preprocessing
– CNV gain/loss assignment
– Mapping CNVs to RefSeq coding exons
– Integrating clinical subtype information
– Running statistical tests
– Generating each figure
All output figures will be saved automatically in the results folder.

## Figures:
All figures used in the written report are stored in the results directory, including:
• CNV call distribution per gene
• Subtype-specific loss frequencies
• CNV loss burden per patient
• Oncoprint-style CNV visualization

## AI Usage Statement: 
Chat (GPT-5) & Gemini was utilized as an assistive tool for code and error detection, syntax clarification, and analyzing statistical outputs. Every AI-generated code was manually verified by running the code in Google Colab and checking that the outputs matched expectations of the project. No figures, statistical values, or CNV results were taken directly from AI; these were all produced in Python. Dataset privacy was not a concern due to the Target-ALL data being publicly available and fully de-identified, and no sensitive information was shared with AI tools. Verification was reviewed, assessed, and ensured correctness within Python for completion of this project. 
