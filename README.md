# 🧬 Protomeus 2
## Responsible Protein Variant & Structural Analysis Platform

---

## 🚀 Overview

**Protomeus 2** is a publication-grade computational framework for **sequence-, mutation-, and structure-aware comparison of protein variants**.  
It is designed with **biological responsibility**, **alignment validation**, and **misuse prevention** as core principles.

This tool is **not a toy**. It is built for researchers, students, and laboratories working with real protein data.

---

## 🧠 Why Protomeus 2 Exists

Many protein analysis tools allow users to:
- Compare non-homologous proteins
- Perform RMSD calculations without validating alignment
- Interpret structural differences that arise from poor comparability

**Protomeus 2 actively prevents this.**

If two proteins are not comparable, the tool will:
- Clearly report this
- Disable misleading analyses
- Warn the user explicitly

---

## 🧩 Core Capabilities

Protomeus 2 integrates **three validated modules** into a single pipeline:

1. Sequence & mutation analysis  
2. Structure superimposition (only when justified)  
3. External interpretation tools panel  

Each module runs independently but communicates biologically consistent results.

---

## 1️⃣ Sequence Extraction

- Extracts amino acid sequences directly from uploaded PDB files
- Handles missing residues and discontinuous chains
- Avoids FASTA assumptions
- Structure-aware sequence reconstruction

---

## 2️⃣ Global Sequence Alignment

- Global alignment using **BLOSUM62**
- Implemented via Biopython PairwiseAligner
- Explicit gap penalties
- Supports large insertions and deletions

### Calculated Metrics
- Sequence identity (%)
- Alignment coverage (%)
- Total aligned length

---

## 3️⃣ Mutation Detection & Classification

Detected differences are classified as:

- **Substitution** → amino acid replacement
- **Insertion** → residue present only in mutant
- **Deletion** → residue present only in wild-type

Each mutation records:
- Wild-type position
- Mutation type
- Exact amino acid change

---

## 4️⃣ Mutation Summary Visualization

Protomeus 2 generates a **mutation summary box** with:

- Fixed white background
- Black base text
- Color-coded changes:
  - **Green** → substitutions
  - **Blue** → insertions
  - **Red** → deletions

The visualization:
- Is alignment-aware
- Preserves positional accuracy
- Prevents overflow or misalignment

---

## 5️⃣ Physicochemical Property Analysis

Calculated using **BioPython ProtParam**:

- Protein length
- Molecular weight (Da)
- Isoelectric point (pI)
- GRAVY score
- Instability index
- Stability classification

Differences between wild-type and mutant are reported explicitly.

---

## 6️⃣ Structural Validation Gate (Critical)

Before performing **any structural superimposition**, Protomeus 2 validates:

- Sequence identity ≥ 30%
- Alignment coverage ≥ 60%
- Comparable protein length

### If validation fails:
- Structural analysis is disabled
- Clear warning is shown
- No RMSD or folding claims are made

---

## 7️⃣ Structural Superimposition

When validation passes:

- Cα atoms are extracted
- Alignment-restricted residues are used
- Kabsch algorithm is applied
- Mutant structure is transformed safely

Interactive visualization is provided using **py3Dmol**.

---

## 8️⃣ External Variant Interpretation Tools

Protomeus 2 provides direct access to trusted external tools:

- iMODS – Normal Mode Analysis
- DynaMut2 – Stability & flexibility
- SIFT – Sequence pathogenicity
- PolyPhen-2 – Structural damage
- PhD-SNP – Disease association
- I-Mutant – ΔΔG stability
- CADD – Variant deleteriousness
- MUpro – Protein stability

These tools are **linked, not embedded**, preserving responsibility.

---

## 🚫 What Protomeus 2 Does NOT Do

- Does NOT predict clinical pathogenicity
- Does NOT infer disease causation
- Does NOT replace wet-lab experiments
- Does NOT force comparison of unrelated proteins
- Does NOT interpret post-translational modifications automatically

---

## ⚠️ Limitations

- Depends on quality of PDB structures
- Cannot model long-range allosteric effects
- Does not simulate dynamics beyond rigid alignment
- PTMs must be interpreted manually
- Single-chain focused analysis

---

## 🎯 Intended Use Cases

- Academic research
- Variant prioritization
- Structural biology education
- Thesis and dissertation projects
- Pre-screening before wet-lab validation

---

## 🧪 Scientific Responsibility Statement

Protomeus 2 is designed to **prevent overinterpretation**.  
All results must be validated experimentally.

The authors assume no responsibility for misuse or unsupported conclusions.

---

## 📦 Requirements

- Python ≥ 3.9
- Biopython
- NumPy
- Pandas
- py3Dmol
- ipywidgets
- Google Colab (recommended)

---

## 🧬 Version

**Protomeus 2**  
A complete redesign focused on correctness, responsibility, and publication-grade output.
