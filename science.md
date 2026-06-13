# A Conserved 18-Neuron Circuit Across Three Male Drosophila Connectomes

## Background

Connectomics enables the reconstruction of complete neural wiring diagrams and provides an opportunity to identify circuit architectures that are conserved across independently reconstructed nervous systems. Such conserved circuits may represent fundamental computational motifs whose preservation reflects biological importance. Using the FlyWire Codex datasets, I sought to identify the largest neuronal circuit shared across multiple Drosophila connectomes and investigate its potential biological significance.

## Circuit Identification

Directed graphs were constructed from the provided edge lists, where neurons were represented as nodes and synaptic connections as directed edges. Candidate neuron correspondences were first restricted using degree-based fingerprints derived from in-degree and out-degree connectivity patterns. Weakly connected components were extracted to constrain the search space to biologically meaningful subnetworks. Highly connected hub neurons were used as anchor points for candidate matching, and candidate induced subgraphs were evaluated under a directed graph isomorphism framework.

VF2 directed graph isomorphism testing confirmed full structural equivalence under a single consistent neuron mapping across MAOL v1.1, MANC v1.2.1, and MCNS v0.9. This procedure identified an 18-neuron weakly connected directed induced subgraph conserved across all three datasets.

## Biological Interpretation

The conserved circuit exhibits a hub-centered architecture containing recurrent and reciprocal connectivity motifs. Such motifs are common features of neural systems and may support signal amplification, persistence of neural activity, temporal integration, or robustness to noisy inputs.

Inspection of FlyWire metadata revealed that many constituent neurons are associated with the male adult optic lobe and remain largely unclassified with respect to cell type and neurotransmitter identity. The presence of a fully conserved connectivity structure despite incomplete biological annotation suggests that this circuit may represent an important but currently under-characterized component of the Drosophila nervous system.

As a researcher with an interest in visual neuroscience, I found the optic-lobe localization particularly compelling. The optic lobe serves as the fly's primary visual processing center and contains specialized circuits involved in motion detection, visual feature extraction, and visually guided behavior. Although the exact function of this circuit remains unknown, its recurrent organization and anatomical localization suggest a role in visual information processing or visuomotor transformation.

## Hypothesis

I hypothesize that this conserved circuit functions as a neural module involved in integrating visual signals and relaying behaviorally relevant information to downstream motor pathways. The circuit's conservation across three independent male connectomes suggests that it may represent a robust computational motif preserved by evolutionary and functional constraints. Future studies using genetic labeling, calcium imaging, and optogenetic perturbation could determine whether this circuit contributes to visual processing, navigation, object tracking, or other visually guided behaviors.

## References

1. Dorkenwald S, et al. FlyWire: Online community for whole-brain connectomics. Nature Methods, 2023.

2. Schlegel P, et al. Whole-brain annotation and multi-connectome analysis of Drosophila. Nature, 2024.

3. Namiki S, et al. The functional organization of descending sensory-motor pathways in Drosophila. eLife, 2018.

4. Masland RH. The neuronal organization of the retina. Nature Neuroscience, 2012.

5. Gruntman E, Turner GC. Integration of visual motion signals in Drosophila. Nature Neuroscience, 2018.
