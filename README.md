#  Design and Comparative Validation of CRISPR gRNAs for HPV-16 E6

A complete **in silico design and validation** of guide RNAs (gRNAs) targeting the **HPV-16 E6 oncogene** using **CRISPR-Cas12a diagnostics**. This project incorporates BLAST validation, strain comparison, mutation screening, and RNA secondary structure analysis to ensure clinical reliability.

---
See full summary in:

📄 [Full Project Report](./https://github.com/AbhishiktaPradhan-code/Design-and-Comparative-Validation-of-CRISPR-gRNAs-for-HPV-16-E6/blob/61bb777c678f80dcadd336cb042458823082a816/HPV16_CRISPR_Cas12_Diagnostic_Design_Report.pdf)



##  Project Goal

To design **highly specific, mutation-resistant gRNAs** for the HPV-16 E6 gene, optimized for compatibility with **Cas12-based detection platforms** such as **DETECTR**.

---

## 🛠 Tools Used

- **CRISPR Design**: [CRISPOR](https://crispor.gi.ucsc.edu/)
- **BLAST Validation**: [NCBI BLASTN (short sequences)](https://blast.ncbi.nlm.nih.gov/Blast.cgi)
- **Strain Comparison**: [Clustal Omega](https://www.ebi.ac.uk/Tools/msa/clustalo/) — HPV-16 vs HPV-18 vs HPV-6b
- **Mutation Check**: [dbSNP](https://www.ncbi.nlm.nih.gov/snp/)
- **RNA Secondary Structure**: [RNAfold (ViennaRNA Web Server)](http://rna.tbi.univie.ac.at/cgi-bin/RNAWebSuite/RNAfold.cgi)

---

##  Workflow Summary

1. **Target Selection**: HPV-16 E6 gene chosen due to its clinical relevance in cervical cancer.
2. **gRNA Design**: Top 6 gRNAs shortlisted using CRISPOR based on on-target score and position.
3. **BLAST Filtering**: All gRNAs confirmed to uniquely target HPV-16 isolates.
4. **Strain Specificity**: gRNA2 and gRNA4 show partial conservation in HPV-18 and HPV-6b.
5. **Mutation Check**: No known SNPs overlap with selected gRNAs (dbSNP).
6. **RNA Structure Evaluation**: RNAfold identified 3 gRNAs with minimal structural folding suitable for Cas12 targeting.

---
##  The selected gRNA Candidates 

>grna_1 TTTCAGGACCCACAGGAGCGACCCAGA
     
>grna_2 TTTATGCATAGTATATAGAGATGGGAA    

>grna_3 TTTGCAGCTCTGTGCATAACTGTGGTA    

>grna_4 TTTGTATGGAACAACATTAGAACAGCA

>grna_5 TTTATCACATACAGCATATGGATTCCC

>grna_6 TTTGACAGTTAATACACCTAATTAACA

##  Final Recommendation

- **gRNA1, gRNA2, and gRNA4** passed all validation steps.
- These three are **recommended for downstream Cas12-based diagnostic testing**.
- gRNA3, gRNA5, and gRNA6 were specific and mutation-free but showed **unfavorable secondary structure** that may affect efficiency.

---

##  Final gRNA Evaluation Summary

| gRNA ID | BLAST Unique | SNP-Free | Type-Specific | RNA Structure | Verdict             |
|---------|---------------|-----------|----------------|----------------|---------------------|
| gRNA 1  | Yes           | Yes       | HPV-16 only    | Good           | Keep                |
| gRNA 2  | Yes           | Yes       | Partial        | Good           | Keep                |
| gRNA 3  | Yes           | Yes       | HPV-16 only    | Moderate       | Caution             |
| gRNA 4  | Yes           | Yes       | Partial        | Good           | Keep                |
| gRNA 5  | Yes           | Yes       | HPV-16 only    | Moderate       | Caution             |
| gRNA 6  | Yes           | Yes       | HPV-16 only    | Poor           | Discard             |




