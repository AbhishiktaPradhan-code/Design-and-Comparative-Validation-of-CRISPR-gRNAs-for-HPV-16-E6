# RNA Secondary Structure Prediction 🧬

**Tool Used:** [RNAfold – ViennaRNA Web Server](http://rna.tbi.univie.ac.at/cgi-bin/RNAWebSuite/RNAfold.cgi)  
**Goal:** Predict gRNA folding patterns that may hinder Cas protein binding. Ideal guides should remain **mostly linear**, avoiding internal pairing or hairpins in the seed region.

---

### Summary Table

| gRNA ID | Sequence (RNA)                  | MFE (kcal/mol) | Structure        | Interpretation                    | Verdict   |
|---------|----------------------------------|----------------|------------------|------------------------------------|-----------|
| gRNA1   | AGGACCCACAGGAGCGACCCAGA          | –0.90          | Small loop       | Mild folding, mostly linear        |  Keep    |
| gRNA2   | UGCAUAGUAUAUAGAGAUGGGAA          | 0.00           | Fully linear     | Ideal structure                    |  Keep    |
| gRNA3   | CAGCUCUGUGCAUAACUGUGGUA          | –1.30          | Hairpin at 5′    | Some folding near seed             |  Caution |
| gRNA4   | UAUGGAACAACAUUAGAACAGCA          | –0.30          | Small hairpin    | Very light folding, tolerable      |  Keep    |
| gRNA5   | CACAUACAGCAUAUGGAUUCCC           | –0.50          | Mid-sequence stem| Moderate fold, possible interference|  Caution |
| gRNA6   | ACAGUUAAUACACCUAAUUAACA          | –2.40          | Large hairpin    | Seed region folded, may disrupt binding |  Discard |

---

## Detailed Interpretations

### 🔹 gRNA1
- **Sequence**: AGGACCCACAGGAGCGACCCAGA
- **Minimum Free Energy (MFE)**: –0.90 kcal/mol
- **Structure**:  
  `..........((......))...`  
  - A small hairpin structure is observed toward the end of the sequence.
  - **Ensemble frequency**: 54.98%
- **Interpretation**: While not fully linear, folding is minimal and likely won't hinder binding.
- **Verdict**: Suitable for use.

---

### 🔹 gRNA2
- **Sequence**: UGCAUAGUAUAUAGAGAUGGGAA
- **MFE**: 0.00 kcal/mol
- **Structure**:  
  `.......................`  
  - No secondary structure predicted (fully unstructured).
  - **Ensemble frequency**: 80.81%  
- **Interpretation**: Best-case structure — fully linear, highly accessible.
-  **Verdict**: Ideal gRNA.

---

### 🔹 gRNA3
- **Sequence**: CAGCUCUGUGCAUAACUGUGGUA
- **MFE**: –1.30 kcal/mol
- **Structure**:  
  `..((.....))............`  
  - A short hairpin is present near the **5′ end**, possibly interfering with seed region activity.
  - **Ensemble frequency**: 51.36%
- **Interpretation**: Might affect binding efficiency depending on guide design and target.
-  **Verdict**: Use with caution or redesign if performance is poor.

🔹 gRNA4
- **Sequence**: UAUGGAACAACAUUAGAACAGCA
- **MFE**: –0.30 kcal/mol
- **Dot-Bracket**: `.(((......)))..........`
- **Structure**: One small internal stem-loop in middle section
- **Ensemble frequency**: 50.20%
- **Interpretation**: Minimal structure, mostly accessible — acceptable.
-  **Verdict**: Keep

---

### 🔹 gRNA5
- **Sequence**: CACAUACAGCAUAUGGAUUCCC
- **MFE**: –0.50 kcal/mol
- **Dot-Bracket**: `..((((.....)))).......`
- **Structure**: Internal stem-loop (~positions 3–14)
- **Ensemble frequency**: 52.06%
- **Interpretation**: Folding occurs mid-sequence, could affect Cas loading.
- **Verdict**: Use with caution or redesign

---

### 🔹 gRNA6
- **Sequence**: ACAGUUAAUACACCUAAUUAACA
- **MFE**: –2.40 kcal/mol
- **Dot-Bracket**: `...((((((.......)))))).`
- **Structure**: Large stable hairpin (~positions 4–20)
- **Ensemble frequency**: 86.91%
- **Interpretation**: Highly structured and stable — **seed region likely occluded**.
- **Verdict**: Discard


