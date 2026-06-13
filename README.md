# FlyWire Summer Internship Qualification Challenge

## Objective

Identify the largest weakly connected directed induced subgraph conserved across at least three of the five FlyWire connectomic datasets.

## Datasets
The full dataset pool consists of five connectomes:
- BANC
- FAFB
- MANC
- MAOL
- MCNS
  
Among these, a subset of three datasets was selected for analysis based on the largest conserved structural motif identified under the applied graph-theoretic matching procedure.

## Selected Datasets

- MAOL v1.1
- MANC v1.2.1
- MCNS v0.9

## Methodology

### 1. Graph Construction

Each dataset was represented as a directed unweighted graph G=(V,E), where nodes correspond to neurons and edges represent synaptic connections. Synaptic weights were ignored in accordance with the challenge specification.

### 2. Degree Fingerprinting

Neurons were characterized using structural signatures defined by in-degree and out-degree values. This provided a compact representation of local connectivity patterns for cross-dataset comparison.

### 3.Weakly Connected Component Extraction

Each graph was decomposed into weakly connected components. Only sufficiently large components were retained to restrict the search space to biologically meaningful subnetworks.

### 4. Hub-Based Candidate Selection

High-degree neurons were used as anchor points for candidate circuit construction. Candidate correspondences were generated based on similarity of degree fingerprints and local connectivity structure.

### 5. Induced Subgraph Construction

For each candidate set of neurons, induced subgraphs were extracted from each dataset by restricting the graph to the selected nodes and preserving only internal edges among them.

### 6. Directed Graph Isomorphism Verification

Candidate induced subgraphs were tested using VF2 directed graph isomorphism to verify exact structural equivalence of connectivity patterns across datasets.

### 7. Three-Way Pairing

Final solutions were required to satisfy a single consistent neuron mapping that preserved full directed connectivity across MAOL, MANC, and MCNS simultaneously.

## Results

Largest conserved weakly connected circuit identified:

N = 18 neurons, was identified across the MAOL–MANC–MCNS.

## Repository Contents

- network.csv - matched neuron correspondence table across MAOL, MANC, and MCNS
- science.md - concise biological interpretation of the conserved circuit


## Reproducibility

The analytical workflow is fully specified and can be reproduced using standard graph-theoretic methods. The pipeline consists of structural fingerprinting, weakly connected component filtering, candidate selection based on hub nodes, and VF2-based directed graph isomorphism verification to ensure structural identity across all three datasets.
