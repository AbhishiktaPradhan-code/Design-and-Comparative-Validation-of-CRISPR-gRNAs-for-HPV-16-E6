# Strain Comparison (HPV-16, HPV-18, HPV-6)

## Goal
To assess whether gRNA sequences are conserved or variable across HPV types, indicating type-specificity vs. broad-spectrum potential.

## Method
- Extracted E6 gene sequences from:
  - NC_001526.4:7125-7601 Human papillomavirus type 16 E6

  - >lcl|NC_001357.1_cds_NP_040310.1_1 [gene=E6] [locus_tag=HpV18gp1] [db_xref=GOA:P06463,InterPro:IPR001334,UniProtKB/Swiss-Prot:P06463] [protein=E6 protein] [protein_id=NP_040310.1] [location=105..581] [gbkey=CDS]

  ->lcl|NC_001355.1_cds_NP_040296.1_1 [gene=E6] [locus_tag=HPV6bgp1] [db_xref=GOA:P06462,InterPro:IPR001334,UniProtKB/Swiss-Prot:P06462] [protein=E6 protein] [protein_id=NP_040296.1] [location=102..554] [gbkey=CDS]

- Aligned using [Clustal Omega](https://www.ebi.ac.uk/Tools/msa/clustalo/)
- Visualized mismatches across aligned sequences near gRNA binding sites.

## gRNA Sites Analyzed
Included the following gRNAs:
>grna_1 TTTCAGGACCCACAGGAGCGACCCAGA  

>grna_2 TTTATGCATAGTATATAGAGATGGGAA    

>grna_3 TTTGCAGCTCTGTGCATAACTGTGGTA    

>grna_4 TTTGTATGGAACAACATTAGAACAGCA

>grna_5 TTTATCACATACAGCATATGGATTCCC

>grna_6 TTTGACAGTTAATACACCTAATTAACA

Mapped each onto alignment manually (via Ctrl+F).

## Key Observations
- gRNA2 and gRNA4 show **partial conservation** across strains (HPV-6, 16, 18)  
- gRNA1, 3, 5, 6 are **highly specific to HPV-16** 

## Conclusion
- gRNA 1,3,5,6  are **type-specific**, ideal for subtype-targeted diagnostics.
- gRNA 2,4 may have potential for **multi-type detection** 
