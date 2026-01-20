🧬 Protomeus 2
Responsible Protein Variant & Structural Analysis Platform
<p align="center"> <img src="assets/protomeus_logo.png" width="300"/> </p>
🚀 Overview

Protomeus 2 is a next-generation protein analysis framework developed to ensure biological correctness, computational rigor, and ethical responsibility in protein variant studies.

Unlike traditional tools, Protomeus 2 actively prevents misuse by validating homology, alignment quality, and comparability assumptions before performing downstream analyses.

🧠 Why Protomeus 2?

Many tools allow:

Structural comparison of unrelated proteins

RMSD calculations without alignment validation

Overinterpretation of point mutations

Protomeus 2 refuses to do that.

It is designed for real science, not pretty pictures.

🔧 Core Modules
1️⃣ Sequence Extraction & Validation

Extracts sequences directly from PDB structures

Validates chain integrity

Handles missing residues and gaps

2️⃣ Global Alignment Engine

Uses BLOSUM62-based global alignment

Computes:

Sequence identity

Alignment coverage

Explicitly detects:

Substitutions

Insertions

Deletions

3️⃣ Mutation Mapping & Visualization

Mutation-aware alignment traversal

Color-coded mutation summary:

🟩 Substitution

🟦 Insertion

🟥 Deletion

Positionally accurate highlighting

4️⃣ Physicochemical Profiling

Molecular weight

Isoelectric point (pI)

GRAVY score

Instability index

5️⃣ Structural Safeguards

Before any superimposition:

✔ Identity ≥ 30%

✔ Coverage ≥ 60%

✔ Same fold assumption validated

If criteria fail:

⚠️ Structural comparison is disabled

6️⃣ Structure Superimposition (When Allowed)

Cα-based alignment

Kabsch algorithm

RMSD computed only on aligned regions

Visualized via NGLView

🚨 Built-In Responsibility Checks

Protomeus 2 automatically detects:

Non-homologous proteins

Excessive missing regions

Cross-species misuse (e.g., chicken vs human CFTR)

And responds with:

Clear warnings

Disabled modules

Transparent explanations

❌ What Protomeus 2 Does NOT Do

❌ No pathogenicity claims

❌ No clinical predictions

❌ No forced alignments

❌ No misuse of RMSD

❌ No assumption that “mutation = effect”

⚠️ Limitations

Dependent on PDB quality

Single-chain analysis

No PTM modeling (phosphorylation handled only if present in structure)

No dynamic simulations (MD is external)

🧪 Intended Use

Variant prioritization

Structural biology research

Thesis & dissertation work

Pre-wet-lab screening

Educational demonstrations

🧭 Ethical Statement

Protomeus 2 is designed to prevent misleading interpretations.
All results must be validated experimentally.
The authors are not responsible for misuse or overinterpretation.
