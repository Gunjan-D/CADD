# CADD Practical File - Lab Work Summary

This repository documents my **Computer-Aided Drug Design (CADD)** practical work, including **chemical data retrieval, structure formats, docking, virtual screening, molecular dynamics, and gene analysis**. The practicals follow a step-by-step workflow using common bioinformatics and cheminformatics databases and tools.

---

## What I Completed

### Practical 1: Chemical File Formats + Compound Property Identification
- Studied a drug molecule (**Morphine**, DrugBank ID: DB00295) and collected:
  - Chemical formula, targets, pathways, toxicity notes, and physical properties. :contentReference[oaicite:1]{index=1}
- Learned and documented key chemical structure file formats:
  - **MOL** (single structure, coordinates + connection table, ends with `M END`) :contentReference[oaicite:2]{index=2}
  - **SDF / 3D-SDF** (can store multiple structures + properties, ends with `$$$$`) :contentReference[oaicite:3]{index=3}
  - **PDB** (Protein Data Bank style structure text, ends with `END`) :contentReference[oaicite:4]{index=4}
  - **SMILES** (linear string representation) :contentReference[oaicite:5]{index=5}
  - **InChI** (International Chemical Identifier string) :contentReference[oaicite:6]{index=6}
- Compared experimental vs predicted properties (LogP, pKa, solubility, etc.) and reviewed ADMET predictions. :contentReference[oaicite:7]{index=7}

---

### Practical 2: PubChem Data Retrieval and Analysis
Using **Morphine** in PubChem:
- Retrieved **compound + substance + bioassay + patent** info. :contentReference[oaicite:8]{index=8}
- Extracted computed chemical properties (molecular weight, XLogP, HBD/HBA, TPSA, etc.). :contentReference[oaicite:9]{index=9}
- Identified **2D structure**, **3D conformer**, and listed similar 3D structures.
- Visualized the 3D structure using **Discovery Studio (DS) Visualizer**. :contentReference[oaicite:10]{index=10}

---

### Practical 3: Molecular Interaction Studies (AutoDock)
Goal: Dock a ligand with a protein using AutoDock tools.
- Selected **HIV protease complex (PDB: 1BDR)** as receptor. :contentReference[oaicite:11]{index=11}
- Prepared receptor:
  - Removed water molecules and ligand, saved cleaned protein. :contentReference[oaicite:12]{index=12}
- Selected ligand from PubChem (example used: **Indinavir**) and prepared it in AutoDock:
  - Added hydrogens, merged non-polar hydrogens, added Kollman charges, assigned AD4 atom types.
  - Generated ligand/receptor **PDBQT** files.
  - Configured grid box + saved GPF and DPF files.
- Ran docking with **Lamarckian Genetic Algorithm**, analyzed best conformations by binding energy and clusters.
- Visualized receptor-ligand interactions in DS Visualizer with 2D interaction diagrams. :contentReference[oaicite:13]{index=13}

---

### Practical 4: Virtual Screening with AutoDock Vina
Goal: Perform docking/virtual screening workflow (Vina-based).
- Selected protein + inhibitor example:
  - Example workflow includes **Curcumin**, and protein IDs referenced include **4K58** and **1A3Q** in the steps. :contentReference[oaicite:14]{index=14}
- Downloaded top compounds in SDF format and used OpenBabel-based steps to handle ligand sets.
- Prepared receptor (remove water, check missing atoms, set grid center/box).
- Produced docking output and identified favorable conformations and interacting amino acids. :contentReference[oaicite:15]{index=15}

---

### Practical 5: Molecular Dynamics Simulation Using GROMACS
Goal: Run MD simulation and analyze stability/geometry.
- Selected a protein structure (example listed: **3VH5 or 1AKI**). :contentReference[oaicite:16]{index=16}
- Steps included:
  - Clean structure (remove water), generate topology, define box, solvate, add ions.
  - Energy minimization, then analysis using `.edr` and plotting via XMGrace/Grace tools. :contentReference[oaicite:17]{index=17}

---

### Practical 6: Gene Annotation using Ensembl Genome Browser
Goal: Explore gene annotation features in Ensembl.
- Worked with **BRCA1**:
  - Located gene position, explored region details, transcripts, gene tree metrics, ontologies, exons, protein and cDNA sequence views. :contentReference[oaicite:18]{index=18}

---

### Practical 7: Gene Prediction using FGENESH
Goal: Predict gene/exon structure from a FASTA sequence.
- Used NCBI nucleotide sequence input and predicted:
  - Sequence length, predicted exon count, start/stop codon positions, and reported scores. :contentReference[oaicite:19]{index=19}

---

### Practical 8: GEO Gene Expression Data Analysis
Goal: Analyze differential expression using GEO2R.
- Loaded GEO dataset, grouped samples (normal vs disease), ran analysis.
- Reviewed plots such as:
  - Volcano plot, mean-difference plot, UMAP, Venn diagram, boxplot, density plot, p-value histogram, QQ plot, mean-variance trend. :contentReference[oaicite:20]{index=20}

---

## Tools and Platforms Used
- DrugBank (drug targets, pathways, properties) :contentReference[oaicite:21]{index=21}  
- PubChem (compound/substance/bioassay/patent + 2D/3D structures) :contentReference[oaicite:22]{index=22}  
- Discovery Studio (DS Visualizer) (3D visualization + interaction diagrams) :contentReference[oaicite:23]{index=23}  
- AutoDock + AutoGrid (docking setup + LGA runs) :contentReference[oaicite:24]{index=24}  
- AutoDock Vina (virtual screening) :contentReference[oaicite:25]{index=25}  
- OpenBabel (ligand handling steps) :contentReference[oaicite:26]{index=26}  
- GROMACS (MD simulation pipeline) 
- Ensembl Genome Browser (gene annotation)  
- FGENESH (gene prediction) 
- NCBI GEO / GEO2R (gene expression analysis)  

---

## Key Outcomes
- Understood how chemical structures are represented across **MOL/SDF/3D-SDF/PDB/SMILES/InChI** formats.
- Practiced end-to-end workflows for:
  - **Chemical information retrieval**
  - **Protein-ligand docking + interaction visualization**
  - **Virtual screening**
  - **Molecular dynamics simulation**
  - **Gene annotation, prediction, and expression analysis**

---

## Notes
This repo is intended as a **documentation record** of practical workflows and results. Steps and outputs are based on the lab manual and screenshots captured in the CADD practical file. 
