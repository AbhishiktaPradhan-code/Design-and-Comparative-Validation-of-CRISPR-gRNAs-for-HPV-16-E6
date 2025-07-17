
##  BLAST Validation of gRNAs

###  Method

- Tool Used:NCBI BLASTn ([link](https://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=blastn&PAGE_TYPE=BlastSearch))
- Query Type: Short nucleotide sequences (gRNAs ~20 nt)
- Settings:
  - Database: `nt` (Nucleotide collection)
  - Program: `blastn`
  - Short query sequences mode:  Enabled
  - Word size: 7
  - Low complexity filter: OFF
  - Organism filter: None (global search)

> Each of the 6 gRNAs was submitted individually to assess sequence specificity.

---

##  Purpose

To confirm that designed gRNAs are **highly specific** to the HPV-16 genome and **do not match** any human or unrelated viral genomic sequences.  
This is critical for diagnostic CRISPR systems like SHERLOCK or DETECTR to avoid **false positives**.

---

##  Results Summary

| gRNA ID | Sequence                               | BLAST Matches | Organism(s) Found In        | % Identity | Passed? |                   
|---------|-----------------------|----------------|----------------|-----------------------------|------------|--------|
| gRNA_1  | `AGGACCCACAGGAGCGACCCAGA `             | 100+           | HPV-16 isolates only         | 100%       | Yes  |
| gRNA_2  | `TGCATAGTATATAGAGATGGGAA`              | 100+           | HPV-16 isolates only         | 100%       | Yes  | 
| gRNA_3  | `CAGCTCTGTGCATAACTGTGGTA `             | 100+           | HPV-16 isolates only         | 100%       | Yes  | 
| gRNA_4  | `TATGGAACAACATTAGAACAGCA`              | 100+           | HPV-16 isolates only         | 100%       | Yes  | 
| gRNA_5  | `TCACATACAGCATATGGATTCCC`              | 100+           | HPV-16 isolates only         | 100%       | Yes  | 
| gRNA_6  | `ACAGTTAATACACCTAATTAACA`              | 100+           | HPV-16 isolates only         | 100%       | Yes  |

*Note: All sequences showed perfect matches only to HPV-16 genomes and variants — no matches in human genome or other unrelated organisms.*

---

##  Interpretation

- ✅ All 6 gRNAs **passed** the BLAST validation.
- No gRNAs showed **cross-reactivity** with the human genome, supporting their **high specificity**.
- This makes them suitable for **CRISPR-based diagnostic assays** targeting HPV-16.

