# FlyWire Summer Internship Qualification Challenge

## Objective

Identify the largest weakly connected directed induced subgraph conserved across at least three FlyWire connectomic datasets.

## Selected Datasets

- MAOL v1.1
- MANC v1.2.1
- MCNS v0.9

## Methodology

### 1. Degree Fingerprinting

Neurons were characterized using their in-degree and out-degree signatures to reduce the candidate search space.

### 2. Weakly Connected Component Extraction

Weakly connected components were extracted from each dataset and used as the search space for conserved circuit discovery.

### 3. Hub-Anchored Search

Highly connected neurons with matching degree signatures were used as anchors for candidate circuit matching.

### 4. VF2 Directed Graph Isomorphism

Candidate subgraphs were verified using VF2 graph isomorphism to ensure identical directed induced connectivity.

### 5. Three-Way Verification

Pairwise verification was performed across MAOL, MANC, and MCNS.

## Results

Largest conserved weakly connected circuit identified:

N = 18 neurons

## Repository Contents

- network.csv
- science.md
- source code
- figures

## Reproducibility

Run the analysis scripts in the code directory to reproduce the results.
