
Design and Comparative Validation of CRISPR gRNAs for HPV-16 E6

A complete in silico design and validation of gRNAs targeting the HPV-16 E6 gene using CRISPR-based diagnostics (Cas12a), incorporating mutation resistance, strain specificity, BLAST filtering, and RNA secondary structure analysis.

 Project Goal

To design highly specific, mutation-resistant gRNAs for the HPV-16 E6 gene, optimized for compatibility with Cas12-based detection systems such as DETECTR.

⸻

 Tools Used
	•	CRISPR Design: [CRISPR tool ]
	•	BLAST Validation: NCBI BLASTN (short sequences)
	•	Strain Comparison: Clustal Omega (HPV-16 vs 18 vs 6)
	•	Mutation Check: dbSNP
	•	RNA Structure Prediction: RNAfold (ViennaRNA Web Server)

⸻

 Workflow Summary
	1.	Target Selection: HPV-16 E6 gene selected due to strong clinical relevance.
	2.	gRNA Design: Top 6 gRNAs selected based on on-target score and location.
	3.	BLAST Filtering: All gRNAs confirmed to uniquely target HPV-16 isolates.
	4.	Strain Specificity: gRNA2 and gRNA4 show partial conservation in HPV-18,HPV-6b.
	5.	SNP Check: No known SNPs overlap with selected gRNAs (dbSNP, ViPR).
	6.	RNA Structure: RNAfold confirms 3 gRNAs with minimal folding → selected.

⸻

 Final Recommendation
	•	 gRNA1, gRNA2 and gRNA4 passed all validation steps.
    •	 These three are recommended for downstream Cas12-based testing.
	•	 gRNA 3, 5, 6 folded unfavorably but passed Blast,Strain specificity.
	

 Outputs

### Final gRNA Evaluation Summary

| gRNA ID | BLAST Unique  | SNP-Free  | Type-Specific  |    RNA Structure | Verdict             |
|---------|---------------|-----------|-----------------|=----------------|---------------------|
| gRNA 1  | Yes           | Yes       | HPV-16 only     | Good            | Keep                |
| gRNA 2  | Yes           | Yes       | Partial         | Good            | Keep                |
| gRNA 3  | Yes           | Yes       | HPV-16 only     | Moderate        | Caution             |
| gRNA 4  | Yes           | Yes       | Partial         | Good            | Keep                |
| gRNA 5  | Yes           | Yes       | HPV-16 only     | Moderate        | Caution             |
| gRNA 6  | Yes           | Yes       | HPV-16 only     | Poor            | Discard             |

⸻

 Slide Deck

See full summary in:

📄 [Download Full Project Report](./HPV16_CRISPR_Cas12_Diagnostic_Design_Report.pdf)


