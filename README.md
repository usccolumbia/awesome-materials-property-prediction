<p align="center"><img src="assets/banner.svg" alt="Awesome Materials Property Prediction" width="100%"></p>

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

> A curated list of resources on **machine-learning prediction of materials properties**: the databases models are trained on, hand-crafted features and learned representations, the model families from kernel methods to equivariant foundation models, out-of-distribution generalization and small-data learning, and the benchmarks and leaderboards used to compare them. It accompanies the survey *Machine Learning for Materials Property Prediction: Features, Models, Generalization and Benchmarks*.

## About the Survey

**Machine Learning for Materials Property Prediction: Features, Models, Generalization and Benchmarks** (paper: in preparation)

Jianjun Hu<sup>1,*</sup>, et al.<br>
<sup>1</sup> Department of Computer Science and Engineering, University of South Carolina, Columbia, SC 29201, USA<br>
<sup>*</sup> Corresponding author: jianjunh@cse.sc.edu

The list currently holds **600** verified entries (DOI or arXiv identifier checked). A machine-readable copy is in [`data/papers.csv`](data/papers.csv) and BibTeX in [`data/references.bib`](data/references.bib).

## Contents

- [About the Survey](#about-the-survey)
- [Datasets and Databases](#datasets-and-databases)
- [Features and Descriptors](#features-and-descriptors)
- [Representation Learning](#representation-learning)
- [Machine Learning Models](#machine-learning-models)
- [OOD Generalization, Redundancy and Uncertainty](#ood-generalization-redundancy-and-uncertainty)
- [Small-Data Learning](#small-data-learning)
- [Benchmarks and Leaderboards](#benchmarks-and-leaderboards)
- [Language Models for Property Prediction](#language-models-for-property-prediction)
- [Applications of Property Models](#applications-of-property-models)
- [Reviews and Perspectives](#reviews-and-perspectives)
- [Property Datasets](#property-datasets)
- [Leaderboard Snapshot](#leaderboard-snapshot)
- [Contributing](#contributing)
- [Citation](#citation)
- [License](#license)

## Datasets and Databases

### 2D materials database

* [The Computational 2D Materials Database: high-throughput modeling and discovery of atomically thin crystals](https://doi.org/10.1088/2053-1583/aacfc1) - C2DB: high-throughput DFT/GW properties for thousands of 2D materials (Haastrup et al., 2018, 2D Materials). [[code](https://c2db.fysik.dtu.dk)]

### Aggregated database

* [LeMat-Bulk: aggregating, and de-duplicating quantum chemistry materials databases](https://arxiv.org/abs/2511.05178) - LeMaterial's LeMat-Bulk unifies and de-duplicates Materials Project, Alexandria and OQMD into a harmonized multi-million-entry dataset (Siron et al., 2025, arXiv). [[code](https://huggingface.co/datasets/LeMaterial/LeMat-Bulk)]

### Catalysis (related)

* [Open Catalyst 2020 (OC20) Dataset and Community Challenges](https://doi.org/10.1021/acscatal.0c04525) - OC20: ~1.3M DFT relaxations (~265M single points) of adsorbate-surface systems with S2EF/IS2RE/IS2RS tasks and leaderboard (Chanussot et al., 2021, ACS Catalysis). [[code](https://github.com/FAIR-Chem/fairchem)]
* [The Open Catalyst 2022 (OC22) Dataset and Challenges for Oxide Electrocatalysts](https://doi.org/10.1021/acscatal.2c05426) - OC22: ~62k DFT relaxations (~9.8M single points) of oxide surfaces with adsorbates and associated benchmark tasks (Tran et al., 2023, ACS Catalysis). [[code](https://github.com/FAIR-Chem/fairchem)]

### Computational DFT database

* [AFLOW: An automatic framework for high-throughput materials discovery](https://doi.org/10.1016/j.commatsci.2012.02.005) - Presents the AFLOW high-throughput framework and associated AFLOWLIB repository of DFT-computed materials properties (Curtarolo et al., 2012, Computational Materials Science). [[code](https://aflowlib.org)]
* [Commentary: The Materials Project: A materials genome approach to accelerating materials innovation](https://doi.org/10.1063/1.4812323) - Introduces the Materials Project, an open high-throughput DFT database of inorganic compounds (now >150k materials) widely used as an ML training source (Jain et al., 2013, APL Materials). [[code](https://materialsproject.org)]
* [Materials Design and Discovery with High-Throughput Density Functional Theory: The Open Quantum Materials Database (OQMD)](https://doi.org/10.1007/s11837-013-0755-4) - Introduces the OQMD, a high-throughput DFT database of formation energies for hundreds of thousands of inorganic compounds (Saal et al., 2013, JOM). [[code](https://oqmd.org)]
* [The AFLOW standard for high-throughput materials science calculations](https://doi.org/10.1016/j.commatsci.2015.07.019) - Defines the standardized calculation parameters underlying AFLOW database entries, enabling consistent ML training data (Calderon et al., 2015, Computational Materials Science). [[code](https://aflowlib.org)]
* [The Open Quantum Materials Database (OQMD): assessing the accuracy of DFT formation energies](https://doi.org/10.1038/npjcompumats.2015.10) - Describes OQMD growth to ~300k compounds and benchmarks its DFT formation energies against experiment (Kirklin et al., 2015, npj Computational Materials). [[code](https://oqmd.org)]
* [The joint automated repository for various integrated simulations (JARVIS) for data-driven materials design](https://doi.org/10.1038/s41524-020-00440-1) - Describes NIST JARVIS infrastructure (JARVIS-DFT, -FF, -ML, -tools) including the ~55k-entry dft_3d dataset with many properties (Choudhary et al., 2020, npj Computational Materials). [[code](https://jarvis.nist.gov)]
* [A dataset of 175k stable and metastable materials calculated with the PBEsol and SCAN functionals](https://doi.org/10.1038/s41597-022-01177-w) - Alexandria-related dataset of 175k materials computed with PBEsol and SCAN functionals for higher-fidelity ML targets (Schmidt et al., 2022, Scientific Data). [[code](https://alexandria.icams.rub.de)]
* [Scaling deep learning for materials discovery](https://doi.org/10.1038/s41586-023-06735-9) - GNoME discovers ~2.2 million new crystals (381k on the convex hull) via active-learning GNNs and releases stable structures (Merchant et al., 2023, Nature). [[code](https://github.com/google-deepmind/materials_discovery)]
* [Machine-Learning-Assisted Determination of the Global Zero-Temperature Phase Diagram of Materials](https://doi.org/10.1002/adma.202210788) - Uses ML-guided high-throughput DFT to build the Alexandria convex hull with millions of calculated compounds (Schmidt et al., 2023, Advanced Materials). [[code](https://alexandria.icams.rub.de)]
* [Improving machine-learning models in materials science through large datasets](https://doi.org/10.1016/j.mtphys.2024.101560) - Releases the expanded Alexandria database (millions of PBE calculations) and shows scaling of GNN property models with data size (Schmidt et al., 2024, Materials Today Physics). [[code](https://alexandria.icams.rub.de)]

### Data access and featurization

* [Matminer: An open source toolkit for materials data mining](https://doi.org/10.1016/j.commatsci.2018.05.018) - Matminer provides dataset loaders (incl. dozens of curated datasets) and featurizers for materials ML (Ward et al., 2018, Computational Materials Science). [[code](https://github.com/hackingmaterials/matminer)]

### Data quality: anthropogenic and selection bias

* [Anthropogenic biases in chemical reaction data hinder exploratory inorganic synthesis](https://doi.org/10.1038/s41586-019-1540-5) - Shows that reported amine-templated metal oxide syntheses follow a power law (17% of amines appear in 79% of compounds) and, using 548 randomly generated experiments, that reagent popularity is uncorrelated with success and that models trained on a smaller randomized dataset outperform those trained on larger human-selected data (Jia et al., 2019, Nature).
* [Predicting energy and stability of known and hypothetical crystals using graph neural network](https://doi.org/10.1016/j.patter.2021.100361) - Demonstrates that a GNN trained only on ground-state structures is biased and that a balanced training set (~16,500 NREL MatDB ground-state plus ~11,000 hypothetical higher-energy structures) is needed to rank polymorph energies correctly, with error analysis exposing outliers and occasional inconsistencies in the training data (Pandey et al., 2021, Patterns).

### Data quality: cross-database discrepancies

* [Quantifying uncertainty in high-throughput density functional theory: A comparison of AFLOW, Materials Project, and OQMD](https://doi.org/10.1103/physrevmaterials.7.053805) - Pairwise comparison of AFLOW, Materials Project and OQMD records computed from the same initial structures finds disagreement up to 0.105 eV/atom in formation energy, 0.21 eV in band gap and 0.65 A^3/atom in volume (comparable to DFT-experiment differences), with up to 7% of records disagreeing on metallicity and 15% on magnetism, traced to pseudopotential, DFT+U and elemental-reference choices (Hegde et al., 2023, Physical Review Materials).

### Data quality: database coverage bias

* [The Roadmap of Inorganic Computational Materials Databases: Capabilities, Credibility, Coverage, and the Open Frontier](https://arxiv.org/abs/2609.19833) - Perspective surveying DFT codes, cost and credibility for nineteen property families and database coverage, concluding that structure, energetics, elasticity and topology are routinely tabulated while nine families (e.g. NMR/EPR parameters, core-level spectra, electron-phonon properties, thermal conductivity, quantum transport) still lack any systematic computational database (Liu et al., 2026, arXiv).

### Data quality: DFT reproducibility across codes

* [Reproducibility in density functional theory calculations of solids](https://doi.org/10.1126/science.aad3000) - Community Delta test comparing 15 solid-state DFT codes and 40 potential/basis-set types on PBE equations of state for 71 elemental crystals, finding that recent codes agree to within differences comparable to those between high-precision experiments, while older methods agree less well (Lejaeghere et al., 2016, Science).
* [How to verify the precision of density-functional-theory implementations via reproducible and universal workflows](https://doi.org/10.1038/s42254-023-00655-3) - Expert recommendation extending the Delta-style verification to Z = 1-96 with 10 cubic unaries and oxides per element, producing 960 all-electron reference equations of state cross-checked between two codes and used to verify and improve nine pseudopotential-based approaches (Bosoni et al., 2023, Nature Reviews Physics).

### Data quality: experimental data errors and curation

* [Tackling dataset curation challenges towards reliable machine learning: a case study on thermoelectric materials](https://doi.org/10.1016/j.mtphys.2025.101948) - Using half-Heusler thermoelectrics, documents inaccurate entries in the LLM-assisted Starrydata2 dataset (ambiguous nomenclature, complex formulas, high-variance multi-source values without synthesis information) that conventional curation misses, and proposes a statistical round-robin-error filter plus a hybrid manual/automatic curation workflow (Athar et al., 2025, Materials Today Physics).

### Data repository

* [NOMAD: The FAIR concept for big data-driven materials science](https://doi.org/10.1557/mrs.2018.208) - Describes the NOMAD repository and FAIR data principles for the largest archive of raw computational materials data (Draxl et al., 2018, MRS Bulletin). [[code](https://nomad-lab.eu)]
* [The NOMAD laboratory: from data sharing to artificial intelligence](https://doi.org/10.1088/2515-7639/ab13bb) - Overview of the NOMAD Laboratory: repository, archive, encyclopedia and AI toolkit for materials data (Draxl et al., 2019, Journal of Physics: Materials). [[code](https://nomad-lab.eu)]
* [Materials Cloud, a platform for open computational science](https://doi.org/10.1038/s41597-020-00637-5) - Presents Materials Cloud, an open platform sharing AiiDA-provenance computational materials data and curated datasets (Talirz et al., 2020, Scientific Data). [[code](https://www.materialscloud.org)]

### Dielectric and piezoelectric: DFPT dielectric database

* [High-throughput screening of inorganic compounds for the discovery of novel dielectric and optical materials](https://doi.org/10.1038/sdata.2016.134) - A DFPT database of dielectric tensors and refractive indices for 1,056 compounds, then the largest available and integrated into the Materials Project, which seeded later ML models of epsilon and n (Petousis et al., 2017, Scientific Data).

### Dielectric and piezoelectric: ferroelectric polarization database

* [An automatically curated first-principles database of ferroelectrics](https://doi.org/10.1038/s41597-020-0407-9) - A symmetry-driven automated DFT workflow screens over 67,000 Materials Project entries to give 255 ferroelectric candidates (126 newly proposed) with structures, band gaps, energies and spontaneous polarizations benchmarked against experiment (Smidt et al., 2020, Scientific Data).

### Experimental database

* [The PAULING FILE Project and Materials Platform for Data Science: From Big Data Toward Materials Genome](https://doi.org/10.1007/978-3-319-44677-6_62) - Describes the PAULING FILE / MPDS curated experimental database of crystal structures, phase diagrams and physical properties (Blokhin et al., 2020, Handbook of Materials Modeling (Springer)). [[code](https://mpds.io)]

### Experimental dataset

* [Predicting the Band Gaps of Inorganic Solids by Machine Learning](https://doi.org/10.1021/acs.jpclett.8b00124) - Curates ~6k experimental band gaps of inorganic solids (basis of Matbench expt_gap) and trains composition-based SVR models (Zhuo et al., 2018, The Journal of Physical Chemistry Letters).

### Experimental: superconductivity, disordered structures

* [Learning Superconductivity from Ordered and Disordered Material Structures](https://proceedings.neurips.cc/paper_files/paper/2024/hash/c4e3b55ed4ac9ba52d7df11f8bddbbf4-Abstract-Datasets_and_Benchmarks_Track.html) - Introduces SuperCon3D, pairing experimental Tc values with ordered and disordered ICSD structures, and SODNet, an equivariant model that uses both ordered and disordered structural information to predict Tc (Chen et al., 2024, NeurIPS 2024 Datasets and Benchmarks Track).

### Ionic conductivity: experimental Li-conductivity database (composition-only)

* [A database of experimentally measured lithium solid electrolyte conductivities evaluated with machine learning](https://doi.org/10.1038/s41524-022-00951-z) - Curates 820 impedance-measured Li-ion conductivities from 214 sources (403 unique compositions near room temperature) and trains a CrabNet composition-only classifier that labels compositions as high or low conductivity to help experimentalists prioritize candidates (Hargreaves et al., 2023, npj Computational Materials).

### Ionic conductivity: experimental Li-conductivity dataset with crystal structures

* [OBELiX: a curated dataset of crystal structures and experimentally measured ionic conductivities for lithium solid-state electrolytes](https://doi.org/10.1039/d5dd00441a) - OBELiX curates 599 synthesized Li solid electrolytes with experimentally measured room-temperature conductivities, composition, space group and lattice parameters (about 320 with full CIFs), provides splits designed to avoid leakage, and benchmarks seven ML models on conductivity regression (Therrien et al., 2026, Digital Discovery). [[code](https://github.com/NRC-Mila/OBELiX)]

### Material classes: polymers

* [An open benchmark for machine learning-based polymer property prediction](https://arxiv.org/abs/2609.27036) - PolyBench26 is an open benchmark of nearly 250,000 polymer-property datapoints over eight properties (experiment, DFT, MD) spanning homopolymers and alternating, random and block copolymers, on which graph-based models give the lowest errors across data sizes and repeat-unit complexity (Learsch et al., 2026, arXiv). [[code](https://github.com/rlearsch/PolymerBenchmark2026)]

### MLIP training trajectories

* [CHGNet as a pretrained universal neural network potential for charge-informed atomistic modelling](https://doi.org/10.1038/s42256-023-00716-3) - Introduces CHGNet and the MPtrj dataset (~1.58M structures from ~146k Materials Project relaxations) with energies, forces, stresses and magmoms (Deng et al., 2023, Nature Machine Intelligence). [[code](https://github.com/CederGroupHub/chgnet)]
* [Open Materials 2024 (OMat24) Inorganic Materials Dataset and Models](https://arxiv.org/abs/2410.12771) - Meta FAIR OMat24 dataset of ~110M DFT calculations on non-equilibrium inorganic structures, with EquiformerV2 models (Barroso-Luque et al., 2024, arXiv). [[code](https://huggingface.co/datasets/fairchem/OMAT24)]
* [A Foundational Potential Energy Surface Dataset for Materials](https://arxiv.org/abs/2503.04070) - MatPES: ~400k carefully sampled structures with PBE and r2SCAN single points for training universal potentials (Kaplan et al., 2025, arXiv). [[code](https://matpes.ai)]

### Multimodal: structure + 2D projection images + structured text

* [Beyond Atomic Geometry Representations in Materials Science: A Human-in-the-Loop Multimodal Framework](https://arxiv.org/abs/2506.00302) - MultiCrystalSpectrumSet (MCS-Set) augments atomic structures with 2D projections and human-in-the-loop textual annotations for multimodal property and summary prediction, and benchmarks of language and vision-language models reveal substantial modality-specific performance gaps (Polat et al., 2025, ICML 2025 Workshop on DataWorld). [[code](https://github.com/KurbanIntelligenceLab/MultiCrystalSpectrumSet)]

### Optoelectronic: defect properties of 2D materials

* [Unveiling the complex structure-property correlation of defects in 2D materials based on high throughput datasets](https://doi.org/10.1038/s41699-023-00369-1) - Introduces the 2D Material Defect (2DMD) DFT datasets of defect properties for MoS2, WSe2, hBN, GaSe, InSe and black phosphorus, together with a platform for applying ML to pristine and defected 2D materials and a data-driven analysis of how defect configurations control their properties (Huang et al., 2023, npj 2D Materials and Applications).

### Property-specific dataset

* [Charting the complete elastic properties of inorganic crystalline compounds](https://doi.org/10.1038/sdata.2015.9) - Full elastic tensors for 1,181 inorganic compounds computed in Materials Project; basis of elastic-moduli ML tasks (de Jong et al., 2015, Scientific Data). [[code](https://materialsproject.org)]
* [A database to enable discovery and design of piezoelectric materials](https://doi.org/10.1038/sdata.2015.53) - DFPT piezoelectric tensors for 941 inorganic compounds in Materials Project (de Jong et al., 2015, Scientific Data). [[code](https://materialsproject.org)]
* [High-throughput density functional perturbation theory and machine learning predictions of infrared, piezoelectric, and dielectric responses](https://doi.org/10.1038/s41524-020-0337-2) - JARVIS DFPT dataset of IR, piezoelectric and dielectric responses for thousands of materials, with ML models trained on it (Choudhary et al., 2020, npj Computational Materials). [[code](https://jarvis.nist.gov)]
* [A band-gap database for semiconducting inorganic materials calculated with hybrid functional](https://doi.org/10.1038/s41597-020-00723-8) - HSE hybrid-functional band gap database for ~10k semiconducting inorganic materials (Kim et al., 2020, Scientific Data).

### Superconductivity: electronic-structure dataset

* [SuperBand: an Electronic-band and Fermi surface structure database of superconductors](https://doi.org/10.1038/s41597-025-05015-7) - SuperBand provides DFT-optimized structures, band structures, DOS and Fermi surfaces for 1,362 superconductors with experimental Tc and 1,112 verified non-superconductors, designed for ML of superconducting properties beyond composition (Zhang et al., 2025, Scientific Data).

### Superconductivity: LLM-extracted experimental parameters

* [Machine-accelerated extraction of experimental superconducting parameters for physical insight and prediction across thousands of materials](https://arxiv.org/abs/2611.15627) - AutoSuperCon: 20,354 entries of eight experimental superconducting parameters for 6,793 superconductors, extracted from over 47,000 arXiv preprints by a large language model and validated against NIMS SuperCon (R2 = 0.96) (Manium et al., 2026, arXiv).

### Superconductivity: structure-matched experimental Tc dataset

* [3DSC - a dataset of superconductors including crystal structures](https://doi.org/10.1038/s41597-023-02721-y) - 3DSC augments SuperCon Tc data (including tested non-superconductors) with approximate 3D crystal structures and shows in ML experiments that adding structural information improves Tc prediction over composition alone (Sommer et al., 2023, Scientific Data).

### Thermal conductivity: anharmonic phonon database

* [Database and deep-learning scalability of anharmonic phonon properties by automated brute-force first-principles calculations](https://doi.org/10.1038/s41524-026-02033-w) - Builds an automated first-principles anharmonic phonon workflow and database of more than 6,500 inorganic compounds, then trains a GNN on structures to predict kappa_L and its spectra, showing that accuracy keeps improving with training-set size and screening for extreme-kappa materials (Ohnishi et al., 2026, npj Computational Materials).

### Thermoelectrics: DFT electronic transport database

* [An ab initio electronic transport database for inorganic materials](https://doi.org/10.1038/sdata.2017.85) - BoltzTraP constant-relaxation-time transport tensors (conductivity, Seebeck coefficient, effective mass) for about 48,000 Materials Project compounds, at publication the largest computed electronic-transport database and a standard label source for transport ML (Ricci et al., 2017, Scientific Data).

### Thermoelectrics: tensorial transport database

* [Dataset of tensorial optical and transport properties of materials from the Wannier function method](https://doi.org/10.1038/s41597-025-05396-9) - A Wannier-function database of tensorial electrical conductivity, thermal conductivity, Seebeck coefficient and zT (plus optical tensors) for 7301 materials, built to enable symmetry-aware ML of anisotropic transport (Fang et al., 2025, Scientific Data).

### Unified database with ML property completion

* [Probing the limits of materials design via a comprehensive crystal database of 14.6 million structures with 140 properties](https://arxiv.org/abs/2610.32678) - MateriaViva unifies 55 databases into 14.6 million distinct crystals with over one billion property values, using an equivariant Crystal Graph Transformer Network and 140 property-prediction models to complete missing properties; it finds tens of thousands of overlooked high-performance known materials and shows that 55-100% of inverse-designed structures are not new (Song et al., 2026, arXiv).

## Features and Descriptors

### Composition descriptors

* [High-Throughput Machine-Learning-Driven Synthesis of Full-Heusler Compounds](https://doi.org/10.1021/acs.chemmater.6b02724) - Uses composition-derived elemental property descriptors with ML to screen Heusler compounds (Oliynyk et al., 2016, Chemistry of Materials).

### Composition descriptors: oxidation states

* [An electrochemical series for materials](https://doi.org/10.1073/pnas.2320134121) - A physical, interpretable model of oxidation states parameterized by machine learning on tens of thousands of ICSD entries yields an electrochemical series for solid-state materials and predicts oxidation states from composition more accurately than a transformer model (Mueller et al., 2024, Proceedings of the National Academy of Sciences).
* [ApprOxiMate: a lightweight composition-only framework for mixed oxidation state estimation](https://doi.org/10.1039/d6dd00291a) - A lightweight composition-only framework that estimates mixed oxidation states in multicomponent inorganic systems, as a cheap alternative to computationally intensive assignment methods for high-throughput discovery (Timen et al., 2026, Digital Discovery).

### Featurizer toolkits

* [DScribe: Library of descriptors for machine learning in materials science](https://doi.org/10.1016/j.cpc.2019.106949) - DScribe: library implementing Coulomb matrix, SOAP, ACSF, MBTR and related descriptors (Himanen et al., 2020, Computer Physics Communications). [[code](https://github.com/SINGROUP/dscribe)]
* [Updates to the DScribe library: New descriptors and derivatives](https://doi.org/10.1063/5.0151031) - Update of the DScribe descriptor library with new descriptors and derivatives (Laakso et al., 2023, The Journal of Chemical Physics). [[code](https://github.com/SINGROUP/dscribe)]

### Representation comparison

* [Materials representation and transfer learning for multi-property prediction](https://doi.org/10.1063/5.0047066) - Studies materials representations and transfer learning for multi-property prediction (Kong et al., 2021, Applied Physics Reviews).
* [Physics-Inspired Structural Representations for Molecules and Materials](https://doi.org/10.1021/acs.chemrev.1c00021) - Review of physics-inspired structural representations for atomistic ML (Musil et al., 2021, Chemical Reviews).
* [Representations of molecules and materials for interpolation of quantum-mechanical simulations via machine learning](https://doi.org/10.1038/s41524-022-00721-x) - Reviews and benchmarks representations of molecules and materials for interpolation ML (Langer et al., 2022, npj Computational Materials).

### Structure descriptors

* [Atom-centered symmetry functions for constructing high-dimensional neural network potentials](https://doi.org/10.1063/1.3553717) - Defines atom-centered symmetry functions for local atomic environments (Behler et al., 2011, The Journal of Chemical Physics).
* [Fast and Accurate Modeling of Molecular Atomization Energies with Machine Learning](https://doi.org/10.1103/PhysRevLett.108.058301) - Introduces the Coulomb matrix representation for ML of molecular atomization energies (Rupp et al., 2012, Physical Review Letters).
* [On representing chemical environments](https://doi.org/10.1103/PhysRevB.87.184115) - Introduces SOAP and compares local atomic environment descriptors (Bartók et al., 2013, Physical Review B).
* [How to represent crystal structures for machine learning: Towards fast prediction of electronic properties](https://doi.org/10.1103/PhysRevB.89.205118) - Partial radial distribution function representation for predicting crystal DOS at the Fermi level (Schütt et al., 2014, Physical Review B).
* [Crystal structure representations for machine learning models of formation energies](https://doi.org/10.1002/qua.24917) - Extends Coulomb-matrix representations (Ewald sum, sine matrix) to periodic crystals (Faber et al., 2015, International Journal of Quantum Chemistry).
* [Universal fragment descriptors for predicting properties of inorganic crystals](https://doi.org/10.1038/ncomms15679) - Property-labelled materials fragments (PLMF) as universal descriptors for inorganic crystals (Isayev et al., 2017, Nature Communications).
* [Machine learning reveals orbital interaction in materials](https://doi.org/10.1080/14686996.2017.1378060) - Orbital-field matrix descriptor built from valence-orbital occupations of coordinating atoms (Lam Pham et al., 2017, Science and Technology of Advanced Materials).
* [Representation of compounds for machine-learning prediction of physical properties](https://doi.org/10.1103/PhysRevB.95.144110) - Compositional and structural representations for ML prediction of compound properties (Seko et al., 2017, Physical Review B).
* [Including crystal structure attributes in machine learning models of formation energies via Voronoi tessellations](https://doi.org/10.1103/PhysRevB.96.024104) - Voronoi-tessellation-based crystal structure attributes combined with composition features (Ward et al., 2017, Physical Review B).
* [Machine learning with force-field-inspired descriptors for materials: Fast screening and mapping energy landscape](https://doi.org/10.1103/PhysRevMaterials.2.083801) - Classical force-field inspired descriptors (CFID) for ML of material properties (Choudhary et al., 2018, Physical Review Materials).
* [Local structure order parameters and site fingerprints for quantification of coordination environment and crystal structure similarity](https://doi.org/10.1039/C9RA07755C) - Local structure order parameters / site fingerprints for coordination environments (Zimmermann et al., 2020, RSC Advances).
* [Unified representation of molecules and crystals for machine learning](https://doi.org/10.1088/2632-2153/aca005) - Many-body tensor representation (MBTR) for molecules and crystals (Huo et al., 2022, Machine Learning: Science and Technology).
* [The pointwise distance distribution is stronger than the pair distribution function](https://doi.org/10.1107/s2053273322090386) - Shows pointwise distance distributions are a stronger crystal invariant than the pair distribution function (Kurlin et al., 2022, Acta Crystallographica Section A Foundations and Advances).
* [Average minimum distances of periodic point sets – foundational invariants for mapping periodic crystals](https://doi.org/10.46793/match.87-3.529w) - Average minimum distance (AMD) isometry invariants for comparing periodic crystals (Widdowson et al., 2022, MATCH Communications in Mathematical and in Computer Chemistry). [[code](https://github.com/dwiddo/average-minimum-distance)]
* [Pointwise Distance Distributions for Detecting Near-Duplicates in Large Materials Databases](https://doi.org/10.1137/25m1736657) - Applies pointwise distance distributions to detect near-duplicate crystals in materials databases (Widdowson et al., 2026, SIAM Journal on Applied Mathematics).

### Structure descriptors: electronic charge density

* [Towards Universal Material Property Prediction with Deep Learning and Single-Descriptor electronic Density](https://arxiv.org/abs/2510.13207) - A deep-learning framework that uses the electronic charge density as its single descriptor predicts eight material properties (R2 up to 0.94), with accuracy improving as more properties are learned jointly (Chen et al., 2025, arXiv).

### Structure-based: oxidation states

* [Oxidation states in solids from data-driven paradigms](https://doi.org/10.1039/d5sc05694b) - TOSS, a data-driven Bayesian approach that computes oxidation states for large-scale crystal datasets with high accuracy and provides labels for machine-learning alternatives (Yin et al., 2025, Chemical Science).

### Symbolic regression

* [Big Data of Materials Science: Critical Role of the Descriptor](https://doi.org/10.1103/PhysRevLett.114.105503) - Compressed-sensing approach to find physically meaningful descriptors for crystal structure energetics (Ghiringhelli et al., 2015, Physical Review Letters).
* [SISSO: A compressed-sensing method for identifying the best low-dimensional descriptor in an immensity of offered candidates](https://doi.org/10.1103/PhysRevMaterials.2.083802) - SISSO: sure independence screening and sparsifying operator for descriptor identification (Ouyang et al., 2018, Physical Review Materials). [[code](https://github.com/rouyang2017/SISSO)]
* [New tolerance factor to predict the stability of perovskite oxides and halides](https://doi.org/10.1126/sciadv.aav0693) - SISSO-derived tolerance factor for predicting perovskite stability (Bartel et al., 2019, Science Advances).
* [Simultaneous learning of several materials properties from incomplete databases with multi-task SISSO](https://doi.org/10.1088/2515-7639/ab077b) - Multi-task SISSO learning several properties from incomplete databases (Ouyang et al., 2019, Journal of Physics: Materials).
* [SISSO++: A C++ Implementation of the Sure-Independence Screening and Sparsifying Operator Approach](https://doi.org/10.21105/joss.03960) - SISSO++: C++/Python implementation of SISSO (Purcell et al., 2022, Journal of Open Source Software). [[code](https://gitlab.com/sissopp_developers/sissopp)]
* [Recent advances in the SISSO method and their implementation in the SISSO++ code](https://doi.org/10.1063/5.0156620) - Reviews recent SISSO advances and their implementation in SISSO++ (Purcell et al., 2023, The Journal of Chemical Physics). [[code](https://gitlab.com/sissopp_developers/sissopp)]
* [A high-performance and portable implementation of the SISSO method for CPUs and GPUs](https://doi.org/10.1088/2632-2153/ae0ab3) - High-performance portable SISSO implementation for CPUs and GPUs (Eibl et al., 2025, Machine Learning: Science and Technology).

### Topological descriptors

* [Quantifying similarity of pore-geometry in nanoporous materials](https://doi.org/10.1038/ncomms15396) - Uses persistent homology to quantify pore-geometry similarity in nanoporous materials (Lee et al., 2017, Nature Communications).
* [Topological representations of crystalline compounds for the machine-learning prediction of materials properties](https://doi.org/10.1038/s41524-021-00493-w) - Persistent-homology-based topological representations for material property prediction (Jiang et al., 2021, npj Computational Materials).
* [Machine learning with persistent homology and chemical word embeddings improves prediction accuracy and interpretability in metal-organic frameworks](https://doi.org/10.1038/s41598-021-88027-8) - Combines persistent homology with chemical word embeddings for crystal property prediction (Krishnapriyan et al., 2021, Scientific Reports).

### Wyckoff representations

* [Rapid discovery of stable materials by coordinate-free coarse graining](https://doi.org/10.1126/sciadv.abn4117) - Wren: Wyckoff-representation model enabling structure-agnostic stability prediction (Goodall et al., 2022, Science Advances). [[code](https://github.com/CompRhys/aviary)]
* [Equivariant Parameter Sharing for Porous Crystalline Materials](https://arxiv.org/abs/2304.01628) - Space-group-equivariant parameter sharing for property prediction of porous crystals (Petković et al., 2023, arXiv).
* [SLICES-PLUS: A crystal representation leveraging spatial symmetry](https://doi.org/10.1016/j.matdes.2025.113856) - Symmetry-augmented string crystal representation used for property prediction and design (Wang et al., 2025, Materials & Design).
* [A Single Architecture for Representing Invariance Under Any Space Group](https://arxiv.org/abs/2512.13989) - Proposes one architecture enforcing invariance under arbitrary space groups (Zhang et al., 2025, arXiv).

## Representation Learning

### Composition embedding: doped materials

* [Predicting thermoelectric properties from chemical formula with explicitly identifying dopant effects](https://doi.org/10.1038/s41524-021-00564-y) - DopNet embeds host materials and dopants separately and predicts experimentally measured thermoelectric properties, reaching an MAE of 0.06 in ZT and extrapolating better to unknown materials than existing methods (Na et al., 2021, npj Computational Materials).

### Composition embedding: oxidation states

* [Composition Based Oxidation State Prediction of Materials Using Deep Learning Language Models](https://doi.org/10.1002/advs.202301011) - BERTOS, a BERT transformer that predicts the oxidation states of all elements from composition alone, reaching 96.82% accuracy on cleaned ICSD data and 97.61% on oxides, and used to screen hypothetical compositions (Fu et al., 2023, Advanced Science).

### Learned composition embeddings

* [ElemNet: Deep Learning the Chemistry of Materials From Only Elemental Composition](https://doi.org/10.1038/s41598-018-35934-y) - Deep network that learns from raw elemental fractions to predict formation enthalpy without hand-crafted features (Jha et al., 2018, Scientific Reports). [[code](https://github.com/NU-CUCIS/ElemNet)]
* [Learning atoms for materials discovery](https://doi.org/10.1073/pnas.1801181115) - Atom2Vec: learns atom vectors from database co-occurrence statistics (Zhou et al., 2018, Proceedings of the National Academy of Sciences).
* [Unsupervised word embeddings capture latent knowledge from materials science literature](https://doi.org/10.1038/s41586-019-1335-8) - Learns word embeddings (mat2vec) from materials science abstracts that encode chemical knowledge (Tshitoyan et al., 2019, Nature). [[code](https://github.com/materialsintelligence/mat2vec)]
* [Compositionally restricted attention-based network for materials property predictions](https://doi.org/10.1038/s41524-021-00545-1) - CrabNet: transformer attention over element embeddings with fractional encoding for composition-based prediction (Wang et al., 2021, npj Computational Materials). [[code](https://github.com/anthony-wang/CrabNet)]
* [Distributed representations of atoms and materials for machine learning](https://doi.org/10.1038/s41524-022-00729-3) - SkipAtom: distributed atom representations learned from crystal structure contexts (Antunes et al., 2022, npj Computational Materials). [[code](https://github.com/lantunes/skipatom)]
* [Formula Graph Self‐Attention Network for Representation‐Domain Independent Materials Discovery](https://doi.org/10.1002/advs.202200164) - Formula graph self-attention network for composition-based and structure-based prediction (Ihalage et al., 2022, Advanced Science).

### Multimodal representations

* [Lattice Lingo: Effect of Textual Detail on Multimodal Learning for Property Prediction of Crystals](https://arxiv.org/abs/2412.04670) - Studies how textual detail affects multimodal structure-text learning for crystal properties (Munjal et al., 2024, arXiv).
* [MatMMFuse: Multimodal fusion model for material property prediction](https://doi.org/10.1088/2632-2153/ae1927) - Multimodal fusion of crystal graph and text embeddings for property prediction (Bhattacharya et al., 2025, Machine Learning: Science and Technology).
* [CAST: Cross Attention based multimodal fusion of Structure and Text for materials property prediction](https://arxiv.org/abs/2502.06836) - Cross-attention fusion of graph-based structure and text embeddings for property prediction (Lee et al., 2025, arXiv).

### Self-supervised learning

* [Graph Contrastive Learning for Materials](https://arxiv.org/abs/2211.13408) - Applies graph contrastive pretraining to crystal graph networks for property prediction (Koker et al., 2022, arXiv).
* [Self-supervised learning for crystal property prediction via denoising](https://arxiv.org/abs/2408.17255) - Self-supervised denoising pretraining of crystal models for property prediction (New et al., 2024, arXiv).
* [Supervised pretraining for material property prediction](https://doi.org/10.1038/s43246-025-00999-6) - Pretrains crystal GNNs with surrogate labels as an alternative to purely self-supervised pretraining (Rahman et al., 2025, Communications Materials).
* [DISTAL: Distillation and Self-Supervised Pretraining for Structure-Agnostic Materials Property Prediction](https://arxiv.org/abs/2609.00059) - Dual-prior framework combining distillation and self-supervised pretraining for structure-agnostic property prediction in low-data settings (Wang et al., 2026, arXiv).
* [CLOUD: A Scalable and Physics-Informed Foundation Model for Crystal Representation Learning](https://doi.org/10.1038/s41467-026-70467-3) - Pretrains a foundation model on unlabeled crystal structures to learn transferable crystal representations for property prediction (Xu et al., 2026, Nature Communications).

### Text and LLM embeddings

* [Regression with Large Language Models for Materials and Molecular Property Prediction](https://arxiv.org/abs/2409.06080) - Studies LLM-based regression for materials and molecular property prediction (Jacobs et al., 2024, arXiv).
* [Leveraging language representation for materials exploration and discovery](https://doi.org/10.1038/s41524-024-01231-8) - Uses language-model embeddings of materials for recall and ranking in materials discovery (Qu et al., 2024, npj Computational Materials).
* [ZEBRA‐Prop: A Zero‐Shot Embedding‐Based Rapid and Accessible Regression Model for Materials Properties](https://doi.org/10.1002/aisy.70592) - Extends LLM-Prop by regressing properties from frozen LLM embeddings of crystal text descriptions without fine-tuning (Yamamoto et al., 2026, Advanced Intelligent Systems).

## Machine Learning Models

### Classical ML

* [Accelerating materials property predictions using machine learning](https://doi.org/10.1038/srep02810) - Kernel ridge regression with fingerprints to predict polymer-chain electronic properties (Pilania et al., 2013, Scientific Reports).
* [Combinatorial screening for new materials in unconstrained composition space with machine learning](https://doi.org/10.1103/PhysRevB.89.094104) - Composition-based ML (decision trees) screening ternary compounds for thermodynamic stability (Meredig et al., 2014, Physical Review B).
* [Machine learning with systematic density-functional theory calculations: Application to melting temperatures of single- and binary-component solids](https://doi.org/10.1103/PhysRevB.89.054303) - Kernel and Gaussian process regression on DFT-derived descriptors for melting temperatures (Seko et al., 2014, Physical Review B).
* [A Statistical Learning Framework for Materials Science: Application to Elastic Moduli of k-nary Inorganic Polycrystalline Compounds](https://doi.org/10.1038/srep34256) - Gradient-boosting framework predicting bulk and shear moduli of k-nary inorganic compounds from composition and structure descriptors (de Jong et al., 2016, Scientific Reports).

### Crystal transformers

* [CrystalFramer: Rethinking the Role of Frames for SE(3)-Invariant Crystal Structure Modeling](https://arxiv.org/abs/2503.02209) - Introduces dynamic, task-adaptive frames for SE(3)-invariant crystal modeling and builds them into the Crystalformer architecture, improving property prediction over static-frame baselines (Ito et al., 2025, ICLR 2025).

### Crystal transformers: Wyckoff representation

* [Wyckoff Transformer: Generation of Symmetric Crystals](https://arxiv.org/abs/2503.02407) - Introduces WyFormer, a transformer over a discrete Wyckoff-position representation conditioned on space group, used to generate symmetric crystals and (via the same representation) to predict properties (Kazeev et al., 2025, Proceedings of the 42nd International Conference on Machine Learning (ICML 2025)). [[code](https://github.com/SymmetryAdvantage/WyckoffTransformer)]

### Defects: structure relaxation

* [Constrained Diffusion for Accelerated Structure Relaxation of Inorganic Solids with Point Defects](https://arxiv.org/abs/2602.19153) - Proposes a primal-dual constraint-aware diffusion model to relax point-defect structures in inorganic solids, evaluated on six Bi2Te3 defect settings (Cui et al., 2025, NeurIPS 2025 AI4Mat workshop).

### Dielectric and piezoelectric: Born effective charges

* [Representing Born effective charges with equivariant graph convolutional neural networks](https://doi.org/10.1038/s41598-025-01250-5) - An equivariant graph convolutional network with equivariant weights and descriptors outputs per-atom Born effective charge tensors directly, showing good accuracy and generalization on perovskite oxides, Li3PO4 and ZrO2 (Kutana et al., 2025, Scientific Reports).

### Dielectric and piezoelectric: edge-based tensor GNN

* [A General Tensor Prediction Framework Based on Graph Neural Networks](https://doi.org/10.1021/acs.jpclett.3c01200) - ETGNN writes crystal tensors as sums of invariant-GNN coefficients multiplying edge-direction projections, which gives rotational equivariance without an equivariant backbone, and predicts Born effective charges and dielectric and piezoelectric tensors on JARVIS-DFT accurately (Zhong et al., 2023, The Journal of Physical Chemistry Letters).

### Dielectric and piezoelectric: electronic dielectric constant

* [Modeling the dielectric constants of crystals using machine learning](https://doi.org/10.1063/5.0013136) - SVR and deep neural networks trained on 1,364 DFPT optical (electronic) dielectric constants predict epsilon_inf, and SHAP analysis shows they recover Clausius-Mossotti and Penn-model trends while beating those analytical models in accuracy (Morita et al., 2020, The Journal of Chemical Physics).

### Dielectric and piezoelectric: equivariant dielectric tensor

* [Dielectric tensor prediction for inorganic materials using latent information from preferred potential](https://doi.org/10.1038/s41524-024-01450-z) - An O(3)-equivariant readout on multi-rank embeddings from a pretrained universal neural network potential predicts total, electronic and ionic dielectric tensors and, in screening of stable Materials Project compounds, flags candidates such as Cs2Ti(WO4)3 (Eg = 2.93 eV, epsilon = 180.9) and CsZrCuSe3 (anisotropy ratio 121.9) (Mao et al., 2024, npj Computational Materials).
* [Discovery of highly anisotropic dielectric crystals with equivariant graph neural networks](https://doi.org/10.1039/d4fd00096j) - An equivariant GNN trained on about 6,700 Materials Project DFPT dielectric tensors predicts the full tensor, reaches state-of-the-art accuracy on the scalar dielectric constant and is used to discover crystals with nearly isotropic connectivity but highly anisotropic dielectric response (Lou et al., 2025, Faraday Discussions).

### Dielectric and piezoelectric: field-aware MLIP

* [Unified differentiable learning of electric response](https://doi.org/10.1038/s41467-025-59304-1) - An equivariant (Allegro-based) potential treats the electric enthalpy as a function of the applied field, so polarization, Born charges and polarizability come out as exact derivatives, reproducing alpha-SiO2 vibrational and dielectric properties and the temperature-dependent hysteresis and domain switching of ferroelectric BaTiO3 (Falletta et al., 2025, Nature Communications).
* [General Learning of the Electric Response of Inorganic Materials](https://doi.org/10.1103/b116-xy8k) - MACE-Field couples a uniform electric field to MACE's equivariant features so that polarization, Born charges and polarizability follow by differentiating one electric-enthalpy functional, and fine-tuning the mace-mp-mh-0 foundation model gives cross-chemistry Z*, epsilon_inf and spontaneous-polarization predictions plus BaTiO3 hysteresis and alpha-quartz IR, Raman and dielectric spectra comparable to DFPT (Martin et al., 2026, PRX Intelligence).

### Dielectric and piezoelectric: frequency-dependent dielectric function

* [Deep learning of spectra: Predicting the dielectric function of semiconductors](https://doi.org/10.1103/PhysRevMaterials.8.L122201) - Builds an IPA database of 9,915 frequency-dependent dielectric tensors and trains OptiMate graph attention networks that predict the dielectric function and refractive index spectra from the crystal structure alone, giving smooth, artifact-free curves (Grunert et al., 2024, Physical Review Materials).
* [Screening for wide-gap, high-refractive-index materials via frequency-dependent dielectric function prediction aided by convolutional autoencoders](https://doi.org/10.1103/dg72-zpqn) - Builds a database of about 30,000 IPA frequency-dependent dielectric functions (PBE and TASK), compresses the spectra about 50-fold with convolutional autoencoders so they are cheap to predict, and uses the models to screen for wide-gap, high-refractive-index materials (Borlido et al., 2026, Physical Review Materials).

### Dielectric and piezoelectric: high-kappa screening

* [Discovery of high-performance dielectric materials with machine-learning-guided search](https://doi.org/10.1016/j.xcrp.2024.102241) - Element substitution, ML pre-screening of band gap and permittivity on a concave Pareto front, DFPT and expert triage led to the synthesis of two dielectrics, CsTaTeO6 and Bi2Zr2O7 (band gap 2.27 eV, permittivity 20.5), the authors' claimed first experimentally confirmed ML-guided multi-objective materials discovery (Riebesell et al., 2024, Cell Reports Physical Science).

### Dielectric and piezoelectric: ionic dielectric tensor

* [Physics-Based Factorized Machine Learning for Predicting Ionic Dielectric Tensors](https://doi.org/10.1103/28wr-w896) - Factorizes the ionic dielectric tensor into equivariant-GNN Born effective charges and phonons from a pretrained ML potential, combined analytically, which substantially improves ionic-contribution accuracy and identifies 31 new high-kappa oxides from over 8,000 candidates (Takigawa et al., 2026, Physical Review X).

### Dielectric and piezoelectric: optical dielectric function

* [Universal Ensemble-Embedding Graph Neural Network for Direct Prediction of Optical Spectra from Crystal Structures](https://doi.org/10.1002/adma.202409175) - GNNOpt, an equivariant GNN with ensemble universal atom embeddings, is trained on only 944 materials and predicts the complex dielectric function, refractive index, absorption and reflectance (Kramers-Kronig-consistent), then screens photovoltaic absorbers and high-quantum-weight materials with DFT validation (Hung et al., 2024, Advanced Materials).

### Dielectric and piezoelectric: piezoelectric modulus

* [Piezoelectric modulus prediction using machine learning and graph neural networks](https://doi.org/10.1016/j.cplett.2022.139359) - Compares engineered composition and structure features with random forests, SVMs and GNNs for the scalar piezoelectric modulus, finds an SVM on crystal-structure features works best, and uses it to rank 12,680 Materials Project compounds and report the top 20 candidates (Hu et al., 2022, Chemical Physics Letters).

### Dielectric and piezoelectric: piezoelectric screening

* [Discovery of wurtzite solid solutions with enhanced piezoelectric response using machine learning](https://doi.org/10.1103/physrevmaterials.8.055406) - A multilevel ML, chemical-intuition and thermodynamics screening protocol over more than 3,000 ternary wurtzite solid solutions from nine base systems (AlN, GaN, ZnO and others) predicts 11 materials with improved piezoelectric response driven by electropositive dopants (Behrendt et al., 2024, Physical Review Materials).

### Dielectric and piezoelectric: refractive index screening

* [High-refractive-index materials screening from machine learning and ab initio methods](https://doi.org/10.1103/physrevmaterials.8.015201) - Uses crystal graph convolutional networks with DFPT verification to screen a large recent dataset for wide-gap, high-refractive-index materials, confirming the inverse gap-dielectric trend while finding candidates competitive with industry standards (Carriço et al., 2024, Physical Review Materials).

### Equivariant

* [Directional Message Passing for Molecular Graphs](https://arxiv.org/abs/2003.03123) - Directional message passing network embedding interatomic distances and angles (DimeNet) (Gasteiger et al., 2020, ICLR 2020). [[code](https://github.com/gasteigerjo/dimenet)]
* [GemNet: Universal Directional Graph Neural Networks for Molecules](https://arxiv.org/abs/2106.08903) - Geometric message passing with two-hop and dihedral information (GemNet) proven universal for directional GNNs (Gasteiger et al., 2021, NeurIPS 2021). [[code](https://github.com/TUM-DAML/gemnet_pytorch)]
* [Equivariant message passing for the prediction of tensorial properties and molecular spectra](https://arxiv.org/abs/2102.03150) - Polarizable atom interaction network (PaiNN) with equivariant vector features for tensorial properties and spectra (Schütt et al., 2021, ICML 2021). [[code](https://github.com/atomistic-machine-learning/schnetpack)]
* [MACE: Higher Order Equivariant Message Passing Neural Networks for Fast and Accurate Force Fields](https://doi.org/10.52202/068431-0830) - Higher-body-order equivariant message passing (MACE) for fast and accurate force fields (Batatia et al., 2022, Advances in Neural Information Processing Systems 35). [[code](https://github.com/ACEsuit/mace)]
* [E(3)-equivariant graph neural networks for data-efficient and accurate interatomic potentials](https://doi.org/10.1038/s41467-022-29939-5) - E(3)-equivariant interatomic potential (NequIP) achieving high data efficiency (Batzner et al., 2022, Nature Communications). [[code](https://github.com/mir-group/nequip)]
* [e3nn: Euclidean Neural Networks](https://arxiv.org/abs/2207.09453) - Library for building E(3)-equivariant neural networks from irreducible representations (Geiger et al., 2022, arXiv). [[code](https://github.com/e3nn/e3nn)]
* [Equivariant Networks for Crystal Structures](https://doi.org/10.52202/068431-0300) - Equivariant networks for crystal structures respecting space-group symmetries (Kaba et al., 2022, Advances in Neural Information Processing Systems 35).
* [EquiformerV2: Improved Equivariant Transformer for Scaling to Higher-Degree Representations](https://arxiv.org/abs/2306.12059) - Equivariant transformer scaling to higher-degree representations using eSCN convolutions (Liao et al., 2023, ICLR 2024). [[code](https://github.com/atomicarchitects/equiformer_v2)]
* [Learning local equivariant representations for large-scale atomistic dynamics](https://doi.org/10.1038/s41467-023-36329-y) - Strictly local equivariant potential (Allegro) enabling scalable large-scale molecular dynamics (Musaelian et al., 2023, Nature Communications). [[code](https://github.com/mir-group/allegro)]
* [Learning Smooth and Expressive Interatomic Potentials for Physical Property Prediction](https://arxiv.org/abs/2502.12147) - Smooth, expressive equivariant potential (eSEN) designed for accurate physical property prediction such as phonons and thermal conductivity (Fu et al., 2025, ICML 2025). [[code](https://github.com/facebookresearch/fairchem)]

### Equivariant networks: porous frameworks

* [Interpretable Nanoporous Materials Design with Symmetry-Aware Networks](https://arxiv.org/abs/2509.15908) - Introduces a site-resolved equivariant framework based on periodic space sampling that predicts reticular-framework properties and attributes them to local sites (Zhou et al., 2025, arXiv).

### Explainability: attention analysis

* [CrabNet for Explainable Deep Learning in Materials Science: Bridging the Gap Between Academia and Industry](https://doi.org/10.1007/s40192-021-00247-y) - Shows that the composition transformer CrabNet learns property-specific element representations without extra supervision, and that its element embeddings and attention maps reveal chemical trends and expose modelling or dataset errors (Wang et al., 2022, Integrating Materials and Manufacturing Innovation). [[code](https://github.com/anthony-wang/CrabNet)]

### Explainability: concept-based GNN (recovering physics)

* [Interpretable Graph Neural Networks for Classifying Structure and Magnetism in Delafossite Compounds](https://arxiv.org/abs/2512.00292) - A concept-whitening graph neural network classifies delafossite stacking and magnetic order (>80% validation accuracy) while aligning latent axes with nine physical descriptors; concept alignment reaches R2 of about 0.6 for d-shell valence-electron concepts and 0.4-0.5 for magnetic-coupling parameters (Joseph et al., 2025, arXiv preprint).

### Explainability: critique (architecture dependence; validation against physics)

* [Can end-to-end learning from raw electronic structure explain magnetic anisotropy?](https://arxiv.org/abs/2610.11742) - A GRU and a 1D CNN trained to predict magnetic anisotropy energy from spin- and orbital-resolved DOS reach similar in-domain accuracy but learn only partly overlapping dependencies; their shared SHAP features match spin-orbit pathways from second-order perturbation theory, yet controlled spectral perturbations show that similar attribution patterns do not imply the same functional dependence (Topolnicki et al., 2026, arXiv preprint).

### Explainability: critique (attribution instability)

* [Robustness of Local Predictions in Atomistic Machine Learning Models](https://doi.org/10.1021/acs.jctc.3c00704) - Points out that only the global target is rigorously defined, so atom-centred contributions used for post hoc interpretation depend on training data and architecture; introduces the local prediction rigidity (LPR) metric to quantify this and gives strategies to make local predictions more robust (Chong et al., 2023, Journal of Chemical Theory and Computation).

### Explainability: critique (explainer disagreement)

* [The Disagreement Problem in Explainable Machine Learning: A Practitioner's Perspective](https://arxiv.org/abs/2202.01602) - Across four datasets, six post hoc explanation methods (e.g. SHAP, LIME, gradient-based) and six models, popular explainers often disagree about the same prediction, and practitioners settle these disagreements with ad hoc heuristics; a domain-general warning that applies directly to SHAP and gradient attributions in materials models (Krishna et al., 2022, arXiv preprint).

### Explainability: explainable crystal GNN

* [CrysXPP: An explainable property predictor for crystalline materials](https://doi.org/10.1038/s41524-022-00716-8) - Crystal-graph model that pairs a pretrained autoencoder (CrysAE) with a learned feature selector for interpretable predictions of electronic, magnetic and elastic properties, beating baselines on seven properties and outperforming DFT when fine-tuned on small experimental datasets (Das et al., 2022, npj Computational Materials). [[code](https://github.com/kdmsit/crysxpp)]

### Explainability: feature attribution consensus on descriptor models

* [Explainable machine learning for oxygen diffusion in perovskites and pyrochlores](https://doi.org/10.1103/k947-srvp) - Builds a database of experimental activation energies and uses consensus feature importance across seven models to explain them: A-site bond ionicity and O2 partial pressure dominate for perovskites, and A-site s-valence count and B-site electronegativity for pyrochlores; unexpectedly, elemental-metal averages outrank features of the constituent binary oxides (Lu et al., 2025, Physical Review Materials).

### Explainability: perspective (causality)

* [Towards physics-informed explainable machine learning and causal models for materials research](https://doi.org/10.1016/j.commatsci.2023.112740) - Perspective tracing the move from shallow data-driven models to graph, symbolic and invariant models, and arguing that explainable and interpretable predictions should be combined with causal learning for materials design and autonomous experiments, with case studies on functional materials (Ghosh et al., 2024, Computational Materials Science).

### Explainability: relevance propagation for GNN potentials

* [Peering inside the black box by learning the relevance of many-body functions in neural network potentials](https://doi.org/10.1038/s41467-025-65863-0) - Extends GNN layer-wise relevance propagation to decompose graph neural network potentials into n-body relevance contributions without losing accuracy; on coarse-grained methane, water and the NTL9 protein (not crystals), the recovered interactions agree with physical principles (Bonneau et al., 2025, Nature Communications).

### Explainability: reliability-explainability trade-off

* [Reliable and explainable machine-learning methods for accelerated material discovery](https://doi.org/10.1038/s41524-019-0248-2) - Shows that on imbalanced materials data, standard metrics and model confidence scores mislead and that introspection with simpler surrogate models costs predictive performance; proposes an ensemble of simple models with transfer learning, a trust score and a rationale generator for crystalline-compound and solar-cell screening (Kailkhura et al., 2019, npj Computational Materials).

### Explainability: review

* [Interpretable and Explainable Machine Learning for Materials Science and Chemistry](https://doi.org/10.1021/accountsmr.1c00244) - Account surveying interpretability and explainability techniques in materials science and chemistry that explicitly warns against inferring causation or generalization from model interpretations and calls for uncertainty estimates on explanations (Oviedo et al., 2022, Accounts of Materials Research).
* [Explainable machine learning in materials science](https://doi.org/10.1038/s41524-022-00884-7) - Entry-point review of explainable AI for materials scientists that defines what "explain" means in a materials context, surveys XAI applications (saliency, attribution, surrogate models) and lays out challenges and opportunities (Zhong et al., 2022, npj Computational Materials).

### Foundation models: analysis of force-field-pretrained latent features

* [Comparing the Latent Features of Universal Machine-Learning Interatomic Potentials](https://doi.org/10.1002/aisy.202501497) - Uses feature reconstruction errors to compare latent features of several universal MLIPs and finds that they encode chemical space in quite different ways that depend on training data, target and protocol, and that fine-tuned uMLIPs keep a strong pretraining bias, a caution for using uMLIP embeddings as generic property descriptors (Sofiia Chorna et al., 2026, Advanced Intelligent Systems).

### Foundation models: denoising autoencoder + contrastive atom embeddings

* [UNATE: UNsupervised ATomic Embedding for crystal structures property prediction](https://arxiv.org/abs/2605.25866) - Learns atom embeddings from about 139,000 unlabeled crystal graphs with a denoising autoencoder plus contrastive learning; replacing raw atomic numbers with these embeddings gives a 2.7% improvement with full data and up to 10% with 25% of the labels (Laura Solà-Garcia et al., 2026, arXiv preprint). [[code](https://github.com/LauraSola/Unsupervised-Atom-Embedding-Gen)]

### Foundation models: diffusion-based structure reconstruction

* [A Diffusion-Based Pre-training Framework for Crystal Property Prediction](https://doi.org/10.1609/aaai.v38i8.28748) - CrysDiff learns the marginal distribution of unlabeled crystal structures through a symmetry-aware (rotation, reflection, periodic translation invariant) diffusion reconstruction task, then fine-tunes toward the property-conditional distribution, and reports outperforming earlier crystal pretraining models on JARVIS-DFT properties (Zixing Song et al., 2024, Proceedings of the AAAI Conference on Artificial Intelligence (AAAI 2024)).

### Foundation models: distillation

* [Towards Fast, Specialized Machine Learning Force Fields: Distilling Foundation Models via Energy Hessians](https://arxiv.org/abs/2501.09009) - Distills large MLFF foundation models into fast specialized students by matching energy Hessians, giving large inference speedups while preserving accuracy on target systems (Amin et al., 2025, ICLR 2025). [[code](https://github.com/ASK-Berkeley/MLFF-distill)]

### Foundation models: fine-tuning

* [ELoRA: Low-Rank Adaptation for Equivariant GNNs](https://proceedings.mlr.press/v267/wang25al.html) - Proposes an equivariance-preserving low-rank adaptation (path-dependent decomposition) for SO(3)-equivariant GNN interatomic potentials, improving energy/force accuracy over full fine-tuning on rMD17 and 10 inorganic datasets (Wang et al., 2025, ICML 2025). [[code](https://github.com/hyjwpk/ELoRA)]
* [Robust and Interpretable Adaptation of Equivariant Materials Foundation Models via Sparsity-promoting Fine-tuning](https://arxiv.org/abs/2606.18691) - Proposes sparsity-promoting fine-tuning that selectively updates parameters of E(3)-equivariant materials foundation models, matching or surpassing full fine-tuning on molecular and crystalline benchmarks (Cho et al., 2026, ICLR 2026).

### Foundation models: frozen uMLIP (force-field) embeddings as features

* [Leveraging neural network interatomic potentials for a foundation model of chemistry](https://doi.org/10.1038/s41524-026-02167-x) - HackNIP extracts fixed-length embeddings from pretrained universal NIPs (ORB, EquiformerV2, MACE) and trains shallow learners (MODNet, XGBoost, MLP), matching or exceeding the Matbench leaderboard on several tasks and matching or beating direct ORB fine-tuning on four of five tasks at about 10^4 samples (bulk modulus 18% better, band gap worse) (So Yeon Kim et al., 2026, npj Computational Materials). [[code](https://github.com/parkyjmit/HackNIP)]

### Foundation models: frozen uMLIP (MACE) embeddings as features

* [Transfer learning on universal interatomic potential embeddings improves generalization in structure-property defect models](https://doi.org/10.26434/chemrxiv.15003938/v2) - A small MLP on frozen 256-dimensional MACE universal-potential embeddings predicts DFT oxygen-vacancy formation energies of oxides with an element-wise cross-validation MAE of 0.38 eV, versus 0.72 eV for a GNN trained from scratch and 0.51 eV for direct MACE relaxations (Matthew D. Witman et al., 2026, ChemRxiv preprint).

### Foundation models: graph-text contrastive

* [Graph-text contrastive learning of inorganic crystal structure toward a foundation model of inorganic materials](https://doi.org/10.1080/27660400.2024.2406219) - CLICS contrasts crystal graphs with texts describing local environments, connectivity and symmetry, and shows that the resulting embeddings support geometric concept prediction, similar-structure search and few-shot or imbalanced structure classification (Keisuke Ozawa et al., 2024, Science and Technology of Advanced Materials: Methods).

### Foundation models: latent diffusion (VAE + latent flow matching)

* [Latent Diffusion Pretraining for Crystal Property Prediction](https://arxiv.org/abs/2606.00776) - A VAE encoder plus latent diffusion pretrained on 380,740 GNoME crystals de-duplicated against downstream sets improves a PDDFormer backbone by 4.26% (JARVIS-DFT) and 4.90% (MP) average MAE, beats CrysDiff and DPF under matched backbones, and helps fine-tuning on about 1,500 experimental formation energies (Shrimon Mukherjee et al., 2026, ICML 2026 (arXiv preprint)). [[code](https://github.com/shrimonmuke0202/CrysLDNet)]

### Foundation models: masked atom types + coordinate and lattice denoising

* [A Denoising Pre-training Framework for Accelerating Novel Material Discovery](https://doi.org/10.1609/aaai.v39i27.35058) - Pretrains on 380,743 unlabeled crystals to recover masked atom types, perturbed positions and perturbed lattices, and reports gains over training from scratch when fine-tuned on Materials Project and JARVIS property tasks (Shuaike Shen et al., 2025, Proceedings of the AAAI Conference on Artificial Intelligence (AAAI 2025)). [[code](https://github.com/zjuKeLiu/DPF)]

### Foundation models: masked species/atom reconstruction with GAN discriminator

* [Self-supervised generative models for crystal structures](https://doi.org/10.1016/j.isci.2024.110672) - Pretrains an equivariant GNN on Materials Project structures to reconstruct masked species and atoms (with a GAN discriminator as cheap evaluator), and the pretrained model is then adapted to small property tasks and groups chemically similar elements without property labels (Fangze Liu et al., 2024, iScience). [[code](https://github.com/fangzel/CrystalGenerativeModels)]

### Foundation models: multimodal contrastive (structure, pXRD, DOS, text)

* [MatBind: a shared embedding space for multimodal materials characterization](https://doi.org/10.1038/s41524-026-02382-6) - Anchors simulated pXRD, total DOS and Robocrystallographer text to crystal structure for about 155k Materials Project materials, giving emergent zero-shot cross-modal retrieval and an embedding space organized by physical properties without supervision; it reports retrieval, not fine-tuned property regression (Le Yang et al., 2026, npj Computational Materials). [[code](https://github.com/HFMI-SOL-AI/MatBind)]

### Foundation models: multimodal contrastive alignment (structure, DOS, charge density, text)

* [Multimodal foundation models for material property prediction and discovery](https://doi.org/10.1016/j.newton.2025.100016) - MultiMat aligns crystal structure (PotNet encoder), DOS, charge density and Robocrystallographer text for about 154,000 Materials Project materials in a CLIP-style shared latent space; the pretrained structure encoder improves on PotNet and CGCNN for bulk modulus, shear modulus, elastic tensor (about 7,000 labels) and band gap (about 10,000 labels), and supports latent-space screening (Viggo Moro et al., 2025, Newton). [[code](https://github.com/vmoro1/multimat)]

### Foundation models: mutex masked-representation reconstruction

* [A Crystal-Specific Pre-Training Framework for Crystal Material Property Prediction](https://arxiv.org/abs/2306.05344) - Pretrains a periodic-invariant DimeNet++ multi-graph encoder on 817,139 OQMD structures with complementary (mutex) masks that reconstruct atom types, centroid distances and Niggli lattice parameters plus an atom-type Barlow Twins term, and is best on all 8 benchmarks (e.g. JDFT2D 38.2 vs Matformer 47.7 and Crystal Twins 44.4) (Haomin Yu et al., 2023, arXiv preprint).

### Foundation models: mutual-information maximization (Deep InfoMax)

* [Establishing Deep InfoMax as an effective self-supervised learning methodology in materials informatics](https://doi.org/10.1039/d4dd00202d) - Pretrains Site-Net on about 70k-89k Materials Project band-gap and formation-energy structures (Matbench) by maximizing mutual information between the crystal point set and its vector representation, and with label masking shows gains for representation learning and transfer to models trained on fewer than 10^3 labels (Michael Moran et al., 2025, Digital Discovery). [[code](https://github.com/lrcfmd/Site-Net-DeepInfoMax)]

### Foundation models: node masking + coordinate-perturbation contrastive + physics pretext

* [Physics-Guided Dual Self-Supervised Learning for Structure-Based Material Property Prediction](https://doi.org/10.1021/acs.jpclett.4c00100) - DSSL pretrains a DeeperGATGNN on unlabeled Materials Project structures with node-masking prediction, coordinate-perturbation contrastive learning and an atomic-stiffness pretext task, and improves fine-tuning on most of ten property datasets (but not all, e.g. one elastic task) (Nihang Fu et al., 2024, The Journal of Physical Chemistry Letters). [[code](https://github.com/usccolumbia/DSSL)]

### Foundation models: scaling laws

* [Scaling Laws of Graph Neural Networks for Atomistic Materials Modeling*](https://doi.org/10.1109/dac63849.2025.11132864) - Systematically varies GNN model size and dataset size for atomistic materials modeling to characterize scaling behavior (Li et al., 2025, 2025 62nd ACM/IEEE Design Automation Conference (DAC)).
* [Scaling Laws for Neural Material Models](https://arxiv.org/abs/2509.21811) - Fits empirical scaling laws in training data, model size (1e2 to 1e9 parameters) and compute for transformer and EquiformerV2 models predicting energies, forces and stresses on OMat24 (Trikha et al., 2025, arXiv).
* [Are Scaling Laws of Universal MLIPs Universal?](https://arxiv.org/abs/2611.15603) - Studies data scaling of M3GNet, MACE and PET on subsets of a MatPES/MP-ALOE pool and compares random, stratified, DIRECT and furthest-point sampling policies (Keane et al., 2026, NeurIPS 2026 AI4Mat workshop).

### Foundation models: self-conditioned coordinate denoising

* [Self-Conditioned Denoising for Atomistic Representation Learning](https://arxiv.org/abs/2603.17196) - Backbone-agnostic denoising in which a clean-structure self-embedding conditions the denoiser, pretrained on Alex-MP-20 (about 0.6-0.7M periodic structures) and on molecular and protein sets of up to 5.2M structures; controlled for backbone and data, it beats prior SSL objectives and matches supervised force-energy pretraining on average (e.g. Matbench mp_gap 0.136 vs 0.134 eV), although most materials numbers are single-fold (Tynan Perez et al., 2026, arXiv preprint). [[code](https://github.com/TyJPerez/SelfConditionedDenoisingAtoms)]

### Foundation models: structure-text contrastive (CLIP-style)

* [Bridging text and crystal structures: literature-driven contrastive learning for materials science](https://doi.org/10.1088/2632-2153/ade58c) - CLaSP contrastively aligns 406,048 COD crystal structures with the titles (and keyword captions from abstracts) of their source publications, giving embeddings that cluster by property and functionality and allow zero-shot text-query screening for property-related keywords such as superconductor, with no property labels used in pretraining (Yuta Suzuki et al., 2025, Machine Learning: Science and Technology). [[code](https://github.com/Toyota/clasp)]

### Foundation models: structure-text contrastive on LLM-generated synthetic narratives

* [Scaling multimodal materials representation learning with synthetic narratives](https://doi.org/10.1038/s41467-026-76378-7) - CLaC aligns crystal graphs with text using about 126k LLM-generated, property-conditioned structure-text pairs and gets better zero-shot cross-modal alignment and retrieval than the same model trained on literature-derived text; it does not report fine-tuned property regression (Yang Jeong Park et al., 2026, Nature Communications).

### Foundation models: weak labels from cheap structural fingerprints (wACSF, GMP, EAD)

* [Pre-training Graph Neural Networks with Structural Fingerprints for Materials Discovery](https://arxiv.org/abs/2503.01227) - Pretrains GNNs to regress cheaply computed atom-centered descriptors on 62,783 relaxed MP structures (no DFT labels needed), giving 15-17% mean MAE improvement over training from scratch across 11 downstream datasets (5% to 35% per dataset), comparable to force-field or denoising pretraining (Shuyi Jia et al., 2025, arXiv preprint). [[code](https://github.com/Fung-Lab/MatDeepLearn_dev)]

### Foundation/uMLIP

* [A universal graph deep learning interatomic potential for the periodic table](https://doi.org/10.1038/s43588-022-00349-3) - Universal graph interatomic potential (M3GNet) with three-body interactions trained on Materials Project relaxations (Chen et al., 2022, Nature Computational Science). [[code](https://github.com/materialsvirtuallab/matgl)]
* [Towards universal neural network potential for material discovery applicable to arbitrary combination of 45 elements](https://doi.org/10.1038/s41467-022-30687-9) - Preferred Potential (PFP), a universal neural network potential spanning 45 elements (Takamoto et al., 2022, Nature Communications).
* [A foundation model for atomistic materials chemistry](https://arxiv.org/abs/2401.00096) - MACE-MP-0 foundation potential trained on MPtrj and applied across diverse materials chemistry (Batatia et al., 2023, arXiv). [[code](https://github.com/ACEsuit/mace)]
* [Unified graph neural network force-field for the periodic table: solid state applications](https://doi.org/10.1039/D2DD00096B) - ALIGNN-FF unified force field for the periodic table trained on JARVIS-DFT (Choudhary et al., 2023, Digital Discovery). [[code](https://github.com/usnistgov/alignn)]
* [Forces are not Enough: Benchmark and Critical Evaluation for Machine Learning Force Fields with Molecular Simulations](https://arxiv.org/abs/2210.07237) - Shows force accuracy alone poorly predicts MD-simulation quality of ML force fields (Fu et al., 2023, Transactions on Machine Learning Research).
* [From Molecules to Materials: Pre-training Large Generalizable Models for Atomic Property Prediction](https://arxiv.org/abs/2310.16802) - Joint multi-domain pre-training (JMP) on molecules and catalysts transferable to materials property fine-tuning (Shoghi et al., 2023, ICLR 2024). [[code](https://github.com/facebookresearch/JMP)]
* [Graph Atomic Cluster Expansion for Semilocal Interactions beyond Equivariant Message Passing](https://doi.org/10.1103/PhysRevX.14.021036) - Graph atomic cluster expansion (GRACE) for semilocal interactions beyond equivariant message passing (Bochkarev et al., 2024, Physical Review X). [[code](https://github.com/ICAMS/grace-tensorpotential)]
* [Orb: A Fast, Scalable Neural Network Potential](https://arxiv.org/abs/2410.22570) - Fast, scalable non-equivariant neural network potential (Orb) for materials (Neumann et al., 2024, arXiv). [[code](https://github.com/orbital-materials/orb-models)]
* [Scalable Parallel Algorithm for Graph Neural Network Interatomic Potentials in Molecular Dynamics Simulations](https://doi.org/10.1021/acs.jctc.4c00190) - Spatial-decomposition parallel algorithm for GNN potentials, introducing SevenNet (Park et al., 2024, Journal of Chemical Theory and Computation). [[code](https://github.com/MDIL-SNU/SevenNet)]
* [MatterSim: A Deep Learning Atomistic Model Across Elements, Temperatures and Pressures](https://arxiv.org/abs/2405.04967) - Deep atomistic model (MatterSim) trained across elements, temperatures and pressures for property prediction (Yang et al., 2024, arXiv). [[code](https://github.com/microsoft/mattersim)]
* [DPA-2: a large atomic model as a multi-task learner](https://doi.org/10.1038/s41524-024-01493-2) - Large atomic model (DPA-2) pretrained with multi-task learning across many DFT datasets (Zhang et al., 2024, npj Computational Materials). [[code](https://github.com/deepmodeling/deepmd-kit)]
* [MatterTune: an integrated, user-friendly platform for fine-tuning atomistic foundation models to accelerate materials simulation and discovery](https://doi.org/10.1039/d5dd00154d) - Platform for fine-tuning atomistic foundation models (JMP, ORB, MatterSim, MACE, EqV2) on downstream property tasks (Kong et al., 2025, Digital Discovery). [[code](https://github.com/Fung-Lab/MatterTune)]
* [UMA: A Family of Universal Models for Atoms](https://doi.org/10.52202/085713-4310) - Mixture-of-linear-experts universal models for atoms (UMA) trained on multiple Meta datasets (Wood et al., 2025, Advances in Neural Information Processing Systems 38). [[code](https://github.com/facebookresearch/fairchem)]
* [A graph neural network for the era of large atomistic models](https://doi.org/10.1038/s41524-026-02146-2) - Line-graph-series GNN (DPA-3) for large atomistic models with scaling behavior (Zhang et al., 2026, npj Computational Materials). [[code](https://github.com/deepmodeling/deepmd-kit)]

### Invariant GNN

* [SchNet: A continuous-filter convolutional neural network for modeling quantum interactions](https://arxiv.org/abs/1706.08566) - Continuous-filter convolutional network for modeling quantum interactions in atomistic systems (Schütt et al., 2017, Advances in Neural Information Processing Systems 30 (NeurIPS 2017)). [[code](https://github.com/atomistic-machine-learning/schnetpack)]
* [SchNet – A deep learning architecture for molecules and materials](https://doi.org/10.1063/1.5019779) - Extends SchNet to periodic materials and demonstrates formation-energy prediction on Materials Project (Schütt et al., 2018, The Journal of Chemical Physics). [[code](https://github.com/atomistic-machine-learning/schnetpack)]
* [Crystal Graph Convolutional Neural Networks for an Accurate and Interpretable Prediction of Material Properties](https://doi.org/10.1103/PhysRevLett.120.145301) - Crystal graph convolutional neural network learning properties directly from atom connectivity in periodic crystals (Xie et al., 2018, Physical Review Letters). [[code](https://github.com/txie-93/cgcnn)]
* [Graph Networks as a Universal Machine Learning Framework for Molecules and Crystals](https://doi.org/10.1021/acs.chemmater.9b01294) - MatErials Graph Network with global state attributes for molecules and crystals property prediction (Chen et al., 2019, Chemistry of Materials). [[code](https://github.com/materialsvirtuallab/megnet)]
* [Graph convolutional neural networks with global attention for improved materials property prediction](https://doi.org/10.1039/D0CP01474E) - Graph attention network with global attention pooling (GATGNN) for crystal property prediction (Louis et al., 2020, Physical Chemistry Chemical Physics). [[code](https://github.com/superlouis/GATGNN)]
* [Developing an improved crystal graph convolutional neural network framework for accelerated materials discovery](https://doi.org/10.1103/PhysRevMaterials.4.063801) - Improves CGCNN with Voronoi-tessellation neighbors and three-body explicit interactions for stability prediction (Park et al., 2020, Physical Review Materials).
* [A geometric-information-enhanced crystal graph network for predicting properties of materials](https://doi.org/10.1038/s43246-021-00194-3) - Geometric-information-enhanced crystal graph network (GeoCGNN) encoding distance vectors and plane waves (Cheng et al., 2021, Communications Materials).
* [Atomistic Line Graph Neural Network for improved materials property predictions](https://doi.org/10.1038/s41524-021-00650-1) - Atomistic line graph neural network that explicitly passes messages over bond angles for crystal and molecular properties (Choudhary et al., 2021, npj Computational Materials). [[code](https://github.com/usnistgov/alignn)]
* [Graph neural networks in TensorFlow-Keras with RaggedTensor representation (kgcnn)](https://doi.org/10.1016/j.simpa.2021.100095) - Keras/TensorFlow library (kgcnn) implementing graph neural networks with ragged tensors for chemistry and materials (Reiser et al., 2021, Software Impacts). [[code](https://github.com/aimat-lab/gcnn_keras)]
* [Efficient and interpretable graph network representation for angle-dependent properties applied to optical spectroscopy](https://doi.org/10.1038/s41524-022-00841-4) - ALIGNN-d adds dihedral angles to line-graph representations for angle-dependent properties such as optical spectra (Hsu et al., 2022, npj Computational Materials).
* [Scalable deeper graph neural networks for high-performance materials property prediction](https://doi.org/10.1016/j.patter.2022.100491) - Deeper global-attention GNN with differentiable group normalization and skip connections enabling very deep materials GNNs (Omee et al., 2022, Patterns). [[code](https://github.com/usccolumbia/deeperGATGNN)]
* [CrysGNN: Distilling Pre-trained Knowledge to Enhance Property Prediction for Crystalline Materials](https://doi.org/10.1609/aaai.v37i6.25892) - Pre-trained crystal GNN (CrysGNN) distilling knowledge to improve downstream property predictors (Das et al., 2023, Proceedings of the AAAI Conference on Artificial Intelligence). [[code](https://github.com/kdmsit/crysgnn)]
* [Connectivity optimized nested line graph networks for crystal structures](https://doi.org/10.1039/d4dd00018h) - Connectivity-optimized (nested line) graph networks (coGN/coNGN) achieving state-of-the-art Matbench structure tasks (Ruff et al., 2024, Digital Discovery). [[code](https://github.com/aimat-lab/gcnn_keras)]

### Ionic conductivity: descriptor-guided transfer learning for ion mobility

* [Decoding the chemical space of fast-ion conductors via a descriptor-guided transfer learning framework](https://doi.org/10.1126/sciadv.aee4959) - IonNet, a multichannel network combining static and statistical descriptors that works with or without crystal structures, outperforms 16 ablation variants and earlier deep models at predicting ion mobility, identifying 87 fast-ion conductors among about 4,500 stable compounds and about 63,000 prospective ones among about 5 million substituted compounds (Wang et al., 2026, Science Advances).

### Ionic conductivity: descriptors from uMLIP energy landscapes

* [Predicting ionic conductivity in solids from the machine-learned potential energy landscape](https://doi.org/10.1103/PhysRevResearch.7.023167) - Heuristic descriptors read from a universal interatomic potential's energy landscape rank Materials Project Li compounds by expected conductivity; 8 of the top 10 are confirmed superionic at room temperature by first-principles calculations, about 50 times faster than uMLIP MD and at least 3,000 times faster than AIMD (Maevskiy et al., 2025, Physical Review Research).

### Ionic conductivity: GNN migration-barrier prediction (transfer learning)

* [Leveraging transfer learning for accurate estimation of ionic migration barriers in solids](https://doi.org/10.1038/s41524-026-01972-8) - A GNN pre-trained on seven bulk properties and fine-tuned on 619 literature DFT migration barriers distinguishes different pathways within a structure and generalizes across intercalants, including multivalent ions; it beats classical ML, GNNs trained from scratch and a uMLIP (test R2 = 0.703, MAE = 0.261 eV in the preprint) (Devi et al., 2026, npj Computational Materials).

### Ionic conductivity: lattice-dynamics descriptors for Na conductors

* [Machine-learning-assisted discovery of lattice dynamics signatures of sodium superionic conductors](https://doi.org/10.1039/d5mh01176k) - High-throughput phonon calculations on 3,903 Na-containing structures (921 Na superionic conductors) show a strong positive correlation between Na phonon mean-squared displacement and diffusion coefficient, and ML models built on phonon descriptors (MSD, Na VDOS centre, acoustic cutoff, low-frequency coupling) rapidly predict transport (Aghoghovbia et al., 2025, Materials Horizons).

### Ionic conductivity: ML-guided DFT-MD discovery of Li conductors

* [Machine Learning-Assisted Discovery of Solid Li-Ion Conducting Materials](https://doi.org/10.1021/acs.chemmater.8b03272) - Using the structure-based classifier to choose which of 12,000+ known compounds to simulate with DFT-MD makes the search 2.7 times more likely than random to find fast Li-ion conductors (F1 = 0.50, 3.5 times random), with at least a 44-fold higher log-average room-temperature conductivity, and the model doubles the F1 of six PhD-student experts (Sendek et al., 2018, Chemistry of Materials).

### Ionic conductivity: MLIP-MD (Deep Potential)

* [Deep potential generation scheme and simulation protocol for the Li10GeP2S12-type superionic conductors](https://doi.org/10.1063/5.0041849) - A DP-GEN active-learning protocol builds Deep Potentials for Li10GeP2S12, Li10SiP2S12 and Li10SnP2S12 that enable MD of about 1000-atom cells from 300 to 1000 K, with size, functional, thermal-expansion and disorder effects controlled so that computed diffusivities agree well with experiment (Huang et al., 2021, The Journal of Chemical Physics).

### Ionic conductivity: MLIP-MD (moment tensor potentials)

* [Bridging the gap between simulated and experimental ionic conductivities in lithium superionic conductors](https://doi.org/10.1016/j.mtphys.2021.100463) - Moment tensor potentials trained on optB88-vdW DFT give accurate lattice parameters and reproduce experimental conductivities and activation energies for Li0.33La0.56TiO3, Li3YCl6 and Li7P3S11, and long NPT MD reveals a low-temperature crossover between two Arrhenius regimes that ab initio MD cannot reach (Qi et al., 2021, Materials Today Physics).

### Ionic conductivity: MLIP-MD survey (on-the-fly sparse GP)

* [Universal Machine Learning Interatomic Potentials: Surveying Solid Electrolytes](https://doi.org/10.1021/acs.jpclett.1c01605) - Ab initio MD with on-the-fly sparse Gaussian-process potentials surveys Li diffusivity in hundreds of ternary crystals, and the expert models can be combined into transferable Li-P-S and Li-Sb-S potentials that also apply to quaternary systems such as Li-Ge-P-S (Hajibabaei et al., 2021, The Journal of Physical Chemistry Letters).

### Ionic conductivity: proton conductors via fine-tuned MLIP-MD screening

* [High-throughput screening and mechanistic insights into solid acid proton conductors](https://doi.org/10.1038/s43246-026-01338-z) - A two-stage screen of more than six million materials uses MLIPs fine-tuned to ab initio data to compute proton diffusion coefficients directly, identifying 27 high-performing solid-acid proton conductors (more than ten previously unexplored) and a universal O-O distance of about 2.5 Angstrom at proton transfer (Hänseroth et al., 2026, Communications Materials).

### Ionic conductivity: proton-conducting perovskite oxides (hydration descriptors)

* [Accelerated Discovery of Proton-Conducting Perovskite Oxide by Capturing Physicochemical Fundamentals of Hydration](https://doi.org/10.1021/acsenergylett.1c01239) - Gradient-boosting models trained on 65 thermogravimetric hydration datasets map 8,613 hypothetical perovskite oxides in physically engineered descriptor spaces and predict proton concentration versus temperature; the model nominated SrSnO3, and SrSn0.8Sc0.2O3-d was then shown experimentally to take up and conduct protons (Hyodo et al., 2021, ACS Energy Letters).

### Ionic conductivity: semi-supervised Li-conductor discovery

* [Identification of potential solid-state Li-ion conductors with semi-supervised learning](https://doi.org/10.1039/D2EE03499A) - A semi-supervised ML pipeline that combines scarce conductivity labels with many unlabelled Li-containing structures ranks new solid-electrolyte candidates; it is validated experimentally by synthesizing and measuring a new superionic conductor that the model predicted (Laskowski et al., 2023, Energy & Environmental Science).

### Ionic conductivity: structure-descriptor screening of Li conductors

* [Holistic computational structure screening of more than 12 000 candidates for solid lithium-ion conductor materials](https://doi.org/10.1039/C6EE02697D) - Screens more than 12,000 Li-containing Materials Project structures with stability, cost and electrochemical filters plus a logistic-regression conductivity classifier trained on experimental data using structure-only features, narrowing the space to a short list of promising solid-electrolyte candidates (Sendek et al., 2017, Energy & Environmental Science).

### Ionic conductivity: transfer learning for small-data Li-conductor screening

* [Screening billions of candidates for solid lithium-ion conductors: A transfer learning approach for small data](https://doi.org/10.1063/1.5093220) - Shows that generic descriptors fail on the small experimental Li-conductivity dataset unless guided by physics, and transfers the physics-informed structural model to composition descriptors through a large model-labelled database, making it possible to screen billions of hypothetical compositions (Cubuk et al., 2019, The Journal of Chemical Physics).

### Ionic conductivity: unsupervised discovery of Li conductors

* [Unsupervised discovery of solid-state lithium ion conductors](https://doi.org/10.1038/s41467-019-13214-1) - Uses unsupervised learning on Li-containing structures, guided by only a limited amount of conductivity data, to prioritize candidates for accurate screening, then confirms 16 new fast Li conductors with 1e-4 to 1e-1 S/cm predicted by ab initio MD (Zhang et al., 2019, Nature Communications).

### Magnetic properties: 2D magnets

* [High-throughput discovery of high Curie point two-dimensional ferromagnetic materials](https://doi.org/10.1038/s41524-020-0300-2) - Automated DFT plus Heisenberg Monte Carlo computes Curie temperatures for 786 2D materials (26 above 400 K) and trains an ML model that finds further high-Curie-point candidates (Kabiraj et al., 2020, npj Computational Materials).
* [Data-driven studies of magnetic two-dimensional materials](https://doi.org/10.1038/s41598-020-72811-z) - DFT plus ML predicts magnetic order, moments and formation energies of van der Waals monolayers derived from a known 2D magnet and identifies the X site as the driver of magnetic coupling (Rhone et al., 2020, Scientific Reports).
* [Data-Driven Studies of the Magnetic Anisotropy of Two-Dimensional Magnetic Materials](https://doi.org/10.1021/acs.jpclett.1c03783) - DFT plus ML study of magnetocrystalline anisotropy in A2B2X6 monolayers derived from Cr2Ge2Te6, identifying descriptors and the role of hybridization (Xie et al., 2021, The Journal of Physical Chemistry Letters).
* [On-the-fly interpretable machine learning for rapid discovery of two-dimensional ferromagnets with high Curie temperature](https://doi.org/10.1016/j.chempr.2021.11.009) - On-the-fly interpretable machine learning for rapid discovery of two-dimensional ferromagnets with high Curie temperature (Lu et al., 2022, Chem).

### Magnetic properties: benchmark of MLIPs on magnetic systems

* [Can MACE Potentials Accurately Describe Magnetism and Phase Stability in Fe-Ni Alloys? A Systematic Benchmark](https://arxiv.org/abs/2605.28395) - A system-specific MACE model trained on spin-polarised SQS data (2.0 meV/atom energy and 24.3 meV/A force validation errors) beats several MACE foundation models, including Hubbard-U variants, on Fe-Ni properties, but every model wrongly predicts that the bcc-to-hcp transition pressure rises with Ni content, showing that magnetic collapse and magnetoelastic effects are not captured (Ramakrishna et al., 2026, arXiv preprint).

### Magnetic properties: Curie temperature

* [Predicting the Curie temperature of ferromagnets using machine learning](https://doi.org/10.1103/PhysRevMaterials.3.104405) - Composition-only models trained on about 2,500 experimental ferromagnets predict TC to about 50 K accuracy and extrapolate along binary composition lines and across the Al-Co-Fe ternary (Nelson et al., 2019, Physical Review Materials).
* [Machine learning predictions of high-Curie-temperature materials](https://doi.org/10.1063/5.0156377) - Composition-only random forest and k-NN models trained on the two largest experimental TC datasets (over 2,500 and 3,000 entries) show systematic regression to the mean (over-predicting low-TC and under-predicting high-TC materials), and learning curves suggest that much more data or better descriptors are needed for exhaustive high-TC searches (Belot et al., 2023, Applied Physics Letters).

### Magnetic properties: dataset and ordering/Tc prediction

* [The northeast materials database for magnetic materials](https://doi.org/10.1038/s41467-025-64458-z) - LLM-extracted experimental database of 67,573 magnetic-materials entries; models trained on it reach 90% accuracy for FM/AFM/NM classification and predict Curie (Neel) temperatures with R2 0.87 (0.83) and MAE 56 K (38 K), flagging 25 FM and 13 AFM high-temperature candidates in the Materials Project (Itani et al., 2025, Nature Communications).

### Magnetic properties: hard-magnet screening

* [Machine learning-driven discovery of hard magnetic materials using high-throughput computation and screening](https://doi.org/10.1016/j.actamat.2025.121347) - ML, M3GNet relaxation of 48,000 candidates and DFT validation identify rare-earth-free FeCo-based hard magnets such as Fe6CoB2 (K1 = 1.76 MJ/m3, Ms above 1.3 T, Tc above 600 K) (Halder et al., 2025, Acta Materialia).
* [Broadening Hard-Magnet Discovery Beyond Symmetry Constraints via Unified Effective Anisotropy](https://doi.org/10.1002/advs.202524393) - A unified effective anisotropy constant defined for all seven crystal systems enables a magnetocrystalline-anisotropy database and a two-stage classification-regression screen of Materials Project without symmetry prefiltering, recovering known hard magnets and finding rare-earth-free orthorhombic and monoclinic candidates; a fine-tuned diffusion model proposes five DFT-confirmed candidates, including TaFe3 (Kim et al., 2026, Advanced Science).

### Magnetic properties: magnetic structure prediction

* [Universal Magnetic Structure Prediction from Atomic Coordinates with Near-Experimental Accuracy](https://arxiv.org/abs/2605.16230) - The magnetic structure network (MSN), an E(3)-equivariant GNN trained on experimental MAGNDATA structures, predicts collinear and noncollinear magnetic structures from crystal structure alone; a primitive modulated structure representation encodes commensurate and incommensurate orders in one framework, and the authors report high-fidelity reconstruction of experimental magnetic structures (Chotrattanapituk et al., 2026, arXiv preprint).

### Magnetic properties: magnetocaloric

* [Machine learning technique for prediction of magnetocaloric effect in La(Fe,Si/Al)13-based materials](https://doi.org/10.1088/1674-1056/27/6/067503) - Gradient-boosted trees relate composition of La(Fe,Si/Al)13 compounds to Curie temperature and maximum magnetic entropy change with R2 of 0.87-0.96 (Zhang et al., 2018, Chinese Physics B).
* [Machine learning predicted magnetic entropy change using chemical descriptors across a large compositional landscape](https://doi.org/10.1016/j.commatsci.2022.111414) - Dataset of experimental magnetic entropy changes across several magnetocaloric classes; a random forest (R2 0.82) screens about 40,000 compounds for room-temperature magnetocaloric candidates (Ucar et al., 2022, Computational Materials Science).

### Magnetic properties: magnetocaloric high-entropy alloys

* [DFT-based machine-learning for the rational design of magnetocaloric high-entropy alloys](https://doi.org/10.1038/s41467-026-77123-w) - Minimal-supercell DFT data and physics-informed ML map the design space of magnetocaloric MM'X high-entropy alloys, reducing computational time by 40-60% and identifying magnetic-moment dispersion as a key descriptor (Cui et al., 2026, Nature Communications).

### Magnetic properties: magnetocrystalline anisotropy and local moments

* [Accurate screening of functional materials with machine-learning potential and transfer-learned regressions: Heusler alloy benchmark](https://doi.org/10.1038/s41524-026-02013-0) - ML high-throughput workflow for quaternary and all-d Heuslers: a universal potential (eSEN-30M-OAM) handles stability, while eSEN models fine-tuned by frozen transfer learning on the DxMag database predict local moments, magnetic stability and magnetocrystalline anisotropy energy; DFT confirms the candidates, and the paper benchmarks uMLIPs and how faithfully they predict local moments (Xiao et al., 2026, npj Computational Materials).

### Magnetic properties: moment screening

* [Prediction of large magnetic moment materials with graph neural networks and random forests](https://doi.org/10.1103/physrevmaterials.7.044407) - CGCNN, MEGNet and random forests trained on Materials Project screen the ICSD for ferromagnets with large moments; magnetic properties prove intrinsically harder to predict than other DFT properties, and 15 untested large-moment candidates are proposed (Kaba et al., 2023, Physical Review Materials).

### Magnetic properties: ordering classification

* [Machine learning magnetism classifiers from atomic coordinates](https://doi.org/10.1016/j.isci.2022.105192) - A Euclidean-equivariant neural network that takes only atomic coordinates classifies magnetic order (FM/AFM/NM) with 77.8% mean accuracy and the propagation vector (zero or nonzero) with 73.6%, reaching 91% for predicting no order in structures that contain magnetic elements (Merker et al., 2022, iScience).
* [Learning magnetic order classification from large-scale materials databases](https://doi.org/10.1103/qftr-2tfm) - Classifiers trained on experimental MAGNDATA labels with simple Materials Project descriptors exceed 92% accuracy for zero versus nonzero propagation vectors and expose a systematic ferromagnetic bias in Materials Project labels for more than 6,840 materials; LightGBM and XGBoost trained on MP labels reach only 82-85% accuracy (macro-F1 63-66%) (Fahmy et al., 2026, Physical Review Materials).

### Magnetic properties: ordering classification and Curie temperature

* [An accelerating approach of designing ferromagnetic materials via machine learning modeling of magnetic ground state and Curie temperature](https://doi.org/10.1080/21663831.2020.1863876) - Random forests on composition and structure descriptors for about 2,800 intermetallics classify FM versus AFM ground states at about 87% accuracy and regress TC at about 91% accuracy (MAE about 58 K in the preprint), with comparable accuracy when applied to Materials Project magnetic intermetallics (Long et al., 2021, Materials Research Letters).

### Magnetic properties: review

* [Machine Learning in Magnetic Materials](https://doi.org/10.1002/pssb.202000600) - Review of ML applied to DFT data to link structure and composition to magnetisation; its Materials Project analysis finds that same-composition materials can differ in magnetisation by space group, and a neural network predicts magnetisation with a standard error of 8.3e-3 muB/A^3 (Katsikas et al., 2021, physica status solidi (b)).

### Magnetic properties: spin-aware MLIP

* [High-dimensional neural network potentials for magnetic systems using spin-dependent atom-centered symmetry functions](https://doi.org/10.1038/s41524-021-00636-z) - Spin-dependent atom-centred symmetry functions let a high-dimensional neural network potential distinguish collinear magnetic states of MnO, reproducing its magnetically distorted rhombohedral structure and giving the Neel temperature with structural fluctuations, entropy and defects included (Eckhoff et al., 2021, npj Computational Materials).
* [Magnetic Moment Tensor Potentials for collinear spin-polarized materials reproduce different magnetic states of bcc Fe](https://doi.org/10.1038/s41524-022-00696-9) - Magnetic moment tensor potentials (mMTPs) add collinear magnetic moments as degrees of freedom and use a two-step coarse-grained minimisation over atomic and spin space to reproduce the vibrational and magnetic behaviour of different magnetic states of bcc Fe, including phonons and MD with fluctuating moments (Novikov et al., 2022, npj Computational Materials).
* [Non-collinear magnetic atomic cluster expansion for iron](https://doi.org/10.1038/s41524-024-01196-8) - A noncollinear magnetic atomic cluster expansion for Fe, trained on collinear and noncollinear spin-DFT data, reproduces ground-state properties of several magnetic phases as well as the magnetic and lattice excitations needed for finite-temperature behaviour and crystal defects (Rinaldi et al., 2024, npj Computational Materials).
* [Spin-dependent graph neural network potential for magnetic materials](https://doi.org/10.1103/PhysRevB.109.144426) - SpinGNN combines Heisenberg-edge and spin-distance-edge GNNs to fit high-order spin-lattice Hamiltonians and runs spin-lattice dynamics of BiFeO3 with over a million atoms, reproducing its AFM ground state, magnetic transition and domain-wall energetics (follow-up SpinGNN++, PRB 110, 104427, adds time-reversal equivariance and noncollinear spins with SOC) (Yu et al., 2024, Physical Review B).

### Material classes: glasses

* [GlassNet: A multitask deep neural network for predicting many glass properties](https://doi.org/10.1016/j.ceramint.2023.08.281) - GlassNet, a multitask deep neural network trained on more than 218k glass compositions, predicts 85 properties of oxide, chalcogenide, halide and other glasses and, combined with the MYEGA equation, outperforms ViscNet on unseen viscosity data (Cassar et al., 2023, Ceramics International).

### Material classes: polymers

* [polyBERT: a chemical language model to enable fully machine-driven ultrafast polymer informatics](https://doi.org/10.1038/s41467-023-39868-6) - polyBERT treats polymer SMILES as a chemical language to produce fingerprints that, with multitask learning, predict many polymer properties about two orders of magnitude faster than handcrafted-fingerprint approaches at similar accuracy (Kuenneth et al., 2023, Nature Communications).

### Multimodal: 3D charge density + composition (Magpie)

* [Physics-Aware Representation Learning on Electronic Charge Density for Materials Property Prediction](https://doi.org/10.1021/acs.jcim.6c00235) - A 3D convolutional autoencoder compresses DFT charge densities into latent features that, combined with Magpie composition descriptors, predict bulk, Young's and shear moduli, formation energy and Debye temperature for about 6,059 compounds (R2 = 0.94, 0.88, 0.87, 0.96 and 0.89), with composition fusion improving accuracy over charge density alone (Kumar et al., 2026, Journal of Chemical Information and Modeling).

### Multimodal: 3D structure graph + text (multimodal LLM)

* [CatalyticMLLM: A Graph-Text Multimodal Large Language Model for Catalytic Materials](https://arxiv.org/abs/2605.17254) - CatalyticMLLM unifies property prediction and CIF generation for catalytic materials in one graph-text multimodal LLM and outperforms decoupled predictor/generator baselines on catalytic relaxed-energy prediction and inverse design (Li et al., 2026, arXiv).

### Multimodal: charge-density images + crystallographic text (CLIP and stacked transfer learning)

* [Transfer Learning in Materials Informatics: structure-property relationships through minimal but highly informative multimodal input](https://arxiv.org/abs/2401.09301) - Pretrained CNNs and language models are transferred to electronic charge-density profile images and crystallographic text, and CLIP and a stacked multi-modality model regress energetic and structural properties across many compositions without GNNs, probing what semantic crystallographic text adds to charge-density images (Massa et al., 2024, arXiv).

### Multimodal: composition + structure (cross-modal knowledge transfer)

* [Enhancing composition-based materials property prediction by cross-modal knowledge transfer](https://doi.org/10.1038/s41598-026-53182-3) - Transferring structural knowledge to composition-only models, either implicitly by pretraining chemical language models on multimodal embeddings or explicitly by generating structures for structure-aware predictors, gave state-of-the-art results in 25 of 32 LLM4Mat-Bench and MatBench tasks (Rubtsov et al., 2026, Scientific Reports).

### Multimodal: crystal graph + element-attribute knowledge graph

* [Material Property Prediction with Element Attribute Knowledge Graphs and Multimodal Representation Learning](https://arxiv.org/abs/2411.08414) - ESNet fuses crystal-structure features with knowledge-graph embeddings of element attributes (radius, electronegativity, ionization energy) and gives leading band-gap accuracy on the Materials Project benchmark while matching existing models on formation energy (Huang et al., 2024, arXiv).

### Multimodal: crystal graph + LLM text (late fusion)

* [Crystal Structure Based Graph Neural Network And LLM Multi-Modal Approach for Material Magnetic Ordering Prediction](https://arxiv.org/abs/2610.25775) - Fusing a crystal-structure GNN with an LLM reading text descriptions classifies magnetic ordering (non-magnetic, FM, AFM, FiM) on Materials Project, MAGNDATA and uranium compounds more accurately than either standalone model under all three fusion strategies tested (Zheng et al., 2026, arXiv).

### Multimodal: crystal graph + text description (semantic-gated message passing)

* [SAGE-Net: Semantics-Augmented Geometric Encoder for Material Property Prediction](https://arxiv.org/abs/2607.22271) - SAGE-Net injects semantics from structure-derived crystallographic text descriptions directly into GNN message passing via semantic-guided gating, giving the lowest MAE on 8 of 10 JARVIS-DFT regression targets across several GNN backbones and strong synthesizability classification (Zhang et al., 2026, arXiv).

### Multimodal: literature text + numerical conditions + reaction pathways

* [A multimodal semantic learning framework for data-driven discovery of nitrate-to-ammonia electrocatalysts](https://doi.org/10.1038/s41524-026-02327-z) - MatSemNet integrates text, numerical and reaction-pathway information mined from the literature to predict nitrate-reduction Faradaic efficiency better than single-modal or descriptor models, and guided rare-earth-doped Co3O4 catalysts that reached 85.5% FE and 28.3 mg h-1 cm-2 ammonia yield experimentally (Liu et al., 2026, npj Computational Materials).

### Multimodal: structure encoders + LLM (task-conditioned attention fusion)

* [Choosing the Right Representations: Task-Aware Fusion for Multimodal Materials Language Models](https://arxiv.org/abs/2611.24641) - A lightweight task-conditioned attention bridge that combines CHGNet features with intermediate Zatom-1 (and optionally UMA-S) representations for a materials LLM outperforms MatterChat with up to 47.8% lower RMSE using fewer trainable parameters and half the training time, reaching 89.61% macro-average classification accuracy with three encoders (Ta et al., 2026, NeurIPS 2026 AI4Mat Workshop).

### Multimodal: surface graph + adsorbate features (cross-attention)

* [A multi-modal transformer for predicting global minimum adsorption energy](https://doi.org/10.1038/s41467-025-58499-7) - AdsMT uses cross-attention between catalyst-surface graphs and adsorbate feature vectors to predict the global minimum adsorption energy without enumerating binding sites, reaching MAEs of 0.09, 0.14 and 0.39 eV on three new benchmark datasets (Chen et al., 2025, Nature Communications). [[code](https://github.com/schwallergroup/AdsMT)]

### Multimodal: XANES + pair distribution function (feature-level fusion, random forest)

* [Interpretable multimodal machine learning analysis of X-ray absorption near-edge spectra and pair distribution functions](https://doi.org/10.1038/s41524-025-01589-3) - Random forests trained on simulated XANES, PDFs and both together for transition-metal oxides show that XANES-only models usually beat PDF-only models even for structural targets (oxidation state, coordination number, bond length), and that XANES dominates when the two are combined, a direct analysis of when a second modality helps (Na Narong et al., 2025, npj Computational Materials).

### Multimodal: XAS + EELS, multiple elements and edges

* [Revealing Local Structures through Machine-Learning-Fused Multimodal Spectroscopy](https://doi.org/10.1021/acsnano.5c16942) - ML models trained on fused multi-element, multi-edge XAS and EELS spectra of NMC cathode oxides infer local element content in quantitative agreement with experiment and detect oxygen vacancies and antisite defects, which single-mode spectra cannot (Jia et al., 2026, ACS Nano).

### Multimodal: XRD + composition (constraint-reasoning phase mapping)

* [Automating crystal-structure phase mapping by combining deep learning with constraint reasoning](https://doi.org/10.1038/s42256-021-00384-1) - Deep reasoning networks demix XRD patterns over a composition library using thermodynamic constraints and identified 13 phases from 307 patterns in the previously unsolved Bi-Cu-V oxide system, outperforming earlier phase-mapping algorithms (Chen et al., 2021, Nature Machine Intelligence).

### Non-scalar targets

* [Symmetry-Adapted Machine Learning for Tensorial Properties of Atomistic Systems](https://doi.org/10.1103/PhysRevLett.120.036002) - Symmetry-adapted Gaussian process regression (SA-GPR) for tensorial properties of atomistic systems (Grisafi et al., 2018, Physical Review Letters).
* [Unifying machine learning and quantum chemistry with a deep neural network for molecular wavefunctions](https://doi.org/10.1038/s41467-019-12875-2) - SchNOrb deep network predicting molecular wavefunctions in local atomic orbital bases (Schütt et al., 2019, Nature Communications). [[code](https://github.com/atomistic-machine-learning/SchNOrb)]
* [Direct Prediction of Phonon Density of States With Euclidean Neural Networks](https://doi.org/10.1002/advs.202004214) - Euclidean neural networks (e3nn) directly predicting phonon density of states of crystals (Chen et al., 2021, Advanced Science). [[code](https://github.com/zhantaochen/phonondos_e3nn)]
* [SE(3)-equivariant prediction of molecular wavefunctions and electronic densities](https://arxiv.org/abs/2106.02347) - SE(3)-equivariant network (PhiSNet) predicting wavefunctions and electronic densities (Unke et al., 2021, NeurIPS 2021).
* [Density of states prediction for materials discovery via contrastive learning from probabilistic embeddings](https://doi.org/10.1038/s41467-022-28543-x) - Mat2Spec predicts phonon and electronic DOS via contrastive learning with probabilistic embeddings (Kong et al., 2022, Nature Communications). [[code](https://github.com/gomes-lab/Mat2Spec)]
* [Deep-learning density functional theory Hamiltonian for efficient ab initio electronic-structure calculation](https://doi.org/10.1038/s43588-022-00265-6) - DeepH learns the DFT Hamiltonian in localized bases with message-passing networks for electronic structure (Li et al., 2022, Nature Computational Science). [[code](https://github.com/mzjb/DeepH-pack)]
* [General framework for E(3)-equivariant neural network representation of density functional theory Hamiltonian](https://doi.org/10.1038/s41467-023-38468-8) - E(3)-equivariant network (DeepH-E3) representing DFT Hamiltonians including spin-orbit coupling (Gong et al., 2023, Nature Communications). [[code](https://github.com/Xiaoxun-Gong/DeepH-E3)]
* [An equivariant graph neural network for the elasticity tensors of all seven crystal systems](https://doi.org/10.1039/D3DD00233K) - MatTen equivariant GNN predicting full elasticity tensors for all seven crystal systems (Wen et al., 2023, arXiv). [[code](https://github.com/wengroup/matten)]
* [Transferable equivariant graph neural networks for the Hamiltonians of molecules and solids](https://doi.org/10.1038/s41524-023-01130-4) - Transferable E(3)-equivariant GNN (HamGNN) predicting tight-binding Hamiltonians of molecules and solids (Zhong et al., 2023, npj Computational Materials). [[code](https://github.com/QuantumLab-ZY/HamGNN)]
* [Virtual node graph neural network for full phonon prediction](https://doi.org/10.1038/s43588-024-00661-0) - Virtual-node GNN predicting full phonon band structures, including Gamma-point and full dispersions (Okabe et al., 2024, Nature Computational Science). [[code](https://github.com/RyotaroOkabe/phonon_prediction)]
* [DeepH-2: Enhancing deep-learning electronic structure via an equivariant local-coordinate transformer](https://arxiv.org/abs/2401.17015) - DeepH-2 equivariant local-coordinate transformer for deep-learning electronic structure (Wang et al., 2024, arXiv). [[code](https://github.com/mzjb/DeepH-pack)]
* [Universal materials model of deep-learning density functional theory Hamiltonian](https://doi.org/10.1016/j.scib.2024.06.011) - Universal DeepH model of DFT Hamiltonians trained across many elements and materials (Wang et al., 2024, arXiv). [[code](https://github.com/mzjb/DeepH-pack)]
* [A Space Group Symmetry Informed Network for O(3) Equivariant Crystal Tensor Prediction](https://arxiv.org/abs/2406.12888) - Space-group symmetry-informed O(3)-equivariant network (GMTNet) for crystal tensor properties such as dielectric and piezoelectric tensors (Yan et al., 2024, ICML 2024). [[code](https://github.com/divelab/AIRS)]
* [Accurate piezoelectric tensor prediction with equivariant attention tensor graph neural network](https://doi.org/10.1038/s41524-025-01546-0) - Equivariant attention tensor GNN for accurate piezoelectric tensor prediction (Dong et al., 2025, npj Computational Materials).
* [Revisiting the Canonicalization for Fast and Accurate Crystal Tensor Property Prediction](https://doi.org/10.1609/aaai.v40i1.37004) - GoeCTP canonicalization approach enabling fast, accurate crystal tensor property prediction (Hua et al., 2026, Proceedings of the AAAI Conference on Artificial Intelligence). [[code](https://github.com/divelab/AIRS)]

### Non-scalar targets: charge density

* [Global Plane Waves From Local Gaussians: Periodic Charge Densities in a Blink](https://arxiv.org/abs/2601.19966) - Introduces ELECTRAFI, which builds anisotropic real-space Gaussians and evaluates plane-wave coefficients analytically to reconstruct periodic charge densities with one inverse FFT (Elsborg et al., 2026, ICML 2026).

### Non-scalar targets: density of states

* [Density of States Prediction of Crystalline Materials via Prompt-guided Multi-Modal Transformer](https://doi.org/10.52202/075280-2694) - Predicts crystal DOS with a prompt-guided multimodal transformer that integrates crystal representations with energy-level information (Lee et al., 2023, Advances in Neural Information Processing Systems 36).
* [Deep Scientific Reasoning under Physical Constraints: Structure-Aware Spectrum Prediction](https://arxiv.org/abs/2610.34021) - Introduces DeepSciReasoner, which predicts electronic DOS with structure-aware spectrum decoding and constraint-preserving physical reasoning (Wang et al., 2026, ICML 2026).

### Non-scalar targets: electron density

* [Equivariant Neural Operator Learning with Graphon Convolution](https://doi.org/10.52202/075280-2709) - Proposes InfGCN, an SE(3)-equivariant neural operator interpretable as graphon convolution, for predicting electron densities, outperforming prior architectures on large-scale electron-density datasets (Cheng et al., 2023, Advances in Neural Information Processing Systems 36).

### Optoelectronic: band gap beyond PBE (hybrid/GW-validated)

* [High-Quality Data Enabling Universality of Band Gap Descriptor and Discovery of Photovoltaic Perovskites](https://doi.org/10.1021/jacs.4c03507) - A machine-learned band-gap descriptor trained on a consistently computed high-accuracy band-gap dataset (doubly screened hybrid functional gaps validated against experiment and state-of-the-art GW) transfers across single and double, halide and oxide, and hybrid organic-inorganic perovskites; screening up to 15,659 materials found 14 unreported lead-free photovoltaic perovskites, with MASnBr3, FA2SnGeBr6, FA2InBiBr6 and Ba2InBiO6 among those standing out for direct gaps, small effective masses, low exciton binding energies and high stability (Wang et al., 2024, Journal of the American Chemical Society).

### Optoelectronic: band gap of 2D MXenes (descriptor-based)

* [Machine-Learning-Assisted Accurate Band Gap Predictions of Functionalized MXene](https://doi.org/10.1021/acs.chemmater.8b00686) - Kernel ridge, support vector, Gaussian process and bagging regressors using simple elemental and structural features (boiling and melting points, atomic radii, phases, bond lengths), without the PBE gap as input, predict band gaps of functionalized MXenes, with the Gaussian process model reaching the lowest RMSE of 0.14 eV (Rajan et al., 2018, Chemistry of Materials).

### Optoelectronic: band gap, absorption and PV figure of merit (composition-based)

* [Data-driven design of novel halide perovskite alloys](https://doi.org/10.1039/d1ee02971a) - Composition-based neural networks trained on 229 PBE and HSE06 calculations of B-site-mixed ABX3 halide perovskites predict stability, band gap, vacancy formation energy, refractive index and absorption for 17,955 alloys, screening 574 promising photovoltaic absorbers; note that descriptors are site-averaged elemental properties of pseudo-cubic structures (Mannodi-Kanakkithodi et al., 2022, Energy & Environmental Science).

### Optoelectronic: band gaps and band-edge positions beyond PBE

* [Predicting band gaps and band-edge positions of oxide perovskites using density functional theory and machine learning](https://doi.org/10.1103/physrevb.106.155156) - ML models trained on HSE06 targets correct GGA band gaps and band-edge positions of ABO3 oxide perovskites, revealing a systematic correction of about 1.5 eV (about 1 eV from lowering the valence band and 0.5 eV from raising the conduction band) and identifying the chemical and structural features that control it (Li et al., 2022, Physical Review B).

### Optoelectronic: band-gap-driven photovoltaic screening (hybrid perovskites)

* [Accelerated discovery of stable lead-free hybrid organic-inorganic perovskites via machine learning](https://doi.org/10.1038/s41467-018-05761-w) - A target-driven ML band-gap model combined with DFT screened 5158 unexplored hybrid organic-inorganic perovskites to six orthorhombic lead-free candidates with suitable band gaps and room-temperature thermal stability, two of which have direct visible-range gaps and good environmental stability (Lu et al., 2018, Nature Communications).

### Optoelectronic: defect energies and electronic properties in 2D materials

* [Sparse representation for machine learning the properties of defects in 2D materials](https://doi.org/10.1038/s41524-023-01062-z) - A sparse representation of defect configurations in 2D lattices lets a neural network learn properties of defective 2D materials with at least a 3.7-fold drop in energy-prediction error versus state-of-the-art approaches while being about an order of magnitude more resource-efficient for training and inference (Kazeev et al., 2023, npj Computational Materials).

### Optoelectronic: defect formation energies

* [Accelerating defect predictions in semiconductors using graph neural networks](https://doi.org/10.1063/5.0176333) - CGCNN, MEGNet and ALIGNN models trained on one of the largest DFT defect datasets (native defects, impurities and complexes in group IV, III-V and II-VI zinc blende semiconductors, augmented with partially optimized configurations) predict charge- and chemical-potential-dependent defect formation energies, with ALIGNN best at an RMSE of about 0.3 eV (Rahman et al., 2024, APL Machine Learning).
* [Leveraging Persistent Homology Features for Accurate Defect Formation Energy Predictions via Graph Neural Networks](https://doi.org/10.1021/acs.chemmater.4c03028) - Adding persistent-homology features of local atomic environments, with suitable graph pooling, to GNNs (including graph transformer and equivariant networks) cuts the MAE of vacancy formation energies in oxide perovskites by 55%, removes the supercell-size convergence issue and captures defect-defect interactions in multiply substituted BaTiO3 (Fang et al., 2025, Chemistry of Materials).

### Optoelectronic: defect formation energies and charge-transition levels

* [Universal machine learning framework for defect predictions in zinc blende semiconductors](https://doi.org/10.1016/j.patter.2022.100450) - Across a chemical space of about 12,000 impurity configurations in 34 group IV, III-V and II-VI zinc blende semiconductors (10% computed with DFT), regression models using elemental, coordination-environment and host descriptors predict neutral formation energies and charge-transition levels and are used to screen impurities with lower formation energy than the dominant native defects (Mannodi-Kanakkithodi et al., 2022, Patterns).

### Optoelectronic: defect ground-state structures

* [Machine-learning structural reconstructions for accelerated point defect calculations](https://doi.org/10.1038/s41524-024-01303-9) - A surrogate model that learns defect reconstruction motifs in metal chalcogenide and mixed-anion crystals predicts favourable reconstructions for unseen defects in unseen compositions in 90% of cases, cutting first-principles calculations by 73%, and is applied to vacancies across CdSexTe1-x alloys (Mosquera-Lois et al., 2024, npj Computational Materials).

### Optoelectronic: GW quasiparticle corrections (2D)

* [Representing individual electronic states for machine learning GW band structures of 2D materials](https://doi.org/10.1038/s41467-022-28122-0) - State-specific fingerprints (ENDOME operator matrix elements and radially decomposed PDOS) from standard DFT train a gradient-boosting model on 46k G0W0 quasiparticle energies of 2D materials that predicts self-energy corrections for unseen materials with 0.14 eV MAE, reduced by a further 30% when the dielectric constant is added (Knøsgaard et al., 2022, Nature Communications).

### Optoelectronic: HSE band gap and band edges (2D, C2DB)

* [Combined Machine Learning and High-Throughput Calculations Predict Heyd-Scuseria-Ernzerhof Band Gap of 2D Materials and Potential MoSi2N4 Heterostructures](https://doi.org/10.1021/acs.jpclett.4c01013) - ML trained on C2DB data predicts HSE band gaps, CBM and VBM for 2176 2D materials, yielding a 3539-material HSE band-edge set used to classify 766 lattice-matched MoSi2N4/2D heterostructures by band alignment (230 type I, 244 type II, 284 type III) (Zhang et al., 2024, The Journal of Physical Chemistry Letters).

### Optoelectronic: hybrid-functional band gap from PBE density

* [Predicting HSE band gaps from PBE charge densities via neural network functionals](https://doi.org/10.1088/1361-648x/ab5f3a) - A single neural-network functional of the PBE charge density predicts HSE band gaps of seven materials (Si, GaAs, MoS2, Ge and Sn, Ti and Zr phosphates) under varied conditions with 172.6 meV RMSE, 34% better than linear PBE-to-HSE regression (Lentz et al., 2020, Journal of Physics: Condensed Matter).

### Optoelectronic: impurity charge-transition levels

* [Machine learning for impurity charge-state transition levels in semiconductors from elemental properties using multi-fidelity datasets](https://doi.org/10.1063/5.0083877) - Trained on LDA/GGA transition levels corrected by a modified band-alignment scheme (no high-fidelity values needed for training), an elemental-property model predicts impurity charge-state transition levels with 0.36 eV RMSE (0.27 eV MAE) against HSE06 values over 14 semiconductor systems, outperforming models trained only on the smaller high-fidelity set (Polak et al., 2022, The Journal of Chemical Physics).

### Optoelectronic: impurity formation enthalpies and charge-transition levels

* [Machine-learned impurity level prediction for semiconductors: the example of Cd-based chalcogenides](https://doi.org/10.1038/s41524-020-0296-7) - Regression models trained on a DFT dataset of impurities in CdTe, CdSe and CdS predict impurity formation enthalpies and charge-transition levels, transfer from the end-member compounds to mixed-anion CdX alloys, and are used to predict Fermi-level-dependent formation energies of hundreds of impurities in five chalcogenides and flag impurities that can shift the equilibrium Fermi level, agreeing well with DFT for the dominant impurities (Mannodi-Kanakkithodi et al., 2020, npj Computational Materials).

### Optoelectronic: multi-fidelity band gap and PV efficiency (composition-based)

* [Discovering novel halide perovskite alloys using multi-fidelity machine learning and genetic algorithm](https://doi.org/10.1063/5.0182543) - Multi-fidelity random forests trained on about 800 PBE and HSE06 halide perovskite alloys plus about 100 experimental points (composition, phase and fidelity descriptors) predict experiment-level decomposition energy, band gap and PV efficiency for more than 150,000 hypothetical compounds, finding thousands with 1-2 eV gaps and >15% efficiency, and a genetic algorithm finds hundreds more (Yang et al., 2024, The Journal of Chemical Physics).

### Optoelectronic: point-defect properties in 2D materials

* [Machine Learning-Enabled Design of Point Defects in 2D Materials for Quantum and Neuromorphic Information Processing](https://doi.org/10.1021/acsnano.0c05267) - Deep transfer learning and physics-informed defect featurization combined with first-principles calculations rapidly predict key point-defect properties in 2D materials and identify over one hundred unexplored dopant defects in layered metal chalcogenides, hexagonal nitrides and metal halides as candidates for quantum emission, resistive switching and neuromorphic computing (Frey et al., 2020, ACS Nano).

### Optoelectronic: quasiparticle band gap (double perovskites)

* [Efficient and Accurate Prediction of Double Perovskite Quasiparticle Band Gaps via Machine Learning and a Descriptor](https://doi.org/10.1021/acs.jpclett.5c00173) - A multistep ML framework with an interpretable descriptor predicts quasiparticle band gaps of double perovskites with over 90% accuracy and screens 4,507 candidates to 94 lead-free structures with suitable gaps, six of which are verified as stable photocatalyst candidates (Niu et al., 2025, The Journal of Physical Chemistry Letters).

### Optoelectronic: spectroscopic limited maximum efficiency (SLME)

* [Accelerated Discovery of Efficient Solar Cell Materials Using Quantum and Machine-Learning Methods](https://doi.org/10.1021/acs.chemmater.9b02166) - TBmBJ SLME calculations for 5097 non-metallic JARVIS-DFT materials identified 1997 candidates above 10% SLME (934 also stable with suitable effective masses), and an ML classifier trained on these data pre-screened over a million materials for efficient solar absorbers (Choudhary et al., 2019, Chemistry of Materials). [[code](https://github.com/usnistgov/jarvis)]

### Optoelectronic: surface work function

* [Discovery of Stable Surfaces with Extreme Work Functions by High-Throughput Density Functional Theory and Machine Learning](https://doi.org/10.1002/adfm.202401764) - A DFT database of 58,332 work functions for 33,631 slabs from 3,716 bulk materials trains a random-forest model on physics-based surface features with 0.09 eV test MAE (about 10^5 times faster than DFT), identifying record-low (1.25 eV, BaMoO3 (100)-Ba-O) and record-high (9.06 eV, Ag2F (001)-F) work-function surfaces (Schindler et al., 2024, Advanced Functional Materials).

### Optoelectronic: vacancy defect formation enthalpies

* [Defect graph neural networks for materials discovery in high-temperature clean-energy applications](https://doi.org/10.1038/s43588-023-00495-2) - A defect graph neural network (dGNN) trained on DFT oxygen-vacancy data predicts site-resolved vacancy formation enthalpies directly from the ideal host crystal, replacing a defect-supercell relaxation per unique site, and, combined with reduction-entropy thermodynamics, screens Materials Project oxides for solar thermochemical hydrogen production (Witman et al., 2023, Nature Computational Science).

### Physics-informed: architecture

* [High accuracy and transferability of a neural network potential through charge equilibration for calcium fluoride](https://doi.org/10.1103/PhysRevB.95.104105) - The charge equilibration via neural network technique (CENT) for CaF2, trained only on non-periodic clusters, reproduces PBE energetics of bulk crystalline phases at ambient and high pressure, surfaces, and phonons with deviations no larger than the LDA-vs-PBE difference (Faraji et al., 2017, Physical Review B).
* [Incorporating long-range physics in atomic-scale machine learning](https://doi.org/10.1063/1.5128375) - Introduces nonlocal, O(3)-equivariant long-distance representations with the asymptotics of the electrostatic potential (LODE), capturing long-range electrostatic energies of point charges, charged dimer binding curves and the dielectric response of water, outperforming local ML schemes (Grisafi et al., 2019, The Journal of Chemical Physics).
* [OrbNet: Deep learning for quantum chemistry using symmetry-adapted atomic-orbital features](https://doi.org/10.1063/5.0021955) - OrbNet, a GNN on symmetry-adapted atomic-orbital features from semi-empirical electronic-structure calculations, predicts DFT energies of drug-like molecules within chemical accuracy at >=1000-fold lower cost (molecular, not crystalline) (Qiao et al., 2020, The Journal of Chemical Physics).
* [A fourth-generation high-dimensional neural network potential with accurate electrostatics including non-local charge transfer](https://doi.org/10.1038/s41467-020-20427-2) - Introduces a fourth-generation HDNNP that combines a charge-equilibration scheme with environment-dependent atomic electronegativities and atomic energies, correctly describing global charge distributions and long-range charge transfer that local MLPs describe incorrectly (Ko et al., 2021, Nature Communications).
* [A deep potential model with long-range electrostatic interactions](https://doi.org/10.1063/5.0083669) - DPLR adds the electrostatics of Gaussian charges at ionic sites and NN-predicted Wannier centroids to the short-range Deep Potential, recovering Coulombic-tail effects missing from the standard DP model (Zhang et al., 2022, The Journal of Chemical Physics).
* [Ewald-based Long-Range Message Passing for Molecular Graphs](https://arxiv.org/abs/2303.04791) - Ewald message passing, a Fourier-space nonlocal augmentation grounded in Ewald summation, improves energy MAEs of four baseline MPNNs by on average 10% on OC20 (periodic) and 16% on OE62, with outsized gains on structures with large long-range energy contributions (Kosmala et al., 2023, Proceedings of the 40th International Conference on Machine Learning (ICML 2023)).
* [Incorporating long-range electrostatics in neural network potentials via variational charge equilibration from shortsighted ingredients](https://doi.org/10.1038/s41524-024-01225-6) - A variational charge-equilibration MLIP that can be trained with or without charge targets; on solid and liquid NaCl it beats a local-descriptor model in energy/force accuracy and captures the DFT long-range tail of the isolated Na-Cl dimer (Shaidu et al., 2024, npj Computational Materials).
* [Latent Ewald summation for machine learning of long-range interactions](https://doi.org/10.1038/s41524-025-01577-7) - Proposes Latent Ewald Summation (LES), which learns a hidden variable from local descriptors and applies an Ewald sum to it, eliminating unphysical predictions of short-range MLIPs (even with message passing) for charged/polar dimers, bulk water and water-vapor interfaces at about twice the cost (Cheng et al., 2025, npj Computational Materials).
* [Machine learning of charges and long-range interactions from energies and forces](https://doi.org/10.1038/s41467-025-63852-x) - Benchmarks LES across charged molecules, ionic liquids, electrolytes, surface adsorption and electrolyte/solid and solid-solid interfaces, showing it recovers exact atomic charges for fixed-charge systems, infers dipoles/quadrupoles and Born-type dipole derivatives, and gives better energy/force accuracy than models trained on explicit charges (King et al., 2025, Nature Communications).

### Physics-informed: evidence

* [Interpretable models for extrapolation in scientific machine learning](https://doi.org/10.1039/D3DD00082F) - Across extrapolation tasks on scientific datasets, simple interpretable linear models perform on average equivalently to black-box machine-learning models (based on the published abstract summary) (Muckley et al., 2023, Digital Discovery).

### Physics-informed: Hessian/phonon supervision

* [PFT: Phonon Fine-tuning for Machine Learned Interatomic Potentials](https://arxiv.org/abs/2601.07742) - Introduces phonon fine-tuning, which supervises MLIP energy Hessians against DFT force constants via stochastic Hessian-vector products to improve vibrational and thermal property prediction (Koker et al., 2026, ICML 2026).

### Physics-informed: hybrid

* [Physically informed artificial neural networks for atomistic modeling of materials](https://doi.org/10.1038/s41467-019-10343-5) - The physically informed neural network (PINN) potential combines an analytical bond-order potential with NN regression of its parameters, demonstrated with a general-purpose potential for Al (Pun et al., 2019, Nature Communications).
* [Calibrating DFT Formation Enthalpy Calculations by Multifidelity Machine Learning](https://doi.org/10.1021/jacsau.2c00235) - A multifidelity random forest using DFT values as low-fidelity input learns experimental formation enthalpies more accurately than PBE (with linear correction), PBEsol, SCAN and r2SCAN, and outperforms deep representation learning and transfer learning; it is used to recalibrate Materials Project enthalpies (Gong et al., 2022, JACS Au).
* [Machine learned environment-dependent corrections for a spds* empirical tight-binding basis](https://doi.org/10.1088/2632-2153/ad4510) - MLDeltaTB is a Delta-learning scheme that predicts environment-dependent corrections to on-site empirical tight-binding parameters from ab initio band structures, reproducing experimental and ab initio electronic properties of random GaAsSb alloys (Soccodato et al., 2024, Machine Learning: Science and Technology).
* [Learning Pairwise Interaction for Extrapolative and Interpretable Machine Learning Interatomic Potentials with Physics-Informed Neural Network](https://doi.org/10.1021/acs.jctc.5c00090) - P2Net parametrizes an analytical bond-order potential layer to decompose energy into atomic-pair contributions, giving interpretable bond analyses for reactions and improved data efficiency (Chun et al., 2025, Journal of Chemical Theory and Computation).

### Physics-informed: long-range

* [ReciNet: Reciprocal Space-Aware Long-Range Modeling for Crystalline Property Prediction](https://arxiv.org/abs/2502.02748) - Builds a learnable Fourier-series representation over reciprocal lattice vectors to capture long-range interactions and pairs it with a geometric GNN for crystal property prediction on JARVIS, MP and Matbench (Nie et al., 2025, arXiv).

### Physics-informed: loss/constraints

* [Machine learning materials physics: Integrable deep neural networks enable scale bridging by learning free energy functions](https://doi.org/10.1016/j.cma.2019.05.019) - An Integrable Deep Neural Network (IDNN) is trained on derivative (chemical potential) data of a B2-ordering binary alloy and analytically integrated to a thermodynamically consistent free energy, which in phase-field simulation correctly forms antiphase boundaries where a B-spline fit fails (Teichert et al., 2019, Computer Methods in Applied Mechanics and Engineering).
* [Joint learning equation of state surfaces with uncertainty-aware physically regularized neural networks](https://doi.org/10.1038/s41598-025-11874-2) - EOSNN jointly learns multiple P-T-V-E equation-of-state surfaces from compression and ab initio data with physical-consistency regularization and uncertainty quantification, outperforming traditional and Gaussian-process EOS models (Kuang et al., 2025, Scientific Reports).
* [Improving Reliability of Machine Learning Interatomic Potentials with Physics-Informed Pretraining](https://doi.org/10.1021/acs.jcim.6c00826) - Pretraining MLIPs (CGCNN, M3GNet, TorchMD-NET) on embedded-atom-model labels before fine-tuning on quantum-mechanical data consistently improves accuracy and MD stability for phosphorus, silica and a Materials Project subset (Zheng et al., 2026, Journal of Chemical Information and Modeling).

### Physics-informed: representation

* [Physical descriptor for the Gibbs energy of inorganic crystalline solids and temperature-dependent materials chemistry](https://doi.org/10.1038/s41467-018-06682-4) - A SISSO-derived physical descriptor predicts the Gibbs energy of stoichiometric inorganic compounds at 300-1800 K with ~50 meV/atom resolution, applied to ~30,000 ICSD materials to build temperature-dependent phase diagrams (Bartel et al., 2018, Nature Communications).
* [Orbital graph convolutional neural network for material property prediction](https://doi.org/10.1103/PhysRevMaterials.4.093801) - OGCNN augments crystal graph convolution with atomic orbital-interaction features and an encoder-decoder, significantly outperforming CGCNN, MBTR, SOAP and conventional regressors on crystalline property benchmarks (Karamad et al., 2020, Physical Review Materials).

### Physics-informed: review

* [Theory-Guided Data Science: A New Paradigm for Scientific Discovery from Data](https://doi.org/10.1109/TKDE.2017.2720168) - Conceptualizes theory-guided data science, with a taxonomy of ways to integrate scientific knowledge into data science models across disciplines including materials discovery (Karpatne et al., 2017, IEEE Transactions on Knowledge and Data Engineering).
* [Embedding domain knowledge for machine learning of complex material systems](https://doi.org/10.1557/mrc.2019.90) - Reviews strategies for embedding materials domain knowledge into ML algorithms, with examples of implementation and the materials systems to which they were applied (Childs et al., 2019, MRS Communications).

### Physics-informed: simulation-taught transport

* [Teaching Molecular Dynamics to a Non-Autoregressive Ionic Transport Predictor](https://arxiv.org/abs/2605.09311) - Proposes a non-autoregressive ionic-transport predictor that is taught by molecular-dynamics trajectories while predicting transport properties from static structures (Kim et al., 2026, ICML 2026).

### Semi-supervised and PU learning: positive-unlabeled learning

* [Structure-Based Synthesizability Prediction of Crystals Using Partially Supervised Learning](https://doi.org/10.1021/jacs.0c07384) - Structure-based crystal-likeness score from positive-unlabeled learning with graph networks, trained on known synthesized crystals and hypothetical structures treated as unlabeled (Jang et al., 2020, Journal of the American Chemical Society).
* [Perovskite synthesizability using graph neural networks](https://doi.org/10.1038/s41524-022-00757-z) - Positive-unlabeled learning with graph neural networks applied to the synthesizability of perovskite compositions and structures (Gu et al., 2022, npj Computational Materials).
* [Predicting the synthesizability of crystalline inorganic materials from the data of known material compositions](https://doi.org/10.1038/s41524-023-01114-4) - SynthNN: a deep model trained on the compositions of known materials that predicts synthesizability and is compared with expert judgement (Antoniuk et al., 2023, npj Computational Materials).
* [Synthesizability of materials stoichiometry using semi-supervised learning](https://doi.org/10.1016/j.matt.2024.05.002) - Semi-supervised synthesizability prediction from stoichiometry alone, for compositions whose structures are unknown (Jang et al., 2024, Matter).
* [SynCoTrain: a dual classifier PU-learning framework for synthesizability prediction](https://doi.org/10.1039/d4dd00394b) - SynCoTrain: a dual-classifier co-training positive-unlabeled framework for synthesizability prediction (Amariamir et al., 2025, Digital Discovery).
* [Crystal synthesizability prediction using contrastive positive unlabeled learning](https://doi.org/10.1016/j.cpc.2024.109465) - Contrastive positive-unlabeled learning for crystal synthesizability prediction (Sun et al., 2025, Computer Physics Communications).

### Semi-supervised and PU learning: semi-supervised learning

* [Materials synthesizability and stability prediction using a semi-supervised teacher-student dual neural network](https://doi.org/10.1039/d2dd00098a) - TSDNN: a semi-supervised teacher-student dual neural network that exploits many unlabelled samples for formation-energy and synthesizability prediction (Gleaves et al., 2023, Digital Discovery).

### Semi-supervised and PU learning: synthesizability

* [Predicting synthesizability of crystalline materials via deep learning](https://doi.org/10.1038/s43246-021-00219-x) - Deep learning on three-dimensional crystal images to classify crystalline materials as synthesizable or not (Davariashtiyani et al., 2021, Communications Materials).

### Superconductivity: 2D electron-phonon Tc screening

* [Machine-learning accelerated prediction of two-dimensional conventional superconductors](https://doi.org/10.1039/d4mh01753f) - ML models combined with DFPT electron-phonon calculations screen over 140,000 2D compounds from Alexandria, finding 105 systems with Tc > 5 K and showing that 2D materials have stronger electron-phonon coupling but lower average phonon frequencies, and hence lower Tc, than 3D counterparts (da Silva et al., 2025, Materials Horizons).

### Superconductivity: bonding descriptors (perspective)

* [Predictions of superconducting properties from chemical bonding interactions](https://arxiv.org/abs/2611.05784) - Perspective consolidating ELF networking-value theory and proposing a framework for Tc prediction of conventional superconductors from easily computable intermediate quantities (Belli et al., 2026, arXiv).

### Superconductivity: bonding descriptors for hydrides

* [Strong correlation between electronic bonding network and critical temperature in hydrogen-based superconductors](https://doi.org/10.1038/s41467-021-25687-0) - Across more than a hundred predicted hydrogen-based superconductors, the ELF-derived networking value correlates with Tc better than previous descriptors regardless of bonding type, and combined with hydrogen fraction and the hydrogen share of the Fermi-level DOS it predicts Tc with an accuracy of about 60 K (Belli et al., 2021, Nature Communications).
* [Refining Tc Prediction in Hydrides via Symbolic‐Regression‐Enhanced Electron‐Localization‐Function‐Based Descriptors](https://doi.org/10.1002/andp.202500280) - On 244 binary and ternary hydrides, the ELF networking descriptor loses accuracy with compositional complexity; a molecularity index plus symbolic regression substantially improves Tc prediction (Belli et al., 2025, Annalen der Physik).
* [TcESTIME: predicting high-temperature hydrogen-based superconductors](https://doi.org/10.1039/d4sc04465g) - TcESTIME combines a complex-network analysis of the ELF bonding network with an ML fit to estimate hydride Tc from DFT electronic properties in seconds, delivered through a web interface (Novoa et al., 2025, Chemical Science).
* [A chemical bonding based descriptor for predicting the role of anharmonicity induced by quantum nuclear effects in hydride superconductors](https://doi.org/10.1038/s41524-026-01973-7) - Bonding descriptors from iCOBI or the bond valence function predict whether quantum nuclear effects destabilize a lattice and enhance Tc in hydride superconductors (Belli et al., 2026, npj Computational Materials).

### Superconductivity: critical magnetic fields

* [Towards the discovery of high critical magnetic field superconductors](https://doi.org/10.1038/s41524-026-02266-9) - Consistent computational database of critical fields Hc, Hc1 and Hc2 for about 7300 electron-phonon superconductors from alpha2F and Eliashberg theory, enabling AI-guided design beyond Tc (Geisler et al., 2026, npj Computational Materials).

### Superconductivity: electron-phonon property ML screening

* [Sampling the Materials Space for Conventional Superconducting Compounds](https://doi.org/10.1002/adma.202307085) - An ML model trained on ~7000 electron-phonon calculations predicts electron-phonon and superconducting properties from structural, compositional and electronic ground-state features, screening ~200,000 near-hull metals and, after DFPT validation, identifying 541 compounds with Tc > 10 K, including LiMoN2 with predicted Tc above 38 K (Cerqueira et al., 2024, Advanced Materials).

### Superconductivity: electron-phonon Tc with dynamical instability

* [Machine-learning guided search for phonon-mediated superconductivity in boron and carbon compounds](https://doi.org/10.1038/s41524-026-01962-w) - An iterative DFPT/Eliashberg plus ML search over 417 boron, carbon and borocarbide compounds, explicitly including dynamically unstable structures with stabilized imaginary modes, compares two ML models and predicts near-hull superconductors such as Ca5B3N6 (35 K) and TaNbC2 (28.4 K) (Nepal et al., 2026, npj Computational Materials).

### Superconductivity: Eliashberg function and Tc (ALIGNN)

* [Designing high-TC superconductors with BCS-inspired screening, density functional theory, and deep-learning](https://doi.org/10.1038/s41524-022-00933-1) - Electron-phonon calculations on 1058 BCS-prescreened JARVIS materials yield 105 dynamically stable compounds with Tc >= 5 K, and ALIGNN deep-learning models trained on this database predict Tc better when the Eliashberg function is learned as an intermediate quantity than when Tc is predicted directly (Choudhary et al., 2022, npj Computational Materials).

### Superconductivity: Eliashberg spectral function

* [Accelerating superconductor discovery through tempered deep learning of the electron-phonon spectral function](https://doi.org/10.1038/s41524-024-01475-4) - BETE-NET, a bootstrapped ensemble of tempered equivariant GNNs trained on alpha2F for 818 materials, predicts its moments and gives Tc with an MAE of 2.1 K when site-projected phonon DOS is used as an inductive bias (Gibson et al., 2025, npj Computational Materials).

### Superconductivity: Eliashberg spectral function and discovery workflow

* [Developing a complete AI-accelerated workflow for superconductor discovery](https://doi.org/10.1038/s41524-026-01964-8) - BEE-NET predicts the Eliashberg function and Tc with 0.87 K MAE and a 99.4% true-negative rate; an AI-accelerated pipeline reduced 1.3 million candidates to 741 stable compounds with DFT Tc > 5 K, two of which were synthesized and confirmed superconducting (Gibson et al., 2026, npj Computational Materials).

### Superconductivity: generative design with ML screening

* [Inverse Design of Next-Generation Superconductors Using Data-Driven Deep Generative Models](https://doi.org/10.1021/acs.jpclett.3c01260) - A crystal diffusion variational autoencoder trained on about 1000 JARVIS DFT superconductors generates 3000 structures, which pretrained ALIGNN models screen to 61 candidates for DFT validation (Wines et al., 2023, The Journal of Physical Chemistry Letters).

### Superconductivity: hydride screening with a Tc model

* [High-throughput discovery of high-temperature conventional superconductors](https://doi.org/10.1103/physrevb.104.054501) - Crystal structure prediction across binary hydrides at 10-500 GPa combined with an iteratively refined Tc model built on density-of-states and Gaspari-Gyorffy inputs selects candidates for converged electron-phonon calculations, yielding 36 dynamically stable superconductors above 100 K, including NaH6 and CaH6 above 200 K at 100 GPa (Shipley et al., 2021, Physical Review B).

### Superconductivity: hydride Tc screening

* [Searching Materials Space for Hydride Superconductors at Ambient Pressure](https://doi.org/10.1002/adfm.202404043) - A machine-learning-assisted electron-phonon screening of more than 150,000 compounds finds about 50 ambient-pressure hydrides with Tc above 20 K (some above 70 K), mostly slightly thermodynamically unstable and combining alkali or alkaline-earth elements with noble metals (Cerqueira et al., 2024, Advanced Functional Materials).
* [Machine learning driven exploration of hydride superconductors at ambient pressure](https://doi.org/10.1016/j.commt.2026.100052) - Combining ab initio electron-phonon calculations with ML models to explore over two million hydride structures identifies more than 600 compounds with predicted Tc above 20 K, all above the convex hull (typically >100 meV/atom), with symbolic regression confirming that a large hydrogen contribution to the Fermi-level DOS marks high-Tc hydrides (Pires et al., 2026, Computational Materials Today).

### Superconductivity: hydride Tc under pressure (GNN + uMLFF)

* [Data-driven design of high pressure hydride superconductors using DFT and deep learning](https://doi.org/10.1088/2752-5724/ad4a94) - DFT Tc calculations for more than 900 hydrides at 0-500 GPa find 122 dynamically stable structures with Tc above that of MgB2 (39 K), and a GNN Tc model plus a universal ML force field for pressure-dependent relaxation are used to speed up screening (Wines et al., 2024, Materials Futures).

### Superconductivity: limits of conventional Tc

* [The maximum Tc of conventional superconductors at ambient pressure](https://doi.org/10.1038/s41467-025-63702-w) - Analyses electron-phonon calculations for over 20,000 metals from ML-assisted screens, with Tc estimated by the empirical McMillan-Allen-Dynes formula: omega_log rarely exceeds 1800 K, trades off against lambda, and higher-Tc compounds are increasingly unstable; a Gaussian approximation potential enables anharmonic SSCHA phonons for Li2AgH6, identified with Li2AuH6 as near the practical ambient-pressure limit (Gao et al., 2025, Nature Communications).

### Superconductivity: ML electron localization function

* [Geometry‐Based Neural‐Network Prediction of Electron Localization Function Topology in Dense Hydrogen](https://doi.org/10.1002/chem.202600030) - Neural network predicts the electron localization function of dense hydrogen from geometry, transferring from fluid to crystalline configurations while preserving ELF topology (Wang et al., 2026, Chemistry – A European Journal).

### Superconductivity: ML-guided hydride structure search

* [Predicting novel superconducting hydrides using machine learning approaches](https://doi.org/10.1103/physrevb.101.144505) - ML models steer crystal structure searches toward hydrides that superconduct closer to ambient conditions; electron-phonon calculations on stable candidates give Tc up to 115 K for RbH12 at 50 GPa (Hutcheon et al., 2020, Physical Review B).

### Superconductivity: MLIP-accelerated anharmonic (SSCHA) phonons

* [Efficient modelling of anharmonicity and quantum effects in PdCuH2 with machine learning potentials](https://doi.org/10.1038/s41524-025-01553-1) - Actively learned ML interatomic potentials paired with the SSCHA cut its cost by about 96% and identify a P4/mmm PdCuH2 phase that is dynamically stable only with quantum nuclear fluctuations as the likely source of the measured ambient-pressure superconductivity (Tc up to 17 K) (Belli et al., 2025, npj Computational Materials).

### Superconductivity: pairing symmetry

* [Machine learning protocol to identify pairing symmetries via quasiparticle interference imaging in Ising superconductors](https://doi.org/10.1103/7zvs-rnmt) - An ML strategy combining first-principles, tight-binding and symmetry-classified Bogoliubov-de Gennes simulations solves the QPI-to-pairing-parameter inverse problem with high accuracy for most pairing channels of monolayer NbSe2 (Hložný et al., 2026, Physical Review B).

### Superconductivity: property-guided generation

* [Guided diffusion for the discovery of new superconductors](https://doi.org/10.1038/s41524-026-02117-7) - DiffCSP pretrained on Alexandria and fine-tuned on 7183 superconductors with classifier-free guidance yields 773 candidates with DFT Tc > 5 K, with experimental validation (Prakash et al., 2026, npj Computational Materials).

### Superconductivity: stable hydride screening

* [Search for thermodynamically stable ambient-pressure superconducting hydrides in the GNoME database](https://doi.org/10.1038/s42005-026-02552-4) - A multistage screen combining machine learning for fast initial evaluation with ab initio Tc calculations over the thousands of 0 K-stable hydrides in GNoME finds 25 cubic hydrides with Tc above 4.2 K and a maximum of 17 K, modest but in phases likely to be experimentally accessible (Sanna et al., 2026, Communications Physics).

### Superconductivity: structure-based lambda and omega_log

* [Machine-learning approach for discovery of conventional superconductors](https://doi.org/10.1103/PhysRevMaterials.7.054805) - Instead of composition-plus-pressure Tc regression, ML models trained on 584 atomic structures predict the electron-phonon parameters lambda and omega_log, from which Tc is computed, and identify two previously synthesized materials with Tc of about 10-15 K at zero pressure (Huan et al., 2023, Physical Review Materials).

### Superconductivity: symbolic regression of Tc from alpha^2F

* [Machine learning of superconducting critical temperature from Eliashberg theory](https://doi.org/10.1038/s41524-021-00666-7) - SISSO symbolic regression on artificially generated alpha^2F(omega) spectra and numerical Eliashberg solutions yields a closed-form Tc formula that matches Allen-Dynes for low-Tc superconductors and substantially corrects its systematic underestimation for higher-Tc ones (Xie et al., 2022, npj Computational Materials).

### Symbolic regression: descriptor discovery

* [Simple descriptor derived from symbolic regression accelerating the discovery of new perovskite catalysts](https://doi.org/10.1038/s41467-020-17263-9) - Symbolic regression finds a simple descriptor (mu/t) for oxide-perovskite OER activity; guided synthesis of new perovskite catalysts with improved activity (Weng et al., 2020, Nature Communications).

### Symbolic regression: general-purpose symbolic regression

* [Composition-Weighted Symbolic Regression for General-Purpose Property Prediction](https://arxiv.org/abs/2605.02267) - Composition-weighted symbolic regression that builds formulas from elemental features for general-purpose property prediction (Huang et al., 2026, arXiv).

### Symbolic regression: hybrid GNN and symbolic regression

* [SA-GAT-SR: self-adaptable graph attention networks with symbolic regression for high-fidelity material property prediction](https://doi.org/10.1038/s41524-025-01854-5) - SA-GAT-SR: graph attention network whose selected features are passed to symbolic regression, combining GNN accuracy with an explicit formula (Liu et al., 2025, npj Computational Materials).

### Symbolic regression: interatomic potentials

* [Physically interpretable interatomic potentials via symbolic regression and reinforcement learning](https://doi.org/10.1038/s41524-025-01952-4) - Physically interpretable interatomic potentials discovered by symbolic regression with reinforcement learning (Varughese et al., 2026, npj Computational Materials).

### Symbolic regression: LLM-guided formula discovery

* [LLM-Feynman: Leveraging Large Language Models for Universal Scientific Formula and Theory Discovery](https://arxiv.org/abs/2503.06512) - LLM-Feynman: LLM-generated candidate formulas refined by systematic optimization and self-evaluation; rediscovers most Feynman-lecture formulas and finds interpretable formulas for materials problems such as 2D synthesizability (Song et al., 2025, arXiv).

### Symbolic regression: SISSO

* [Materials-discovery workflow guided by symbolic regression for identifying acid-stable oxides for electrocatalysis](https://doi.org/10.1038/s41524-025-01596-4) - Discovery workflow guided by SISSO symbolic regression that identifies acid-stable oxides for electrocatalysis from a small set of DFT data (Nair et al., 2025, npj Computational Materials).
* [Unveiling the Core of Materials Properties via SISSO and Sensitivity Analysis](https://arxiv.org/abs/2604.08122) - SISSO combined with sensitivity analysis to identify the key physical parameters that govern materials properties (Foppa et al., 2026, arXiv).

### Thermal conductivity: active-learned MLIP screening

* [Machine Learning Discovery of Record-Low Lattice Thermal Conductivity in Double Perovskites](https://doi.org/10.1002/advs.202515766) - An active-learned deep MLIP (Elemental-SDNNFF) coupled to the BTE screens 9,709 cubic double perovskites (1,597 dynamically stable) and finds Cs2HgPtCl6 with a room-temperature kappa_L of 0.071 W/mK, confirmed with four-phonon DFT and DeePMD MD (Anam et al., 2026, Advanced Science).

### Thermal conductivity: Bayesian optimization on first-principles kappa_L

* [Prediction of Low-Thermal-Conductivity Compounds with First-Principles Anharmonic Lattice-Dynamics Calculations and Bayesian Optimization](https://doi.org/10.1103/physrevlett.115.205901) - Bayesian optimization seeded with first-principles anharmonic lattice-dynamics kappa_L for 101 compounds screens a 54,779-compound library and finds 221 very-low-kappa_L materials (Seko et al., 2015, Physical Review Letters).

### Thermal conductivity: feature-based transfer learning

* [Exploring diamondlike lattice thermal conductivity crystals via feature-based transfer learning](https://doi.org/10.1103/physrevmaterials.5.053801) - Transfers descriptors from a network pretrained on a data-rich lower-order property to a small kappa_L dataset, enabling extrapolative screening of over 60,000 compounds for diamond-like high-kappa_L crystals and identifying polarizability and van der Waals radius as anharmonicity-related descriptors (Ju et al., 2021, Physical Review Materials).

### Thermal conductivity: GNN and random forest on computed kappa_L

* [Charting lattice thermal conductivity for inorganic crystals and discovering rare earth chalcogenides for thermoelectrics](https://doi.org/10.1039/d1ee00442e) - CGCNN and random-forest models trained on about 2,700 computed kappa values predict log kappa with MAE below 0.15 and R2 above 0.85, chart kappa_L for all ordered ICSD crystals, and lead to rare-earth chalcogenide thermoelectric candidates (Zhu et al., 2021, Energy & Environmental Science).

### Thermal conductivity: GNN on bonding descriptors

* [Accelerated discovery of extreme lattice thermal conductivity by crystal graph attention networks and chemical bonding](https://doi.org/10.1038/s41524-025-01871-4) - A crystal attention GNN predicts normalized -ICOHP and ICOBI bonding descriptors that correlate with kappa_L across more than 4,500 crystals, screens about 200,000 structures, and DFT validation finds 106 stable compounds below 5 W/mK and 13 above 100 W/mK (Al-Fahdi et al., 2025, npj Computational Materials).

### Thermal conductivity: interpretable physics formula

* [An interpretable formula for lattice thermal conductivity of crystals](https://doi.org/10.1016/j.mtphys.2024.101549) - An interpretable, dimensionally consistent formula based on bulk modulus, shear modulus and Grueneisen parameter predicts kappa_L with 8.97% mean relative error and is applied to 4,601 binary and 6,995 ternary Materials Project compounds, predicting high kappa_L of 101 W/mK for AlBN2 (Wang et al., 2024, Materials Today Physics).

### Thermal conductivity: Matminer-descriptor GPR on experimental kappa_L

* [Machine learning models for the lattice thermal conductivity prediction of inorganic materials](https://doi.org/10.1016/j.commatsci.2019.109155) - Gaussian process regression on 61 Matminer elemental, structural and valence-electron features, reduced by recursive feature elimination, predicts experimentally measured kappa_L for about 100 inorganic compounds (81 binary, 19 ternary) and is compared with earlier theoretical models (Chen et al., 2019, Computational Materials Science).

### Thermal conductivity: ML-assisted half-Heusler screening

* [Finding Unprecedentedly Low-Thermal-Conductivity Half-Heusler Semiconductors via High-Throughput Materials Modeling](https://doi.org/10.1103/physrevx.4.011019) - Combines ML, physical insight and ab initio calculations to scan about 79,000 AFLOW half-Heusler entries, finding kappa_L spanning more than two orders of magnitude among 450 mechanically stable semiconductors and estimating kappa_L for 77 thermodynamically stable ones (Carrete et al., 2014, Physical Review X).

### Thermal conductivity: MLIP (moment tensor potential)

* [Accessing thermal conductivity of complex compounds by machine learning interatomic potentials](https://doi.org/10.1103/physrevb.100.144308) - Actively learned moment tensor potentials trained on a few hundred DFT calculations reproduce the phonon spectrum and the BTE and Green-Kubo lattice thermal conductivity of the complex skutterudite CoSb3 (Korotaev et al., 2019, Physical Review B).
* [Accelerating first-principles estimation of thermal conductivity by machine-learning interatomic potentials: A MTP/ShengBTE solution](https://doi.org/10.1016/j.cpc.2020.107583) - Moment tensor potentials trained on short AIMD trajectories replace DFT in computing anharmonic force constants for ShengBTE, reproducing full-DFT thermal conductivities of several bulk and 2D materials at much lower cost (Mortazavi et al., 2021, Computer Physics Communications).

### Thermal conductivity: MLIP (polynomial, on-the-fly)

* [On-the-fly training of polynomial machine learning potentials in computing lattice thermal conductivity](https://doi.org/10.1063/5.0211296) - Integrates on-the-fly polynomial MLIPs into a modular phono3py kappa_L workflow and tests it on 103 wurtzite, zinc-blende and rocksalt compounds, greatly reducing the DFT cost of high-throughput kappa_L calculations (Togo et al., 2024, The Journal of Chemical Physics).

### Thermal conductivity: phonon-descriptor GPR

* [Coupling the High-Throughput Property Map to Machine Learning for Predicting Lattice Thermal Conductivity](https://doi.org/10.1021/acs.chemmater.9b01046) - High-throughput ab initio kappa_L for 120 stable nonmetallic compounds identifies four descriptors (maximum phonon frequency, integrated Grueneisen parameter up to 3 THz, average mass, cell volume), and a GPR model on them predicts log kappa_L with RMSE of about 0.21 while the Slack model strongly overestimates it (Juneja et al., 2019, Chemistry of Materials).

### Thermal conductivity: SISSO symbolic regression with sensitivity analysis

* [Accelerating materials-space exploration for thermal insulators by mapping materials properties via artificial intelligence](https://doi.org/10.1038/s41524-023-01063-y) - SISSO symbolic regression with sensitivity analysis gives an analytic kappa_L model from only 75 experimental values, whose most influential inputs drive a hierarchical screen of 732 materials that finds 80 ultra-insulators (Purcell et al., 2023, npj Computational Materials).

### Thermal conductivity: symbolic regression

* [Lattice Thermal Conductivity Prediction Using Symbolic Regression and Machine Learning](https://doi.org/10.1021/acs.jpca.0c08103) - Genetic-programming symbolic regression finds four analytical kappa_L formulae that beat the Slack formula on the authors' dataset, and shows that extrapolation to differently distributed data remains hard for both symbolic regression and ML models (Loftis et al., 2020, The Journal of Physical Chemistry A).

### Thermal conductivity: uMLIP fine-tuning for high-throughput kappa_L

* [Symmetry-Based Parameter Efficient Low-Rank Fine-Tuning for High-Throughput Calculation of Lattice Thermal Conductivity](https://arxiv.org/abs/2610.29634) - Symmetry-based few-shot LoRA fine-tuning of MatterSim 1M on a few compounds per space group (half-Heuslers, Fm-3m, spinels) cuts the mean absolute relative kappa_L error by 2-3 times compared with the non-fine-tuned model, and is 5-7 times faster than fine-tuning per compound across 100 compounds (Arabov et al., 2026, arXiv).

### Thermal conductivity: uMLIP-based ultralow-kappa screening

* [Accelerated discovery of crystalline materials with record ultralow lattice thermal conductivity via a universal descriptor](https://doi.org/10.1038/s41467-025-67333-z) - A descriptor using only the number of atoms in the primitive cell and the sound velocity, combined with uMLIP high-throughput workflows, screens over 25,000 materials and leads to the experimental record-low kappa of 0.15-0.16 W/mK in CsAg2I3 (170-400 K) (Shen et al., 2025, Nature Communications).
* [Approaching the Limit of Intrinsic Crystalline Thermal Insulation](https://arxiv.org/abs/2606.11072) - A high-throughput workflow coupling uMLIPs with particle-like and wave-like (Wigner) phonon transport finds dozens of crystals with room-temperature kappa below 0.2 W/mK and experimentally validates CsTlI4 at 0.14 W/mK, with force-constant-based descriptors for ultralow kappa (Cheng et al., 2026, arXiv).

### Thermoelectrics: band-structure descriptor

* [Effective mass and Fermi surface complexity factor from ab initio band structure calculations](https://doi.org/10.1038/s41524-017-0013-3) - Boltzmann transport on ab initio band structures yields Seebeck- and conductivity-derived effective masses whose ratio defines a Fermi-surface complexity factor N_v*K* (valley degeneracy times anisotropy), which is high in good thermoelectrics such as PbTe and is proposed for high-throughput screening (Gibbs et al., 2017, npj Computational Materials).

### Thermoelectrics: crystal graphs vs DFT descriptors for power factor

* [Predicting thermoelectric properties from crystal graphs and material descriptors - first application for functional materials](https://arxiv.org/abs/1811.06219) - A three-layer fully connected network on Materials Project-mined bonding and density-of-states descriptors predicts the scattering-time-independent power factor much better than CGCNN or XGBoost trained on crystal and atomic information alone (Laugier et al., 2018, arXiv).

### Thermoelectrics: crystal-graph GNN for electronic transport

* [Learning thermoelectric transport from crystal structures via multiscale graph neural network](https://doi.org/10.1103/m8nb-bbp8) - A multiscale GNN that encodes crystals at global, atomic, bond and angle levels reaches state-of-the-art accuracy on electronic-transport benchmarks with good extrapolation, and with ab initio checks it identifies compounds with outstanding electronic transport (the abstract gives no headline error) (Zeng et al., 2026, Physical Review Applied).

### Thermoelectrics: DFT-derived features for power factor

* [Machine learning based feature engineering for thermoelectric materials by design](https://doi.org/10.1039/d3dd00131h) - On a dataset of Materials Project-derived features paired with calculated thermoelectric power factors, an interpretable random forest beats more complex models (the abstract gives no headline metric) (Vaitesswar et al., 2024, Digital Discovery).

### Thermoelectrics: generative inverse-design screening with ML surrogates

* [Inverse design of functional materials: a case study in thermoelectrics](https://doi.org/10.1038/s41524-026-02307-3) - A CDVAE trained on MatHub-3d generated 6400 structures. M3GNet and MEGNet surrogates cut 1461 unique compositions to about 1000 stable candidates, DFT deformation-potential transport screening left 64, and phonon calculations confirmed four new dynamically stable compounds with kappa_L of 0.67-1.72 W m^-1 K^-1 (Wang et al., 2026, npj Computational Materials).

### Thermoelectrics: high-throughput ZT workflow with ML

* [High-Throughput Prediction of the Thermal and Electronic Transport Properties of Large Physical and Chemical Spaces Accelerated by Machine Learning: Charting the <i>ZT</i> of Binary Skutterudites](https://doi.org/10.1021/acsami.3c15741) - Combines new ab initio electron and phonon transport methods with machine learning in a high-throughput framework to chart ZT across the whole binary-skutterudite family as a function of carrier concentration, grain size and temperature, for both p- and n-type (Santana-Andreo et al., 2024, ACS Applied Materials & Interfaces).

### Thermoelectrics: ML interpolation of electron-phonon coupling

* [Generalized deformation potential and machine-learning approaches for electron-phonon coupling and thermoelectric transport in semiconductors](https://doi.org/10.1103/8wwd-8ymg) - Machine-learning interpolation of about 100 first-principles electron-phonon matrix elements per band and mode reproduces state-of-the-art thermoelectric transport for 2D MoS2 and agrees well with experiment, with better accuracy than a generalized deformation-potential model (D'Souza et al., 2026, Physical Review B).

### Thermoelectrics: orbital-field-matrix CNN on AMSET data

* [High-throughput thermoelectric materials screening by deep convolutional neural network with fused orbital field matrix and composition descriptors](https://doi.org/10.1063/5.0187855) - A CNN classifier on fused orbital-field-matrix and composition descriptors, trained on in-house DFT plus AMSET transport data (no constant relaxation time), screened 3465 cubic, dynamically stable OQMD semiconductors for power factor above 10 uW cm^-1 K^-2 and identified many candidates with ZT near or above 1 at 300-700 K (Al-Fahdi et al., 2024, Applied Physics Reviews).

### Thermoelectrics: physical descriptors beyond constant relaxation time

* [Material Descriptors for the Discovery of Efficient Thermoelectrics](https://doi.org/10.1021/acsaem.0c00825) - Full energy- and momentum-dependent electron-phonon and ionized-impurity scattering calculations on half-Heuslers identify n_v*eps_r/(D_o^2*m_cond) (valleys, dielectric constant, conductivity mass, deformation potential) as the most useful generic descriptor of optimal power factor for screening (Graziosi et al., 2020, ACS Applied Energy Materials).

### Thermoelectrics: structure descriptors on BoltzTraP data

* [Data-driven discovery of 3D and 2D thermoelectric materials](https://doi.org/10.1088/1361-648x/aba06b) - BoltzTraP screening of about 36,000 3D and 900 2D JARVIS-DFT materials found 2932 3D and 148 2D candidates, and gradient-boosted trees on structure-aware classical-force-field-inspired descriptors (CFID) were trained to predict n- and p-type Seebeck coefficients and power factors to pre-screen materials before further DFT (Choudhary et al., 2020, Journal of Physics: Condensed Matter).

### Transformer

* [Periodic Graph Transformers for Crystal Material Property Prediction](https://doi.org/10.52202/068431-1096) - Periodic graph transformer (Matformer) encoding lattice periodicity for crystal property prediction (Yan et al., 2022, Advances in Neural Information Processing Systems 35). [[code](https://github.com/YKQ98/Matformer)]
* [Efficient Approximations of Complete Interatomic Potentials for Crystal Property Prediction](https://arxiv.org/abs/2306.10045) - Crystal GNN using efficiently approximated complete infinite-sum interatomic potentials (PotNet) (Lin et al., 2023, ICML 2023). [[code](https://github.com/divelab/AIRS)]
* [Crystalformer: Infinitely Connected Attention for Periodic Structure Encoding](https://arxiv.org/abs/2403.11686) - Transformer with infinitely connected attention over periodic structures for crystal property prediction (Taniai et al., 2024, ICLR 2024). [[code](https://github.com/omron-sinicx/crystalformer)]
* [Complete and Efficient Graph Transformers for Crystal Material Property Prediction](https://arxiv.org/abs/2403.11857) - SE(3)-invariant and equivariant crystal graph transformers (ComFormer) with complete crystal representations (Yan et al., 2024, ICLR 2024). [[code](https://github.com/divelab/AIRS)]
* [A Cartesian encoding graph neural network for crystal structure property prediction: application to thermal ellipsoid estimation](https://doi.org/10.1039/d4dd00352g) - Cartesian-encoding GNN (CartNet) for crystal properties including anisotropic thermal ellipsoids (Solé et al., 2025, Digital Discovery). [[code](https://github.com/imatge-upc/CartNet)]

## OOD Generalization, Redundancy and Uncertainty

### Applicability domain

* [A general approach for determining applicability domain of machine learning models](https://doi.org/10.1038/s41524-025-01573-x) - Uses kernel density estimation in feature space to define model applicability domains, flagging inputs where errors and uncertainty estimates become unreliable (Schultz et al., 2025, npj Computational Materials).

### Calibration

* [Calibrated uncertainty for molecular property prediction using ensembles of message passing neural networks](https://doi.org/10.1088/2632-2153/ac3eb3) - Combines MPNN ensembles with recalibration to obtain well-calibrated predictive uncertainties for atomistic property prediction (Busk et al., 2021, Machine Learning: Science and Technology).
* [Calibration after bootstrap for accurate uncertainty quantification in regression models](https://doi.org/10.1038/s41524-022-00794-8) - Shows bootstrap-ensemble uncertainties are miscalibrated and proposes a simple post-hoc recalibration that yields accurate error bars for materials regression (Palmer et al., 2022, npj Computational Materials).

### Distribution shift

* [Not as simple as we thought: a rigorous examination of data aggregation in materials informatics](https://doi.org/10.1039/D3DD00207A) - Shows that naively aggregating materials datasets from different sources does not reliably improve, and can harm, predictive performance, particularly for OOD samples (Ottomano et al., 2024, Digital Discovery).

### Domain adaptation

* [Realistic material property prediction using domain adaptation based machine learning](https://doi.org/10.1039/D3DD00162H) - Frames OOD materials prediction with known target test sets as domain adaptation and shows DA methods improve accuracy on several realistic split scenarios (Hu et al., 2024, Digital Discovery).
* [Out-of-Distribution Material Property Prediction Using Adversarial Learning](https://doi.org/10.1021/acs.jpcc.4c07481) - Uses adversarial (domain-adversarial) learning to improve materials property prediction on out-of-distribution test sets (Li et al., 2025, The Journal of Physical Chemistry C).

### Evaluation pitfalls

* [Machine-learned metrics for predicting the likelihood of success in materials discovery](https://doi.org/10.1038/s41524-020-00401-8) - Introduces metrics (e.g., predicted fraction of improved candidates) to estimate in advance how likely an ML-guided search is to find improved materials (Kim et al., 2020, npj Computational Materials).
* [Robust model benchmarking and bias-imbalance in data-driven materials science: a case study on MODNet](https://doi.org/10.1088/1361-648X/ac1280) - Shows how dataset bias and imbalance distort benchmark error estimates and discusses robust evaluation, using MODNet as a case study (De Breuck et al., 2021, Journal of Physics: Condensed Matter). [[code](https://github.com/ppdebreuck/modnet)]
* [Quantifying the performance of machine learning models in materials discovery](https://doi.org/10.1039/D2DD00113F) - Argues standard error metrics poorly reflect discovery success and proposes discovery-oriented metrics based on sequential-learning simulations (Borg et al., 2023, Digital Discovery).

### Extrapolation

* [Can machine learning find extraordinary materials?](https://doi.org/10.1016/j.commatsci.2019.109498) - Evaluates whether regression and classification models can identify materials with property values exceeding those in the training data (Kauwe et al., 2020, Computational Materials Science).
* [Evaluating explorative prediction power of machine learning algorithms for materials discovery using k-fold forward cross-validation](https://doi.org/10.1016/j.commatsci.2019.109203) - Proposes k-fold forward cross-validation, sorting samples by property value to measure ability to predict beyond the training range (Xiong et al., 2020, Computational Materials Science).
* [Known Unknowns: Out-of-Distribution Property Prediction in Materials and Molecules](https://doi.org/10.1038/s41524-025-01808-x) - Applies bilinear transduction to extrapolate to property values outside the training range, improving recall of high-performing materials and molecules (Segal et al., 2025, npj Computational Materials).
* [Achieving robust extrapolation in materials property prediction via decoupled transfer learning](https://doi.org/10.1103/pbrg-x848) - Proposes a decoupled transfer-learning scheme to improve extrapolative prediction of materials properties beyond the training distribution (Sugiura et al., 2026, PRX Intelligence).

### Improving OOD: test-time refinement

* [Understanding and mitigating distribution shifts for universal machine learning interatomic potentials](https://doi.org/10.1039/d5dd00260e) - Diagnoses distribution shifts that degrade MLFF foundation models and proposes two test-time refinements (spectral graph rewiring of test graphs and gradient steps on an auxiliary physical prior) without ab initio labels (Kreiman et al., 2026, Digital Discovery).

### OOD benchmark

* [Can machine learning identify the next high-temperature superconductor? Examining extrapolation performance for materials discovery](https://doi.org/10.1039/C8ME00012C) - Introduces leave-one-cluster-out cross-validation (LOCO CV) to assess extrapolation of materials ML models to new chemistries (Meredig et al., 2018, Molecular Systems Design & Engineering).
* [Probing out-of-distribution generalization in machine learning for materials](https://doi.org/10.1038/s43246-024-00731-w) - Analyzes many OOD tasks across chemistry and structure splits and finds most heuristic OOD tasks are actually covered by the training representation space, with only a few being truly challenging (Li et al., 2025, Communications Materials).

### Redundancy

* [Exploiting redundancy in large materials datasets for efficient machine learning with less data](https://doi.org/10.1038/s41467-023-42992-y) - Shows that large fractions of materials training sets are redundant and can be pruned with little loss of in-distribution accuracy, while OOD performance is not improved by more redundant data (Li et al., 2023, Nature Communications).
* [MD-HIT: Machine learning for material property prediction with dataset redundancy control](https://doi.org/10.1038/s41524-024-01426-z) - Proposes MD-HIT, a CD-HIT-like redundancy-reduction algorithm for composition and structure datasets, showing random-split benchmarks overestimate performance (Li et al., 2024, npj Computational Materials). [[code](https://github.com/usccolumbia/MD-HIT)]

### Uncertainty quantification

* [MatUQ: a benchmark for uncertainty-aware out-of-distribution materials property prediction with graph neural networks](https://doi.org/10.1038/s41524-026-02272-x) - Benchmark for uncertainty-aware OOD materials property prediction with GNNs (Tan et al., 2026, npj Computational Materials).

### Uncertainty: bootstrap, dropout, random-init and snapshot ensembles

* [Comparative study of ensemble-based uncertainty quantification methods for neural network interatomic potentials](https://doi.org/10.1088/2632-2153/ae9fb4) - Compares bootstrap, dropout, random-initialization and snapshot ensembles for carbon-allotrope NN potentials in- and out-of-distribution (cold curves, phonons), finding that OOD uncertainty can plateau or even decrease as true error grows, so precision is not a reliable proxy for accuracy on system-level predictions (Kurniawan et al., 2026, Machine Learning: Science and Technology).

### Uncertainty: conditional coverage

* [Null-Corrected Conditional Coverage in Materials Property Prediction: A Five-Dataset Replication](https://arxiv.org/abs/2611.14521) - Replicates conditional-coverage evaluation of seven interval (including conformal-style) methods across five materials datasets with a null-corrected worst-bin statistic (Boruah et al., 2026, arXiv).

### Uncertainty: conformal prediction with latent distances

* [Robust and scalable uncertainty estimation with conformal prediction for machine-learned interatomic potentials](https://doi.org/10.1088/2632-2153/aca7b1) - Combines conformal prediction with latent-space distances (CP+latent) for neural network force-field energies, giving calibrated and sharp intervals under i.i.d. data that are insensitive to hyperparameters and scale to a 1-million-image training set, while degrading when the i.i.d. assumption is violated (Hu et al., 2022, Machine Learning: Science and Technology).

### Uncertainty: conformal-style learned quantile calibration

* [Flexible uncertainty calibration for machine-learned interatomic potentials](https://doi.org/10.1038/s41524-026-02080-3) - Recasts conformal prediction as a parameterized optimization that learns environment-dependent quantile functions on top of MACE-MP-0, giving substantially (order-of-magnitude in the preprint) better uncertainty-error correlation on ionic crystals, catalytic surfaces and molecules and transferring calibration across exchange-correlation functionals (Ho et al., 2026, npj Computational Materials).

### Uncertainty: ensembles, MC dropout and evidential regression for CGCNN

* [Clarifying trust of materials property predictions using neural networks with distribution-specific uncertainty quantification](https://doi.org/10.1088/2632-2153/accace) - Benchmarks k-fold ensembling, Monte Carlo dropout and evidential regression on a CGCNN predicting OC20 adsorption energies on alloys using accuracy, sharpness, dispersion, calibration and tightness, finding evidential regression competitively trustworthy at low cost and post-hoc recalibration essential for screening (Gruich et al., 2023, Machine Learning: Science and Technology).

### Uncertainty: evidential regression for potentials

* [Evidential deep learning for interatomic potentials](https://doi.org/10.1038/s41467-025-67663-y) - Introduces a physics-inspired evidential interatomic potential (eIP) that gives single-pass uncertainties without loss of accuracy, consistently outperforming other UQ methods across datasets and supporting active exploration of water and universal potentials (Xu et al., 2025, Nature Communications).

### Uncertainty: Gaussian processes, bagging and dropout BNNs for descriptor models

* [Modelling magnetic material properties with uncertainty-aware neural networks](https://doi.org/10.1016/j.commatsci.2026.115073) - Benchmarks Gaussian process regression, random-forest bagging and dropout Bayesian NNs on Curie-temperature and Nd2Fe14B intrinsic-property data, showing that calibration, sharpness and confidence-curve diagnostics separate methods that look equivalent on point-error metrics, and extends the approach to GNN coercivity prediction (Wager et al., 2026, Computational Materials Science).

### Uncertainty: GNN features with Gaussian-process head

* [Entropy-based active learning of graph neural network surrogate models for materials properties](https://doi.org/10.1063/5.0065694) - Couples a crystal GNN featurizer with a Gaussian-process head to give predictive variances for solid-state properties and uses them for entropy-based active learning, doubling the rate of test-error improvement relative to random sampling (Allotey et al., 2021, The Journal of Chemical Physics).

### Uncertainty: heterogeneous ensembles of universal potentials

* [Heterogeneous ensemble enables a universal uncertainty metric for atomistic foundation models](https://doi.org/10.1038/s41524-025-01905-x) - Builds an uncertainty metric U from disagreement among different pretrained uMLIPs that tracks true errors across diverse chemistries, and uses it for uncertainty-aware distillation that matches full-DFT training for W with only 4% of the DFT labels (Liu et al., 2025, npj Computational Materials).

### Uncertainty: last-layer prediction rigidity (Laplace-like)

* [A prediction rigidity formalism for low-cost uncertainties in trained neural networks](https://doi.org/10.1088/2632-2153/ad805f) - Derives prediction rigidities from a constrained optimization linked to Bayesian inference and a justified last-layer approximation, giving cheap post-hoc uncertainties for any pretrained neural regressor without changing the network or training, demonstrated from toy models to chemistry and meteorology (Bigi et al., 2024, Machine Learning: Science and Technology).

### Uncertainty: latent Mahalanobis extrapolation grade for foundation potentials

* [A latent-space extrapolation grade built into graph atomic cluster expansion foundation potentials](https://arxiv.org/abs/2609.40060) - Builds a calibrated per-atom Mahalanobis extrapolation grade (CALM) into GRACE foundation potentials that correlates with force errors on OMat24 and SMAX, detects structural and chemical extrapolation, and costs only percent-level extra compute (Lysogorskiy et al., 2026, arXiv).

### Uncertainty: latent-distance UQ with distribution-free recalibration

* [Improved Uncertainty Estimation of Graph Neural Network Potentials Using Engineered Latent Space Distances](https://doi.org/10.1021/acs.jpcc.4c04972) - Builds an OC20 relaxed-energy UQ benchmark for equivariant GNNs with distribution-free recalibration and finds engineered latent-distance methods the best-calibrated and most economical option, with sensible behaviour on out-of-training equation-of-state and adsorbate-coverage cases (Musielewicz et al., 2024, The Journal of Physical Chemistry C).

### Uncertainty: MC dropout Bayesian potential

* [Uncertainty quantification in molecular simulations with dropout neural network potentials](https://doi.org/10.1038/s41524-020-00390-8) - Proposes dropout uncertainty neural network (DUNN) potentials, applied to carbon, that propagate energy and force uncertainty to stress and graphene phonon dispersion and flag configurations outside the training set (Wen et al., 2020, npj Computational Materials).

### Uncertainty: MC dropout for crystal GNNs

* [Uncertainty-Quantified Hybrid Machine Learning/Density Functional Theory High Throughput Screening Method for Crystals](https://doi.org/10.1021/acs.jcim.0c00003) - CGCNN-HD adds tanh activations and dropout-based uncertainty to CGCNN formation-energy prediction, cutting DFT calculations by more than 50x in a Mg-Mn-O photoanode screen and raising discoverability of promising materials from 30% (plain CGCNN) to 68% (Noh et al., 2020, Journal of Chemical Information and Modeling).

### Uncertainty: OOD detection

* [MOOD: Benchmarking Post-Hoc OOD Detection for Materials Property Prediction](https://arxiv.org/abs/2611.11839) - Benchmarks 15 post-hoc OOD detectors and 2 probes across 4 GNNs, 5 MatBench tasks and 15 compositional/structural shifts (Yu et al., 2026, NeurIPS 2026 Evaluations & Datasets Track).

### Uncertainty: post-hoc

* [P-DRUM: Post-hoc Descriptor-based Residual Uncertainty Modeling for Machine Learning Potentials](https://arxiv.org/abs/2509.02927) - Proposes a post-hoc UQ method that uses descriptors of an already-trained GNN potential to model residual errors, as a cheap alternative to ensembles (Huang et al., 2025, NeurIPS 2025 ML4PS workshop).

### Uncertainty: quantile regression, direct interval models and Gaussian processes

* [Uncertainty Prediction for Machine Learning Models of Material Properties](https://doi.org/10.1021/acsomega.1c03752) - Compares quantile-loss models, direct learning of prediction intervals and Gaussian processes for per-sample prediction intervals on 12 JARVIS-DFT properties, slightly favouring direct interval modelling as easiest to fit and least prone to over- or under-estimating errors (Tavazza et al., 2021, ACS Omega). [[code](https://github.com/usnistgov/jarvis)]

### Uncertainty: readout ensembles and quantile regression for foundation potentials

* [Uncertainty quantification for neural network potential foundation models](https://doi.org/10.1038/s41524-025-01572-y) - Introduces readout ensembling (fine-tuning only readout layers of an ensemble of MACE-MP-0 copies) for epistemic uncertainty and quantile regression for aleatoric uncertainty, showing on the foundation model and fine-tuned variants that the two give distinct, complementary measures of output quality (Bilbrey et al., 2025, npj Computational Materials).

### Uncertainty: shallow (last-layer) ensembles

* [Uncertainty quantification by direct propagation of shallow ensembles](https://doi.org/10.1088/2632-2153/ad594a) - Proposes direct propagation of shallow ensembles (multiple heads on a shared backbone trained with an NLL loss) as a low-overhead UQ scheme that propagates errors to derived quantities without correlation assumptions, benchmarked on generic and atomistic chemistry and materials tasks (Kellner et al., 2024, Machine Learning: Science and Technology).

### Uncertainty: shallow ensembles and last-layer Laplace

* [How to Train a Shallow Ensemble](https://doi.org/10.1021/acs.jctc.6c00310) - Shows that explicit NLL training of shallow ensembles calibrates better than random-initialization ensembles or last-layer Laplace, that force uncertainties need their own NLL term, and that fine-tuning from an energy-trained or Laplace-sampled ensemble keeps calibration while cutting training time by up to 96% across systems including amorphous carbon and BaTiO3 (Schäfer et al., 2026, Journal of Chemical Theory and Computation).

### Uncertainty: single-model latent-feature uncertainty

* [Fast uncertainty estimates in deep learning interatomic potentials](https://doi.org/10.1063/5.0136574) - Estimates uncertainty from a single equivariant interatomic potential with virtually no extra training or inference cost, matching deep-ensemble uncertainty quality and ensemble-driven active learning at an order-of-magnitude lower cost (Zhu et al., 2023, The Journal of Chemical Physics).

### Uncertainty: tensor outputs

* [Equivariant Covariance Tensors: Guaranteed SPD Uncertainty for Tensor-Valued Geometric Learning](https://arxiv.org/abs/2608.24386) - Introduces E(3)-equivariant prediction of full 6x6 covariance matrices with guaranteed SPD structure for rank-2 tensor-valued targets (Liu et al., 2026, ICML 2026).

### UQ

* [A quantitative uncertainty metric controls error in neural network-driven chemical discovery](https://doi.org/10.1039/C9SC02298H) - Proposes a latent-space distance uncertainty metric for neural networks that controls error in transition-metal complex discovery, outperforming ensembles at lower cost (Janet et al., 2019, Chemical Science).
* [Uncertainty Quantification Using Neural Networks for Molecular Property Prediction](https://doi.org/10.1021/acs.jcim.0c00502) - Systematically compares ensemble, dropout, MVE and other NN UQ methods, finding no single method dominates across datasets and metrics (Hirschfeld et al., 2020, Journal of Chemical Information and Modeling).
* [Methods for comparing uncertainty quantifications for material property predictions](https://doi.org/10.1088/2632-2153/ab7e1a) - Compares UQ methods for adsorption-energy prediction and proposes evaluation via accuracy, calibration, sharpness and NLL (Tran et al., 2020, Machine Learning: Science and Technology). [[code](https://github.com/ulissigroup/uncertainty_benchmarking)]
* [Evidential Deep Learning for Guided Molecular Property Prediction and Discovery](https://doi.org/10.1021/acscentsci.1c00546) - Applies deep evidential regression to property prediction, giving single-pass calibrated uncertainties used to guide discovery (Soleimany et al., 2021, ACS Central Science). [[code](https://github.com/aamini/chemprop)]
* [Quality of uncertainty estimates from neural network potential ensembles](https://doi.org/10.1103/PhysRevE.105.015311) - Shows ensemble spread of NN potentials can severely underestimate true errors, especially for out-of-sample configurations (Kahle et al., 2022, Physical Review E).
* [Single-model uncertainty quantification in neural network potentials does not consistently outperform model ensembles](https://doi.org/10.1038/s41524-023-01180-8) - Compares evidential, MVE and GMM single-model UQ against ensembles for NN potentials, finding ensembles remain the most robust, especially out of domain (Tan et al., 2023, npj Computational Materials).
* [Materials property prediction with uncertainty quantification: A benchmark study](https://doi.org/10.1063/5.0133528) - Benchmarks ensemble, MC dropout, evidential and other UQ methods for GNN materials property prediction, including under OOD settings (Varivoda et al., 2023, Applied Physics Reviews).
* [Uncertainty quantification and propagation in atomistic machine learning](https://doi.org/10.1515/revce-2024-0028) - Reviews UQ methods (ensembles, Bayesian, evidential, distance-based, conformal) and uncertainty propagation in atomistic ML (Dai et al., 2024, Reviews in Chemical Engineering).
* [Uncertainty quantification in graph neural networks with shallow ensembles](https://doi.org/10.1088/2632-2153/ae0bf0) - Evaluates shallow (last-layer) ensembles as a cheap alternative to deep ensembles for GNN uncertainty in atomistic modeling (Vinchurkar et al., 2025, Machine Learning: Science and Technology).

## Small-Data Learning

### Active learning

* [Accelerated search for materials with targeted properties by adaptive design](https://doi.org/10.1038/ncomms11241) - Uses surrogate models with uncertainty-based selection to find NiTi-based shape-memory alloys with low hysteresis from a small initial dataset (Xue et al., 2016, Nature Communications).
* [Active learning for accelerated design of layered materials](https://doi.org/10.1038/s41524-018-0129-0) - Uses Gaussian-process-based Bayesian optimization to find layered heterostructures with target band gaps using few DFT calculations (Bassman Oftelie et al., 2018, npj Computational Materials).
* [Active learning in materials science with emphasis on adaptive sampling using uncertainties for targeted design](https://doi.org/10.1038/s41524-019-0153-8) - Reviews active learning and Bayesian optimization with uncertainty-driven sampling for materials design under limited data (Lookman et al., 2019, npj Computational Materials).
* [Benchmarking the acceleration of materials discovery by sequential learning](https://doi.org/10.1039/C9SC05999G) - Benchmarks sequential learning strategies on experimental catalyst datasets and defines acceleration and enhancement metrics (Rohr et al., 2020, Chemical Science).
* [Bayesian Optimization for Materials Design with Mixed Quantitative and Qualitative Variables](https://doi.org/10.1038/s41598-020-60652-9) - Proposes latent-variable Gaussian process BO to handle mixed categorical and continuous materials design variables (Zhang et al., 2020, Scientific Reports).
* [Materials design with target-oriented Bayesian optimization](https://doi.org/10.1038/s41524-025-01704-4) - Introduces a target-oriented expected improvement acquisition for finding materials with a specific property value in few experiments (Tian et al., 2025, npj Computational Materials).

### Bayesian optimization: tabular foundation models

* [Out-of-the-Box Tabular Foundation Models for Bayesian Optimization in Materials Discovery](https://arxiv.org/abs/2611.12491) - Evaluates TabPFN and TabICL as out-of-the-box surrogates for Bayesian optimization on materials benchmarks against GPs, random forests and CatBoost (Flöge et al., 2026, NeurIPS 2026 AI4Mat workshop). [[code](https://github.com/PriorLabs/matsci-bo-bench)]

### Benchmark

* [Benchmarking AutoML for regression tasks on small tabular data in materials design](https://doi.org/10.1038/s41598-022-23327-1) - Benchmarks AutoML frameworks on small tabular materials-design regression datasets (Conrad et al., 2022, Scientific Reports).

### Data augmentation

* [Data-augmentation for graph neural network learning of the relaxed energies of unrelaxed structures](https://doi.org/10.1038/s41524-022-00891-8) - Augments training data with perturbed structures labeled with relaxed energies so GNNs predict relaxed energies from unrelaxed inputs (Gibson et al., 2022, npj Computational Materials).
* [Data-augmented crystal graph convolutional neural network for uncertainty-aware thermodynamic stability prediction](https://doi.org/10.1016/j.matdes.2026.117155) - Combines data augmentation with uncertainty-aware CGCNN for thermodynamic stability prediction (Qureshi et al., 2026, Materials & Design).

### Delta-learning

* [Big Data Meets Quantum Chemistry Approximations: The Delta-Machine Learning Approach](https://doi.org/10.1021/acs.jctc.5b00099) - Introduces Delta-learning, modeling the difference between a cheap baseline and a high-level method to reach high accuracy with little data (Ramakrishnan et al., 2015, Journal of Chemical Theory and Computation).

### Descriptors

* [A general-purpose machine learning framework for predicting properties of inorganic materials](https://doi.org/10.1038/npjcompumats.2016.28) - Introduces Magpie composition features with partitioned random forests, showing accurate predictions from modest datasets including experimental band gaps (Ward et al., 2016, npj Computational Materials).

### Fine-tuning foundation models

* [Data-efficient fine-tuning of foundational models for first-principles quality sublimation enthalpies](https://doi.org/10.1039/D4FD00107A) - Fine-tunes a MACE foundation model with tens of reference structures to predict molecular-crystal sublimation enthalpies at first-principles quality (Kaur et al., 2025, Faraday Discussions).
* [Fine-tuning foundation models of materials interatomic potentials with frozen transfer learning](https://doi.org/10.1038/s41524-025-01727-x) - Shows freezing early layers of MACE-MP foundation models during fine-tuning gives data-efficient, accurate system-specific potentials (Radova et al., 2025, npj Computational Materials).

### Low-dimensional crystal-graph descriptor

* [Accurate property prediction with interpretable machine learning model for small datasets via transformed atom vector](https://doi.org/10.1103/physrevmaterials.6.123803) - The transformed atom vector, a low-dimensional interpretable crystal-graph descriptor, predicts HSE band gaps of 2D materials from only 500 samples and supports a property-oriented element-substitution search (Chen et al., 2022, Physical Review Materials).

### Meta-learning

* [Advancing Extrapolative Predictions of Material Properties through Learning to Learn](https://arxiv.org/abs/2404.08657) - Uses meta-learning (learning to learn) to improve extrapolative prediction of material properties (Noda et al., 2024, arXiv).

### Multi-fidelity

* [Multi-fidelity machine learning models for accurate bandgap predictions of solids](https://doi.org/10.1016/j.commatsci.2016.12.004) - Uses co-kriging to combine low-fidelity PBE and high-fidelity HSE band gaps for accurate predictions with fewer expensive calculations (Pilania et al., 2017, Computational Materials Science).
* [Learning properties of ordered and disordered materials from multi-fidelity data](https://doi.org/10.1038/s43588-020-00002-x) - Multi-fidelity MEGNet jointly learns band gaps from PBE, GLLB-SC, HSE, SCAN and experimental data, reducing high-fidelity errors (Chen et al., 2021, Nature Computational Science). [[code](https://github.com/materialsvirtuallab/megnet)]
* [A simple denoising approach to exploit multi-fidelity data for machine learning materials properties](https://doi.org/10.1038/s41524-022-00925-1) - Treats low-fidelity data as noisy high-fidelity labels and denoises them to improve band-gap prediction with scarce high-fidelity data (Liu et al., 2022, npj Computational Materials).
* [Learning from multiple quantum chemical methods: Delta-learning, transfer learning, co-kriging, and beyond](https://doi.org/10.1016/B978-0-323-90049-2.00012-3) - Book chapter reviewing Delta-learning, transfer learning, co-kriging and related multi-fidelity schemes for combining quantum chemical methods (Dral et al., 2023, Quantum Chemistry in the Age of Machine Learning (Elsevier)).
* [Transfer learning with graph neural networks for improved molecular property prediction in the multi-fidelity setting](https://doi.org/10.1038/s41467-024-45566-8) - Shows adaptive-readout GNN transfer from abundant low-fidelity to sparse high-fidelity data gives large gains in drug discovery and quantum mechanics tasks (Buterez et al., 2024, Nature Communications).

### Multi-fidelity screening

* [A multi-fidelity machine learning approach to high throughput materials screening](https://doi.org/10.1038/s41524-022-00947-9) - A multi-output Gaussian process fuses experimental and computational fidelities into a single dynamically evolving design instead of a fixed computational funnel, learning the relationships between methods on the fly and cutting optimization cost by about a factor of three on three materials design problems (Fare et al., 2022, npj Computational Materials).

### Multi-fidelity: adsorption

* [MADField: Multi-fidelity Amortized Density Field for Adsorption in Nanoporous Materials](https://arxiv.org/abs/2606.21284) - Reframes gas adsorption in nanoporous materials as equilibrium density-field estimation learned from two fidelities (GCMC and classical DFT) (Kim et al., 2026, ICML 2026 AI for Science workshop).

### Multitask

* [MT-CGCNN: Integrating Crystal Graph Convolutional Neural Network with Multitask Learning for Material Property Prediction](https://arxiv.org/abs/1811.05660) - Extends CGCNN with multitask learning to jointly predict several crystal properties (Sanyal et al., 2018, arXiv).
* [Materials property prediction for limited datasets enabled by feature selection and joint learning with MODNet](https://doi.org/10.1038/s41524-021-00552-2) - MODNet combines relevance-redundancy feature selection with joint (multi-target) learning, outperforming GNNs on small Matbench datasets (De Breuck et al., 2021, npj Computational Materials). [[code](https://github.com/ppdebreuck/modnet)]
* [Multi-task graph neural networks for simultaneous prediction of global and atomic properties in ferromagnetic systems](https://doi.org/10.1088/2632-2153/ac6a51) - Multi-task GNN jointly predicting global and atomic properties of ferromagnetic alloys (Lupo Pasini et al., 2022, Mach. Learn.: Sci. Technol. 3, 025007).
* [Curvature-informed multi-task learning for graph networks](https://arxiv.org/abs/2208.01684) - Studies curvature-informed multi-task optimization for graph networks predicting materials properties (New et al., 2022, arXiv).
* [MatSciML: A Broad, Multi-Task Benchmark for Solid-State Materials Modeling](https://arxiv.org/abs/2309.05934) - Benchmark for multi-task, multi-dataset learning on solid-state materials (Lee et al., 2023, arXiv).
* [Multi-Task Fine-Tuning Enables Robust Out-of-Distribution Generalization in Atomistic Models](https://arxiv.org/abs/2601.08486) - Shows multi-task fine-tuning of atomistic models improves OOD generalization (Zhang et al., 2026, arXiv).

### Physics-informed

* [A strategy to apply machine learning to small datasets in materials science](https://doi.org/10.1038/s41524-018-0081-z) - Shows that adding crude physical estimates as descriptors substantially improves ML accuracy on small materials datasets (Zhang et al., 2018, npj Computational Materials).
* [Physically Informed Machine Learning Prediction of Electronic Density of States](https://doi.org/10.1021/acs.chemmater.1c04252) - Predicts electronic DOS with a GNN using physically informed encodings, enabling derived properties with improved data efficiency (Fung et al., 2022, Chemistry of Materials).
* [Extrapolative prediction of small-data molecular property using quantum mechanics-assisted machine learning](https://doi.org/10.1038/s41524-023-01194-2) - Uses quantum-mechanical descriptors to improve extrapolative prediction for small-data property tasks (Shimakawa et al., 2024, npj Computational Materials).

### Review

* [Small data machine learning in materials science](https://doi.org/10.1038/s41524-023-01000-z) - Reviews data sources, algorithms and strategies (active, transfer learning, augmentation) for small-data materials ML (Xu et al., 2023, npj Computational Materials).

### Self-supervised benchmark: zeolites

* [ZeoBench: A Benchmark for Self-Supervised Learning on 3D Zeolite Representations](https://arxiv.org/abs/2611.09880) - Presents ZeoBench, a benchmark of self-supervised 3D representation-learning strategies for low-data zeolite property prediction (Sun et al., 2026, NeurIPS 2026 Datasets and Benchmarks Track).

### SSL

* [Crystal twins: self-supervised learning for crystalline material property prediction](https://doi.org/10.1038/s41524-022-00921-5) - Pretrains CGCNN with Barlow Twins/SimSiam objectives on augmented crystals, improving downstream accuracy on small Matbench tasks (Magar et al., 2022, npj Computational Materials). [[code](https://github.com/RishikeshMagar/Crystal-Twins)]
* [Self-supervised learning of materials concepts from crystal structures via deep neural networks](https://doi.org/10.1088/2632-2153/aca23d) - Learns crystal-structure embeddings self-supervised by matching structures with their XRD patterns, capturing materials similarity without labels (Suzuki et al., 2022, Machine Learning: Science and Technology).
* [Pretraining Strategies for Structure Agnostic Material Property Prediction](https://doi.org/10.1021/acs.jcim.3c00919) - Compares self-supervised, fingerprint-supervised and multimodal pretraining for composition-only transformers, improving small-data property prediction (Huang et al., 2024, Journal of Chemical Information and Modeling).

### Synthetic data augmentation

* [MatWheel: Addressing Data Scarcity in Materials Science Through Synthetic Data](https://arxiv.org/abs/2504.09152) - Trains CGCNN on synthetic structures generated by a conditional generative model (Con-CDVAE) and shows benefits in extremely data-scarce settings (Li et al., 2025, ICLR 2025 AI4Mat workshop).

### Training set selection

* [Minimizing data requirements for chemical and material property prediction via cluster-based training set selection](https://doi.org/10.1038/s43588-026-01076-9) - Across 100 space-filling and active-learning algorithms on 60 property prediction tasks, cluster-based training set selection consistently outperforms active learning; a Gaussian-process-variance argument shows it is optimal in the low-data limit, and being label-independent it can build one dataset for several properties in parallel (Gallagher et al., 2026, Nature Computational Science).

### Transfer

* [Enhancing materials property prediction by leveraging computational and experimental data using deep transfer learning](https://doi.org/10.1038/s41467-019-13297-w) - Pretrains ElemNet on large DFT data (OQMD) and fine-tunes on small experimental formation enthalpies, achieving errors comparable to DFT-experiment discrepancy (Jha et al., 2019, Nature Communications). [[code](https://github.com/NU-CUCIS/ElemNet)]
* [Predicting Materials Properties with Little Data Using Shotgun Transfer Learning](https://doi.org/10.1021/acscentsci.9b00804) - Introduces XenonPy.MDL, a library of many pretrained models, and shows shotgun transfer from them improves predictions with very small datasets (Yamada et al., 2019, ACS Central Science). [[code](https://github.com/yoshida-lab/XenonPy)]
* [Predicting materials properties without crystal structure: deep representation learning from stoichiometry](https://doi.org/10.1038/s41467-020-19964-7) - Roost learns composition representations and demonstrates transfer from OQMD to experimental band gaps, plus ensemble-based uncertainty (Goodall et al., 2020, Nature Communications). [[code](https://github.com/CompRhys/roost)]
* [AtomSets as a hierarchical transfer learning framework for small and large materials datasets](https://doi.org/10.1038/s41524-021-00639-w) - Uses pretrained MEGNet features with set-based models to achieve good accuracy on datasets ranging from hundreds to hundreds of thousands of samples (Chen et al., 2021, npj Computational Materials). [[code](https://github.com/materialsvirtuallab/maml)]
* [Cross-property deep transfer learning framework for enhanced predictive analytics on small materials data](https://doi.org/10.1038/s41467-021-26921-5) - Shows models pretrained on one large property dataset transfer to improve prediction of different properties on small datasets (Gupta et al., 2021, Nature Communications). [[code](https://github.com/NU-CUCIS/CrossPropertyTL)]
* [Transfer learning for materials informatics using crystal graph convolutional neural network](https://doi.org/10.1016/j.commatsci.2021.110314) - Evaluates fine-tuning and feature-extraction transfer of CGCNN pretrained on large DFT data to small property datasets (Lee et al., 2021, Computational Materials Science).
* [Towards overcoming data scarcity in materials science: unifying models and datasets with a mixture of experts framework](https://doi.org/10.1038/s41524-022-00929-x) - Combines multiple pretrained source models via a mixture-of-experts gating to outperform pairwise transfer learning on data-scarce tasks (Chang et al., 2022, npj Computational Materials).
* [Transfer learning on large datasets for the accurate prediction of material properties](https://doi.org/10.1039/D3DD00030C) - Pretrains crystal-graph attention networks on millions of PBE calculations and fine-tunes to higher-fidelity (PBEsol, SCAN) data, reducing data needs (Hoffmann et al., 2023, Digital Discovery).
* [Structure-aware graph neural network based deep transfer learning framework for enhanced predictive analytics on diverse materials datasets](https://doi.org/10.1038/s41524-023-01185-3) - Extends cross-property transfer learning to structure-based GNNs (ALIGNN), improving accuracy on many small materials datasets (Gupta et al., 2024, npj Computational Materials).

## Benchmarks and Leaderboards

### Generalization evaluation

* [A critical examination of robustness and generalizability of machine learning prediction of materials properties](https://doi.org/10.1038/s41524-023-01012-9) - Finds ML models trained on Materials Project 2018 degrade on newer 2021 data, highlighting distribution-shift issues (Li et al., 2023, npj Computational Materials).

### GNN benchmark

* [Benchmarking graph neural networks for materials chemistry](https://doi.org/10.1038/s41524-021-00554-0) - MatDeepLearn benchmarks several GNNs (CGCNN, MEGNet, SchNet, MPNN, GCN) on bulk, surface, 2D and cluster datasets under a common framework (Fung et al., 2021, npj Computational Materials). [[code](https://github.com/vxfung/MatDeepLearn)]

### Interatomic-potential benchmarks: defect migration

* [Migration as a Probe: A Generalizable Benchmark Framework for Specialist vs. Generalist Machine-Learned Force Fields](https://arxiv.org/abs/2509.00090) - Benchmarks specialist, fine-tuned and foundation MLFFs using defect-migration NEB pathways in Cr-doped Sb2Te3 as interpolation and extrapolation probes (Cao et al., 2025, NeurIPS 2025 AI4Mat workshop).

### Ionic conductivity: migration-barrier dataset and GNN/uMLIP benchmark

* [Benchmarking machine learning models for predicting lithium ion migration](https://doi.org/10.1038/s41524-025-01571-z) - The LiTraj dataset (13,000 percolation barriers, 122,000 empirical-force-field migration barriers and 1,700 DFT migration trajectories) shows that structure-to-barrier GNNs can separate fast from poor Li conductors and that fine-tuned uMLIPs reach near-DFT accuracy on NEB migration barriers (Dembitskiy et al., 2025, npj Computational Materials). [[code](https://github.com/AIRI-Institute/LiTraj)]

### Ionic conductivity: uMLIP benchmark for barriers and diffusivity

* [Benchmarking Universal Machine Learning Interatomic Potentials for Alkali-Ion Battery Kinetics](https://doi.org/10.1021/acsmaterialslett.6c00134) - Benchmarks M3GNet, CHGNet, MatterSim, MACE, SevenNet, GRACE and Orb against DFT on cathodes and solid electrolytes: Orb-v3 gives the best static migration barriers (MAE about 75 to 111 meV), GRACE-OMat24 best reproduces MD diffusivities, and high-temperature non-equilibrium training data matter more for kinetic accuracy than architecture (Guo et al., 2026, ACS Materials Letters).

### Ionic conductivity: uMLIP-MD vs AIMD against experiment

* [A Comparative Study of Molecular Dynamics Approaches for Simulating Ionic Conductivity in Solid Lithium Electrolytes](https://arxiv.org/abs/2603.28012) - Benchmarks MD-computed ionic conductivity for 21 Li solid electrolytes with experimental reference values and finds a MACE foundation model comparable to DFT-driven MD in accuracy while running more than 350 times faster on one GPU than DFT on a 64-CPU node (Shaaban Kabakibo et al., 2026, arXiv).

### LLM benchmark

* [MaScQA: investigating materials science knowledge of large language models](https://doi.org/10.1039/d3dd00188a) - 650 materials-science exam questions to evaluate LLM knowledge and reasoning (Zaki et al., 2024, Digital Discovery). [[code](https://github.com/M3RG-IITD/MaScQA)]
* [LLM4Mat-bench: benchmarking large language models for materials property prediction](https://doi.org/10.1088/2632-2153/add3bb) - Largest LLM property benchmark: ~1.9M crystals from 10 sources and 45 properties with composition, CIF and text inputs (Niyongabo Rubungo et al., 2025, Machine Learning: Science and Technology). [[code](https://github.com/vertaix/LLM4Mat-Bench)]

### MLIP benchmark

* [MLIP Arena: Advancing Fairness and Transparency in Machine Learning Interatomic Potentials via an Open, Accessible Benchmark Platform](https://doi.org/10.52202/085713-4410) - Open benchmark platform evaluating MLIPs on physical-consistency tasks (diatomics, EOS, MD stability, phonons, NEB, elasticity) beyond DFT-error metrics (Chiang et al., 2025, Advances in Neural Information Processing Systems 38). [[code](https://github.com/atomind-ai/mlip-arena)]
* [Systematic softening in universal machine learning interatomic potentials](https://doi.org/10.1038/s41524-024-01500-6) - Shows universal MLIPs systematically underestimate PES curvature (surface energies, phonons, defects) and that fine-tuning corrects it (Deng et al., 2025, npj Computational Materials).

### Model evaluation

* [Is Domain Knowledge Necessary for Machine Learning Materials Properties?](https://doi.org/10.26434/chemrxiv.11879193.v1) - Compares domain-knowledge featurization with learned representations for composition-based property prediction (Murdock et al., 2020, ChemRxiv (later IMMI)).
* [Examining graph neural networks for crystal structures: Limitations and opportunities for capturing periodicity](https://doi.org/10.1126/sciadv.adi3245) - Analyzes GNN failure to capture periodicity and shows hybrid descriptor-GNN models improve Matbench-type tasks (Gong et al., 2023, Science Advances).

### Multi-method leaderboard

* [JARVIS-Leaderboard: a large scale benchmark of materials design methods](https://doi.org/10.1038/s41524-024-01259-w) - Community leaderboard spanning AI, electronic structure, force fields, quantum computation and experiments (274 benchmarks and 1281 contributions at publication) (Choudhary et al., 2024, npj Computational Materials). [[code](https://github.com/usnistgov/jarvis_leaderboard)]

### NLP benchmark

* [MatSci-NLP: Evaluating Scientific Language Models on Materials Science Language Tasks Using Text-to-Schema Modeling](https://doi.org/10.18653/v1/2023.acl-long.201) - MatSci-NLP: benchmark of 7 materials-science NLP tasks for evaluating language models (Song et al., 2023, ACL 2023). [[code](https://github.com/BangLab-UdeM-Mila/NLP4MatSci-ACL23)]

### OOD benchmark

* [Structure-based out-of-distribution (OOD) materials property prediction: a benchmark study](https://doi.org/10.1038/s41524-024-01316-4) - Benchmarks GNN property models on OOD splits of Matbench-derived tasks, finding marked degradation versus random splits (Omee et al., 2024, npj Computational Materials).

### Phonon benchmark

* [Universal machine learning interatomic potentials are ready for phonons](https://doi.org/10.1038/s41524-025-01650-1) - Benchmarks universal MLIPs on harmonic phonons of ~10k materials from the MDR phonon database (Loew et al., 2025, npj Computational Materials).

### Property-prediction benchmark

* [Benchmarking materials property prediction methods: the Matbench test set and Automatminer reference algorithm](https://doi.org/10.1038/s41524-020-00406-3) - Matbench v0.1: 13 supervised tasks (312 to 132k samples; composition and structure inputs) with nested CV, plus the Automatminer baseline (Dunn et al., 2020, npj Computational Materials). [[code](https://github.com/materialsproject/matbench)]

### Stability evaluation

* [A critical examination of compound stability predictions from machine-learned formation energies](https://doi.org/10.1038/s41524-020-00362-y) - Shows low formation-energy MAE does not imply accurate stability (decomposition energy) prediction for compositional ML models (Bartel et al., 2020, npj Computational Materials). [[code](https://github.com/CJBartel/TestStabilityML)]

### Stability/discovery benchmark

* [A framework to evaluate machine learning crystal stability predictions](https://doi.org/10.1038/s42256-025-01055-1) - Matbench Discovery: prospective benchmark on ~257k WBM structures evaluating stability classification (F1, DAF), energy regression, and kappa_SRME thermal conductivity (Riebesell et al., 2025, Nature Machine Intelligence). [[code](https://github.com/janosh/matbench-discovery)]

### Thermal conductivity: kappa SRME benchmark for foundation MLIPs

* [Thermal conductivity predictions with foundation atomistic models](https://doi.org/10.1038/s41467-026-76391-w) - Defines the symmetric relative (mean) errors SRE/SRME on per-phonon Wigner conductivity contributions and Grueneisen parameters for 103 phononDB-PBE solids, benchmarks M3GNet, CHGNet, MACE-MP-0, SevenNet and ORB, and shows fine-tuning MACE on three DFT frames brings LiBr kappa within 2% of DFT (Póta et al., 2026, Nature Communications).

### Thermal conductivity: surrogate kappa_L regressor benchmark

* [Fast and accurate prediction of lattice thermal conductivity via machine learning surrogates](https://doi.org/10.1039/d6dd00278a) - Benchmarks 15 kappa_L surrogates (physics descriptors plus ML, end-to-end GNNs, and pretrained-MLIP embeddings plus ML) on 6,966 Phonix entries under random, space-group-disjoint and out-of-distribution splits, finding MLIP-embedding models best for interpolation and the ALiEGNN network most robust out of distribution (Wang et al., 2026, Digital Discovery).

### Thermal conductivity: uMLIP force-constant and kappa_L benchmark

* [A Comprehensive Assessment and Benchmark Study of Large Atomistic Foundation Models for Phonons](https://doi.org/10.1002/aidi.202500075) - Benchmarks EquiformerV2, MatterSim, MACE and CHGNet on second/third-order force constants and kappa_L for 2,429 OQMD crystals, finding fine-tuned EquiformerV2 (OMat24) best while MACE and CHGNet give poor kappa_L despite similar force errors, so force accuracy alone does not predict kappa_L accuracy (Anam et al., 2025, Advanced Intelligent Discovery).

### Uncertainty: calibration under shift and active learning

* [When active learning fails, uncalibrated out of distribution uncertainty quantification might be the problem](https://doi.org/10.1038/s41524-026-02368-4) - Compares ALIGNN deep ensembles, loss-landscape uncertainties and XGBoost/random-forest/NN ensembles on bandgap, formation energy and solubility, finding that recalibration fitted in-domain generalizes inconsistently out of domain and that calibrated uncertainties generally fail to beat random sampling or uncalibrated uncertainties in OOD active learning (Dale et al., 2026, npj Computational Materials).

## Language Models for Property Prediction

### CIF language models

* [Crystal structure generation with autoregressive large language modeling](https://doi.org/10.1038/s41467-024-54639-7) - CrystaLLM: GPT-style model trained on millions of CIFs that generates plausible crystal structures (Antunes et al., 2024, Nature Communications). [[code](https://github.com/lantunes/CrystaLLM)]
* [Fine-Tuned Language Models Generate Stable Inorganic Materials as Text](https://arxiv.org/abs/2402.04379) - Fine-tunes LLaMA-2 on text-encoded crystals; ~49% of sampled structures predicted metastable (Gruver et al., 2024, ICLR 2024). [[code](https://github.com/facebookresearch/crystal-text-llm)]

### Domain language model

* [MatSciBERT: A materials domain language model for text mining and information extraction](https://doi.org/10.1038/s41524-022-00784-w) - BERT pretrained on materials-science literature, improving NER, relation and abstract classification tasks (Gupta et al., 2022, npj Computational Materials). [[code](https://github.com/M3RG-IITD/MatSciBERT)]
* [Quantifying the advantage of domain-specific pre-training on named entity recognition tasks in materials science](https://doi.org/10.1016/j.patter.2022.100488) - Introduces MatBERT and quantifies gains of domain pretraining for materials NER (Trewartha et al., 2022, Patterns). [[code](https://github.com/lbnlp/MatBERT)]

### Domain LLM

* [DARWIN Series: Domain Specific Large Language Models for Natural Science](https://arxiv.org/abs/2308.13565) - DARWIN is a series of open-source LLMs for physics, chemistry and materials science fine-tuned on over 60,000 instruction data points generated automatically from scientific texts (Xie et al., 2023, arXiv).
* [Foundational Large Language Models for Materials Research](https://arxiv.org/abs/2412.09560) - LLaMat, LLaMA continually pretrained on materials literature and crystallographic data, excels at materials NLP and information extraction, and its LLaMat-CIF variant generates stable crystals (Mishra et al., 2024, arXiv).
* [DARWIN 1.5: Large Language Models as Materials Science Adapted Learners](https://arxiv.org/abs/2412.11970) - DARWIN 1.5, trained on 6M materials papers and 21 experimental datasets covering 49,256 materials, predicts properties from natural language with up to 59.1% accuracy improvement over base LLaMA-7B and outperforms SOTA ML baselines on several tasks (Xie et al., 2024, arXiv).

### Embeddings

* [A Sober Look at LLMs for Material Discovery: Are They Actually Good for Bayesian Optimization Over Molecules?](https://arxiv.org/abs/2402.05015) - Using LLMs as fixed feature extractors and with parameter-efficient finetuning for Bayesian-optimization surrogates on real chemistry problems, the study tests whether LLMs genuinely help principled BO over molecules (Kristiadi et al., 2024, arXiv (ICML 2024)).
* [Multimodal language and graph learning of adsorption configuration in catalysis](https://doi.org/10.1038/s42256-024-00930-7) - Graph-assisted self-supervised pretraining aligning a language model with GNN embeddings reduces adsorption-energy MAE by about 10% and transfers across fine-tuning datasets (Ock et al., 2024, Nature Machine Intelligence).

### Evaluation

* [Assessment of fine-tuned large language models for real-world chemistry and material science applications](https://doi.org/10.1039/D4SC04401K) - A multi-group benchmark of fine-tuned open-source LLMs on diverse real-world chemistry and materials tasks found fine-tuning superior to traditional ML in most cases (Herck et al., 2025, Chemical Science).

### Fine-tuning

* [Accurate, interpretable predictions of materials properties within transformer language models](https://doi.org/10.1016/j.patter.2023.100803) - Text descriptions (composition, symmetry, site geometry) fed to a literature-pretrained transformer outperformed crystal graph networks on four of five classification properties when all reference data were used (Korolev et al., 2023, Patterns).
* [Catalyst Energy Prediction with CatBERTa: Unveiling Feature Exploration Strategies through Large Language Models](https://doi.org/10.1021/acscatal.3c04956) - CatBERTa, a pretrained transformer encoder on human-readable text of initial adsorbate-catalyst structures, predicts adsorption energy with precision comparable to conventional GNNs (Ock et al., 2023, ACS Catalysis).
* [AlloyBERT: Alloy property prediction with large language models](https://doi.org/10.1016/j.commatsci.2024.113256) - AlloyBERT, a RoBERTa-based model on textual alloy composition and processing descriptions, reached MSE 0.00015 (MPEA) and 0.00611 (RAYS), beating the best shallow models (0.00025 and 0.0076) (Chaudhari et al., 2024, Computational Materials Science).
* [AtomGPT: Atomistic Generative Pretrained Transformer for Forward and Inverse Materials Design](https://doi.org/10.1021/acs.jpclett.4c01126) - AtomGPT predicts formation energies, band gaps and superconducting Tc from chemical and structural text with accuracy comparable to GNNs, and also generates structures (Choudhary et al., 2024, The Journal of Physical Chemistry Letters).
* [Large Language Models for Inorganic Synthesis Predictions](https://doi.org/10.1021/jacs.4c05840) - Fine-tuned LLMs predicted inorganic synthesizability and precursor selection comparably to, and sometimes better than, bespoke ML models (Kim et al., 2024, Journal of the American Chemical Society).

### In-context learning

* [14 examples of how LLMs can transform materials science and chemistry: a reflection on a large language model hackathon](https://doi.org/10.1039/D3DD00113J) - Reports 14 hackathon projects exploring diverse LLM applications in molecular and materials science, including predictive modelling (Jablonka et al., 2023, Digital Discovery).
* [Bayesian Optimization of Catalysis With In-Context Learning](https://arxiv.org/abs/2304.05341) - Frozen LLMs perform regression with uncertainty via in-context learning, enabling Bayesian optimization over natural-language catalyst procedures that matches or outperforms Gaussian processes on solubility and OCM benchmarks (Ramos et al., 2023, arXiv).

### LLM applications and agents

* [Reflections from the 2024 Large Language Model (LLM) Hackathon for Applications in Materials Science and Chemistry](https://arxiv.org/abs/2411.15221) - Summarizes 34 hackathon projects using LLMs/agents for property prediction, molecular/materials design and automation (Zimmermann et al., 2024, arXiv).

### LLM evaluation

* [Probing the limitations of multimodal language models for chemistry and materials research](https://doi.org/10.1038/s43588-025-00836-3) - MaCBench evaluates vision-language models on materials and chemistry data extraction, experiments and interpretation tasks (Alampara et al., 2025, Nature Computational Science).

### LLM fine-tuning for property prediction

* [Leveraging large language models for predictive chemistry](https://doi.org/10.1038/s42256-023-00788-1) - Fine-tuned GPT-3 on text-formatted questions matches or beats conventional ML for low-data chemistry/materials property tasks (Jablonka et al., 2024, Nature Machine Intelligence). [[code](https://github.com/kjappelbaum/gptchem)]
* [Large language models for material property predictions: elastic constant tensor prediction and materials design](https://doi.org/10.1039/d5dd00061k) - ElaTBot fine-tuned LLM predicts full elastic constant tensors and supports agent-style materials design (Liu et al., 2025, Digital Discovery).

### LLM-GNN hybrid

* [Hybrid-LLM-GNN: integrating large language models and graph neural networks for enhanced materials property prediction](https://doi.org/10.1039/d4dd00199k) - Concatenates LLM text embeddings with GNN embeddings, improving accuracy across JARVIS/Materials Project property tasks (Li et al., 2025, Digital Discovery).

### Multimodal text+graph

* [CrysMMNet: Multimodal Representation for Crystal Property Prediction](https://arxiv.org/abs/2307.05390) - Fuses graph and Robocrystallographer text representations to improve crystal property prediction (Das et al., 2023, UAI 2023 / arXiv).

### Multimodal/agents

* [Augmenting large language models with chemistry tools](https://doi.org/10.1038/s42256-024-00832-8) - ChemCrow augments GPT-4 with 18 expert tools to autonomously perform synthesis, drug discovery and materials design tasks (Bran et al., 2024, Nature Machine Intelligence).
* [ChatMOF: an artificial intelligence system for predicting and generating metal-organic frameworks using large language models](https://doi.org/10.1038/s41467-024-48998-4) - ChatMOF, a GPT-4-based agent with a toolkit and evaluator, achieves 96.9% accuracy for searching, 95.7% for property prediction and 87.5% for generating MOFs (Kang et al., 2024, Nature Communications).
* [LLaMP: Large Language Model Made Powerful for High-fidelity Materials Knowledge Retrieval](https://doi.org/10.18653/v1/2025.emnlp-main.1280) - LLaMP is a retrieval-augmented hierarchical ReAct agent framework that queries Materials Project data and runs atomistic simulations without fine-tuning, and is shown to mitigate intrinsic LLM bias (Chiang et al., 2025, Proceedings of the 2025 Conference on Empirical Methods in Natural Language Processing).
* [MatterChat: A Multi-Modal LLM for Material Science](https://arxiv.org/abs/2502.13107) - MatterChat aligns a pretrained interatomic potential with a pretrained LLM via a bridging module, improving inorganic property prediction over general-purpose LLMs such as GPT-4 (Tang et al., 2025, arXiv).

### Structure-token transformer pretraining

* [Unified Material Transformer as Scalable Material Property Predictor](https://openreview.net/forum?id=hPbJbp6x1l) - A transformer with a structure tokenizer and 3D positional encoding, pretrained with BERT- and GPT-style objectives, matches or exceeds several specialized models with one architecture; its element embeddings follow known chemical trends (Anonymous et al., 2024, OpenReview (THU 2024 Winter AML submission)).

### Text representations

* [Robocrystallographer: automated crystal structure text descriptions and analysis](https://doi.org/10.1557/mrc.2019.94) - Generates human-readable text descriptions of crystal structures, later used as LLM inputs for property prediction (Ganose et al., 2019, MRS Communications). [[code](https://github.com/hackingmaterials/robocrystallographer)]
* [Less can be more for predicting properties with large language models](https://doi.org/10.1038/s43588-026-01045-2) - MatText study of text representations of materials, showing LLMs underuse geometric information for property prediction (Alampara et al., 2026, Nature Computational Science). [[code](https://github.com/lamalab-org/MatText)]

### Text-based property regression

* [LLM-Prop: predicting the properties of crystalline materials using large language models](https://doi.org/10.1038/s41524-025-01536-2) - Fine-tunes a T5 encoder on Robocrystallographer text descriptions, outperforming GNNs on band gap and volume prediction (TextEdge dataset) (Niyongabo Rubungo et al., 2025, npj Computational Materials). [[code](https://github.com/vertaix/LLM-Prop)]

## Applications of Property Models

### Autonomous laboratories

* [An autonomous laboratory for the accelerated synthesis of inorganic materials](https://doi.org/10.1038/s41586-023-06734-w) - The A-Lab combines computed stability data, machine learning, and robotics to plan and run solid-state syntheses of inorganic targets autonomously (Szymanski et al., 2023, Nature).

### Crystal structure prediction

* [Accelerating crystal structure prediction by machine-learning interatomic potentials with active learning](https://doi.org/10.1103/PhysRevB.99.064114) - Moment-tensor machine-learning potentials trained by active learning replace most DFT calculations in evolutionary crystal structure prediction (Podryabinkin et al., 2019, Physical Review B).

### Property-guided generation

* [Accelerating inverse materials design using generative diffusion models with reinforcement learning](https://arxiv.org/abs/2511.03112) - MatInvent optimizes crystal diffusion models with reinforcement learning, using property predictors as rewards, and reaches target property values within about 60 iterations (about 1,000 property evaluations) (Chen et al., 2025, arXiv).
* [A generative model for inorganic materials design](https://doi.org/10.1038/s41586-025-08628-5) - MatterGen is a diffusion model for inorganic crystals that can be steered toward target chemistry, symmetry, and property constraints (Zeni et al., 2025, Nature). [[code](https://github.com/microsoft/mattergen)]

### Screening: electrical conductivity

* [High-throughput study of electrical conductivity in ordered metals](https://doi.org/10.1038/s41524-026-02370-w) - ML combined with high-throughput ab initio calculations screens over 2.8 million compounds for metallic transport; full electron-phonon calculations on the top candidates agree with available experiments and identify conductors such as LiBePt2 approaching the conductivity of aluminium (da Silva et al., 2026, npj Computational Materials).

## Reviews and Perspectives

### Composition-based prediction

* [Machine learning prediction of materials properties from chemical composition: Status and prospects](https://doi.org/10.1063/5.0235541) - Review of ML prediction of materials properties from chemical composition with a focus on physics-guided ML, covering statistical learning, feature reduction, composition representations, prediction of structure and electronic properties, and resource tables of databases, tools and predictors (Alghadeer et al., 2024, Chemical Physics Reviews).

### Crystal structure and property prediction

* [A Comprehensive Review of Machine-Learning Approaches for Crystal Structure/Property Prediction](https://doi.org/10.3390/cryst15110925) - Review of crystal structure prediction and crystal property prediction together, tracing the transition from classical optimization algorithms to supervised and unsupervised ML, with ML modeling of crystal defects and case studies (Sadeghian et al., 2025, Crystals).

### Data infrastructure review

* [Data-Driven Materials Science: Status, Challenges, and Perspectives](https://doi.org/10.1002/advs.201900808) - Reviews data infrastructures, databases and ML in data-driven materials science (Himanen et al., 2019, Advanced Science).

### Deep learning review

* [Recent advances and applications of deep learning methods in materials science](https://doi.org/10.1038/s41524-022-00734-6) - Review of deep learning for atomistic, image, spectral and text data in materials science (Choudhary et al., 2022, npj Computational Materials).

### Dielectric and piezoelectric: ferroelectric MLMD review

* [Polarization Dynamics in Ferroelectrics: Insights Enabled by Machine Learning Molecular Dynamics](https://doi.org/10.1002/advs.76203) - Perspective reviewing ML molecular dynamics for polarization switching, domain nucleation and migration and topological polar textures in ferroelectrics, with open problems in long-range electrostatics, multiferroic spin-lattice coupling and data-efficient pretraining of large atomistic models (Bai et al., 2026, Advanced Science).

### Foundation models

* [Foundation models for materials discovery – current state and future directions](https://doi.org/10.1038/s41524-025-01538-0) - Perspective on foundation models, including LLMs, for materials discovery, covering property prediction, synthesis planning and molecular generation, and how new data capture methods and modalities will shape the field (Pyzer-Knapp et al., 2025, npj Computational Materials).

### Foundation models and LLM agents

* [A Survey of AI for Materials Science: Foundation Models, LLM Agents, Datasets, and Tools](https://doi.org/10.1145/3822503) - Survey of foundation models, LLM agents, datasets and tools for materials science including property prediction (Van et al., 2026, ACM Computing Surveys).

### Foundation models review

* [Foundation models for atomistic simulation of chemistry and materials](https://doi.org/10.1038/s41570-025-00793-5) - Review of atomistic foundation models (universal MLIPs, pretraining datasets) and their evaluation (Yuan et al., 2026, Nature Reviews Chemistry).

### General review

* [Machine learning in materials informatics: recent applications and prospects](https://doi.org/10.1038/s41524-017-0056-5) - Early review of fingerprinting and ML for materials property prediction (Ramprasad et al., 2017, npj Computational Materials).
* [Machine learning for molecular and materials science](https://doi.org/10.1038/s41586-018-0337-2) - Landmark Nature review of ML workflows, representations and opportunities for molecules and materials (Butler et al., 2018, Nature).
* [Recent advances and applications of machine learning in solid-state materials science](https://doi.org/10.1038/s41524-019-0221-0) - Comprehensive review of ML for solid-state materials: descriptors, algorithms, stability and property prediction (Schmidt et al., 2019, npj Computational Materials).
* [The Role of Machine Learning in the Understanding and Design of Materials](https://doi.org/10.1021/jacs.0c09105) - Perspective on ML for materials understanding and design, emphasizing data and representations (Moosavi et al., 2020, Journal of the American Chemical Society).
* [Opportunities and Challenges for Machine Learning in Materials Science](https://doi.org/10.1146/annurev-matsci-070218-010015) - Discusses ML opportunities, pitfalls and model assessment in materials science (Morgan et al., 2020, Annual Review of Materials Research).
* [Machine learning in materials science: From explainable predictions to autonomous design](https://doi.org/10.1016/j.commatsci.2021.110360) - Review spanning interpretable property prediction to autonomous materials design (Pilania et al., 2021, Computational Materials Science).

### GNN review

* [Graph neural networks for materials science and chemistry](https://doi.org/10.1038/s43246-022-00315-6) - Review of GNN architectures, datasets and benchmarks for materials and chemistry property prediction (Reiser et al., 2022, Communications Materials).

### Inverse design

* [AI-Driven Inverse Design of Materials: Past, Present, and Future](https://doi.org/10.1088/0256-307x/42/2/027403) - Review of AI-driven inverse materials design, from experiment- and theory-driven discovery and high-throughput electronic-structure methods to recent AI generative and design approaches (Han et al., 2025, Chinese Physics Letters).
* [Machine Learning-Based Methods for Materials Inverse Design: A Review](https://doi.org/10.32604/cmc.2025.060109) - Review of ML-based materials inverse design, analysing exploration-based, model-based and optimization-based methods and their applications to alloys, optical and acoustic materials (Liu et al., 2025, Computers, Materials & Continua).

### Ionic conductivity: review of ML pipelines for solid electrolytes

* [Machine learning pipelines for the design of solid-state electrolytes](https://doi.org/10.1039/d5mh01525a) - Reviews ML pipelines for inorganic solid electrolytes (data, features, classical and deep models, MLIP-accelerated MD, generative design and closed-loop discovery), organized around five discovery challenges, with explicit treatment of the data gap for multivalent (Mg, Ca, Zn, Al) conductors (Jain et al., 2026, Materials Horizons).

### Material classes: alloys

* [Machine learning for alloys](https://doi.org/10.1038/s41578-021-00340-w) - Review of machine-learning-driven alloy research, covering representations, descriptors and interatomic potentials (building on cluster-expansion-style methods) and applications to metallic glasses, high-entropy alloys, superalloys, shape-memory alloys, magnets and catalysts (Hart et al., 2021, Nature Reviews Materials).
* [Machine learning for high-entropy alloys: Progress, challenges and opportunities](https://doi.org/10.1016/j.pmatsci.2022.101018) - Review of ML for high-entropy alloys covering ML interatomic potentials for atomistic simulation of chemically disordered alloys (phase prediction, planar defects, plasticity) and macro-scale models for lattice structure, phase formation and mechanical properties, with uncertainty quantification and inverse design as open directions (Liu et al., 2023, Progress in Materials Science).
* [A Comprehensive Review of the Computational Approaches for Structure–Property Prediction of High Entropy Materials](https://doi.org/10.1007/s44210-026-00084-8) - Review of computational approaches for structure-property prediction of high-entropy materials (Chabri et al., 2026, High Entropy Alloys & Materials).

### Material classes: glasses

* [Machine learning for glass science and engineering: A review](https://doi.org/10.1016/j.nocx.2019.100036) - Review of early progress in using machine learning to replace trial-and-error design of oxide glasses with tailored properties, framed by the Materials Genome Initiative (Liu et al., 2019, Journal of Non-Crystalline Solids: X).
* [Artificial intelligence and machine learning in glass science and technology: 21 challenges for the 21st century](https://doi.org/10.1111/ijag.15881) - Perspective identifying 21 grand challenges in glass science, from glass formation and composition-processing-property relationships to industrial flaw detection, that either enable or are enabled by AI and machine learning (Ravinder et al., 2021, International Journal of Applied Glass Science).

### Material classes: magnetocaloric (review)

* [Application of machine learning in magnetocaloric materials: A review](https://doi.org/10.1016/j.mtcomm.2025.111933) - Review of machine-learning applications in magnetocaloric materials (Mo et al., 2025, Materials Today Communications).

### Material classes: perovskite photovoltaics

* [Machine learning for perovskite solar cells: a comprehensive review on opportunities and challenges for materials scientists](https://doi.org/10.1039/d5el00041f) - Review of recent advances, opportunities and challenges of machine learning for materials scientists working on perovskite solar cells, including prediction of their materials and device properties (de la Asunción-Nadal et al., 2025, EES Solar).

### Material classes: polymers

* [Polymer informatics: Current status and critical next steps](https://doi.org/10.1016/j.mser.2020.100595) - Ramprasad-group review of the polymer informatics ecosystem (surrogate property models, fingerprinting, synthesizability and inverse design), highlighting the scarcity of curated data and of representations that capture processing and synthesis (Chen et al., 2021, Materials Science and Engineering: R: Reports).

### Material classes: surfaces and catalysis

* [Interpretable machine learning for knowledge generation in heterogeneous catalysis](https://doi.org/10.1038/s41929-022-00744-z) - Perspective classifying ML approaches in heterogeneous catalysis by interpretability, noting that most work uses black-box models to predict descriptors such as adsorption and formation energies, and outlining how interpretable ML can support hypothesis formation (Esterhuizen et al., 2022, Nature Catalysis).
* [Machine-learning atomic simulation for heterogeneous catalysis](https://doi.org/10.1038/s41524-022-00959-5) - Review of atomic simulation in heterogeneous catalysis and the shift toward ML potentials combined with global optimization to resolve complex surface structures and reaction networks (Chen et al., 2023, npj Computational Materials).
* [Machine Learning Potentials for Heterogeneous Catalysis](https://doi.org/10.1021/acscatal.4c06717) - Perspective on machine learning potentials for heterogeneous catalysis, which extend ab initio MD beyond a few hundred atoms and tens of picoseconds to simulate interfacial structure, dynamics and reactivity at near-DFT accuracy (Omranpour et al., 2025, ACS Catalysis).

### Mechanical properties of metals

* [Intelligent prediction of mechanical properties in metallic materials based on machine learning: A review & perspective](https://doi.org/10.6052/1000-0992-25-026) - Systematic review and perspective on machine-learning prediction of mechanical properties of metallic materials (Advances in Mechanics 56(1):123-168) (Cao et al., 2026, Advances in Mechanics).

### MLIP review

* [Machine-learned potentials for next-generation matter simulations](https://doi.org/10.1038/s41563-020-0777-6) - Review of machine-learned interatomic potentials and their role in property simulation (Friederich et al., 2021, Nature Materials).
* [A practical guide to machine learning interatomic potentials - Status and future](https://doi.org/10.1016/j.cossms.2025.101214) - Practical guide to MLIPs including universal potentials, datasets and benchmarking (Jacobs et al., 2025, Current Opinion in Solid State and Materials Science).

### Multimodal: review covering multimodal learning (structure, electronic, microscopy, spectroscopy, processing, text)

* [Toward automated discovery with generative models multimodal learning and closed loop workflows in inverse materials design](https://doi.org/10.1016/j.xcrp.2026.103561) - This review of generative crystal models and closed-loop inverse design includes a survey of multimodal representations that combine crystal structure with thermodynamic and electronic data, microscopy, spectroscopy, processing context and text, and proposes a nine-rung discovery-credibility ladder with minimum reporting standards (Babu et al., 2026, Cell Reports Physical Science).

### Multimodal: review of multimodal materials data (composition, microstructure, processing, characterization)

* [Generative and multimodal AI for materials prediction and design: progress, challenges, and perspectives](https://doi.org/10.1088/2515-7639/ae93fd) - This review introduces a property hierarchy from intrinsic to processing-dependent properties and finds that multimodal materials evidence remains concentrated in composition and idealized structure, with microstructure, processing and characterization modalities under-represented and weakly integrated (Liu et al., 2026, Journal of Physics: Materials).

### Optoelectronic materials

* [Machine learning-enabled optoelectronic material discovery: a comprehensive review](https://doi.org/10.20517/jmi.2025.13) - Review of ML combined with high-throughput screening for optoelectronic materials, predicting electronic structure, thermodynamic stability and charge transport, covering workflows, data integration and model frameworks, and challenges in data standardization, interpretability and closed-loop validation (Shu et al., 2025, Journal of Materials Informatics).

### Perspective

* [Machine learning for materials science: Barriers to broader adoption](https://doi.org/10.1016/j.matt.2023.03.028) - Discusses data, validation and cultural barriers to adopting ML in materials science (Boyce et al., 2023, Matter).

### Physics-informed: quantum machine learning

* [Ab Initio Machine Learning in Chemical Compound Space](https://doi.org/10.1021/acs.chemrev.0c01303) - Review of quantum-mechanics-based machine learning (QML) in chemical compound space, combining the efficiency of statistical surrogate models with an ab initio view of matter to reach universality and transferability (Huang et al., 2021, Chemical Reviews).

### Property prediction and synthesis overview

* [Application of Machine Learning in Material Synthesis and Property Prediction](https://doi.org/10.3390/ma16175977) - Review outlining basic ML principles and common algorithms, and surveying their use for property prediction and synthesis guidance in areas such as superconductivity, thermoelectrics, photovoltaics, catalysis and high-entropy alloys (Huang et al., 2023, Materials).

### Property prediction overview

* [Machine learning approaches for the prediction of materials properties](https://doi.org/10.1063/5.0018384) - Tutorial-style overview of the machine-learning workflow for predicting materials properties, written for chemists and materials scientists new to ML, with examples and practical questions for each stage (Chibani et al., 2020, APL Materials).

### Small data

* [Machine learning strategies for small sample size in materials science](https://doi.org/10.1007/s40843-024-3204-5) - Review of machine-learning strategies for small sample sizes in materials science (Tao et al., 2025, Science China Materials).

### Superconductivity: review of ML for superhydrides

* [Unveiling future superconductors through machine learning](https://doi.org/10.1016/j.mtphys.2024.101384) - Minireview of how ML assists each stage of the superhydride discovery cycle (structure search, stability, Tc estimation), with emphasis on ternary and higher hydrides and open challenges (Bai et al., 2024, Materials Today Physics).

### Superconductivity: roadmap

* [The 2021 room-temperature superconductivity roadmap](https://doi.org/10.1088/1361-648x/ac2864) - Community roadmap collecting viewpoints from leading groups on the status of and long-term theoretical and experimental challenges toward ambient-temperature superconductivity; notes that current design is dominated by conventional phonon-mediated superconductors while ambient-temperature superconductivity may require other pairing mechanisms (Boeri et al., 2022, Journal of Physics: Condensed Matter).

### Thermal conductivity: review

* [Machine learning for predicting thermal transport properties of solids](https://doi.org/10.1016/j.mser.2021.100642) - Reviews ML for thermal transport in solids, covering MLIPs for phonon transport in defective, amorphous and high-temperature systems, ML correlations between kappa and other properties for high-throughput screening, and ML-driven structural design for target conductance (Qian et al., 2021, Materials Science and Engineering: R: Reports).
* [Predicting lattice thermal conductivity via machine learning: a mini review](https://doi.org/10.1038/s41524-023-00964-2) - Mini-review of direct ML prediction of kappa_L from descriptors and indirect prediction through MLIP-accelerated MD and first-principles calculations, with perspectives on data and model limitations (Luo et al., 2023, npj Computational Materials).

### Thermal transport

* [Materials Discovery and Properties Prediction in Thermal Transport via Materials Informatics: A Mini Review](https://doi.org/10.1021/acs.nanolett.8b05196) - Mini review of materials informatics for predicting and discovering materials with desired thermal transport properties, including thermal interface and thermoelectric materials (Wan et al., 2019, Nano Letters).

### Thermodynamic stability

* [Accelerating the prediction of stable materials with machine learning](https://doi.org/10.1038/s43588-023-00536-w) - Review of machine-learning methods for accelerating the prediction of thermodynamically stable materials (Griesemer et al., 2023, Nature Computational Science).

### Thermoelectrics: defect engineering

* [AI-Driven Defect Engineering for Advanced Thermoelectric Materials](https://doi.org/10.1002/adma.202505642) - Review of AI and ML for thermoelectric design in a multiscale defect space, covering deep, graph and transformer models with high-throughput simulations, AI-enhanced defect engineering (composition, entropy, dislocation and grain-boundary design) and inverse design (Fu et al., 2025, Advanced Materials).

### Thermoelectrics: review

* [Machine Learning Approaches for Thermoelectric Materials Research](https://doi.org/10.1002/adfm.201906041) - Reviews ML methods used in thermoelectric research, the role each method plays, and strategies for the small databases typical of thermoelectrics (Wang et al., 2019, Advanced Functional Materials).
* [A review of machine learning approaches for the discovery of thermoelectric materials](https://doi.org/10.1080/23746149.2025.2536269) - Reviews ML for thermoelectric discovery from experimental, crystallographic and DFT data, covering property prediction (including ZT), descriptor engineering and structural optimization, with an emphasis on earth-abundant alternatives (Yelgel et al., 2025, Advances in Physics: X).

### Uncertainty: review of uncertainty-driven active learning

* [Active Learning for Interatomic Potentials: A Review of Uncertainty-Driven Data Efficiency](https://arxiv.org/abs/2610.23776) - Reviews more than seventy 2020-2026 active-learning studies for interatomic potentials, from query-by-committee and GP force fields to foundation-model fine-tuning, and concludes that uncertainty estimates are not interchangeable across architectures and are often least reliable where they matter most (Chepkasov et al., 2026, arXiv).

## Property Datasets

Datasets for each commonly predicted property, with sample counts and download links. Counts marked `~` are approximate (paper or secondary source); unmarked counts were read from the official page or counted from the released file (JARVIS: non-null values in the 2022.12.12 `dft_3d`/`dft_2d` releases, counted 2026-11-08). MateriaViva counts are numbers of structures with that property. Machine-readable copy: [`data/property_datasets.csv`](data/property_datasets.csv).

### Energetics and stability

| Property | Unit | Dataset | Collection | Samples | Input | Fidelity |
| --- | --- | --- | --- | ---: | --- | --- |
| Band gap & heat of formation (perovskites) | eV | [castelli_perovskites](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 18,928 | structure | DFT-GLLBSC/RPBE |
| Decomposition energy / stability | eV/atom | [GNoME stable materials](https://github.com/google-deepmind/materials_discovery) | GNoME | ~381,000 | structure | DFT-PBE |
| Energy above hull | eV/atom | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 7,259,115 | structure | mixed (per-method) |
| Energy above hull | eV/atom | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 75,993 | structure | DFT-OptB88vdW |
| Energy of nitride polymorphs | eV/atom | [tholander_nitrides](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 12,815 | structure | DFT |
| Energy, forces (aggregated MLIP data) | various | [ColabFit (HF org)](https://huggingface.co/colabfit) | ColabFit | ? | structure | various DFT |
| Energy, forces, stress | eV; eV/A; GPa | [OMat24](https://huggingface.co/datasets/facebook/OMAT24) | OMat24 | ~110,000,000 | structure | DFT-PBE/PBE+U |
| Energy, forces, stress | eV; eV/A; GPa | [MatPES](https://matpes.ai) | MatPES | ~400,000 | structure | DFT-PBE and r2SCAN |
| Energy, forces, stress, magmom | eV; eV/A; GPa | [MPtrj](https://figshare.com/articles/dataset/23713842) | MPtrj | ~1,580,395 | structure | DFT-PBE/PBE+U |
| Energy, formation energy | eV/atom | [LeMat-Bulk](https://huggingface.co/datasets/LeMaterial/LeMat-Bulk) | LeMaterial (HF) | ~6,700,000 | structure | DFT-PBE/PBESol/SCAN |
| Exfoliation energy | meV/atom | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 5,824 | structure | mixed (per-method) |
| Exfoliation energy | meV/atom | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 813 | structure | DFT-OptB88vdW |
| Exfoliation energy | meV/atom | [JARVIS dft_2d (2022.12.12)](https://ndownloader.figshare.com/files/38521268) | JARVIS-DFT | 748 | structure | DFT-OptB88vdW |
| Exfoliation energy | meV/atom | [matbench_jdft2d](https://matbench.materialsproject.org/) | Matbench v0.1 | 636 | structure | DFT-OptB88vdW |
| Formation energy | eV/atom | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 8,777,728 | structure | mixed (per-method) |
| Formation energy | eV/atom | [matbench_mp_e_form](https://matbench.materialsproject.org/) | Matbench v0.1 | 132,752 | structure | DFT-PBE |
| Formation energy | eV/atom | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 75,993 | structure | DFT-OptB88vdW |
| Formation energy | eV/atom | [flla](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 3,938 | structure | DFT-PBE |
| Formation energy | eV/atom | [JARVIS dft_2d (2022.12.12)](https://ndownloader.figshare.com/files/38521268) | JARVIS-DFT | 1,103 | structure | DFT-OptB88vdW |
| Formation energy & vacancy formation energy (perovskite oxides) | eV/atom | [wolverton_oxides](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 4,914 | composition | DFT-PBE |
| Formation energy (perovskites) | eV/unit cell | [matbench_perovskites](https://matbench.materialsproject.org/) | Matbench v0.1 | 18,928 | structure | DFT-RPBE |
| Formation energy / energy above hull | eV/atom | [Materials Project](https://next-gen.materialsproject.org/) | Materials Project | ~170,000 | structure | DFT-PBE/PBE+U (r2SCAN mixing) |
| Formation energy / stability | eV/atom | [OQMD](https://oqmd.org) | OQMD | ~1,300,000 | structure | DFT-PBE |
| Formation energy, band gap | eV/atom; eV | [AFLOW](https://aflowlib.org) | AFLOW | ~3,500,000 | structure | DFT-PBE |
| Formation energy, ehull, band gap, magnetization | eV/atom | [Alexandria PBE 3D](https://alexandria.icams.rub.de) | Alexandria | ~4,500,000 | structure | DFT-PBE |
| Formation enthalpy (experimental) | eV/atom | [expt_formation_enthalpy_kingsbury](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 2,135 | composition | experiment |
| Formation enthalpy (experimental) | eV/atom | [expt_formation_enthalpy](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 1,276 | composition | experiment |
| Stability (ehull) | eV/atom | [WBM (Matbench Discovery test)](https://matbench-discovery.materialsproject.org) | Matbench Discovery | ~256,963 | structure | DFT-PBE |

### Electronic

| Property | Unit | Dataset | Collection | Samples | Input | Fidelity |
| --- | --- | --- | --- | ---: | --- | --- |
| Band gap | eV | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 7,824,894 | structure | mixed (per-method) |
| Band gap | eV | [Materials Project](https://next-gen.materialsproject.org/) | Materials Project | ~170,000 | structure | DFT-PBE |
| Band gap | eV | [matbench_mp_gap](https://matbench.materialsproject.org/) | Matbench v0.1 | 106,113 | structure | DFT-PBE |
| Band gap (double perovskites) | eV | [double_perovskites_gap](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 1,306 | composition | DFT-GLLBSC |
| Band gap (experimental) | eV | [expt_gap](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 6,354 | composition | experiment |
| Band gap (experimental) | eV | [matbench_expt_gap](https://matbench.materialsproject.org/) | Matbench v0.1 | 4,604 | composition | experiment |
| Band gap (experimental) | eV | [expt_gap_kingsbury](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 4,604 | composition | experiment |
| Band gap (HSE06) | eV | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 56 | structure | DFT-HSE06 |
| Band gap (OptB88vdW) | eV | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 75,993 | structure | DFT-OptB88vdW |
| Band gap (OptB88vdW) | eV | [JARVIS dft_2d (2022.12.12)](https://ndownloader.figshare.com/files/38521268) | JARVIS-DFT | 1,103 | structure | DFT-OptB88vdW |
| Band gap (PBE, HSE) of MOFs | eV | [QMOF](https://github.com/Andrew-S-Rosen/QMOF) | QMOF | ~20,000 | structure | DFT-PBE/HSE |
| Band gap (TBmBJ) | eV | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 19,805 | structure | DFT-TBmBJ |
| Band gap (TBmBJ) | eV | [JARVIS dft_2d (2022.12.12)](https://ndownloader.figshare.com/files/38521268) | JARVIS-DFT | 246 | structure | DFT-TBmBJ |
| Band gap, magnetic, stiffness, etc. (2D) | various | [C2DB](https://c2db.fysik.dtu.dk) | C2DB | ~16,000 | structure | DFT-PBE/HSE/G0W0 |
| Bulk/shear modulus, Debye temp, thermal conductivity (AEL-AGL) | GPa; K; W/m/K | [AFLOW AEL-AGL](https://aflowlib.org) | AFLOW | ~5,000 | structure | DFT-PBE (AEL-AGL quasi-harmonic) |
| Effective mass (electron) | m_e | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 5,209 | structure | mixed (per-method) |
| Electric field gradient (max) | V/m^2 | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 11,871 | structure | DFT |
| Electron effective mass | m_e | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 17,645 | structure | DFT-BoltzTraP |
| Electronic transport (Seebeck, conductivity) | various | [ricci_boltztrap_mp_tabular](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 47,737 | structure | DFT-PBE |
| Hole effective mass | m_e | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 17,645 | structure | DFT-BoltzTraP |
| Lattice thermal conductivity | W/m/K | [AFLOW-AGL / TCMD sets](https://aflowlib.org) | AFLOW | ? | structure | DFT |
| Metallicity (classification) | bool | [matbench_mp_is_metal](https://matbench.materialsproject.org/) | Matbench v0.1 | 106,113 | structure | DFT-PBE |
| Metallicity (classification) | bool | [matbench_expt_is_metal](https://matbench.materialsproject.org/) | Matbench v0.1 | 4,921 | composition | experiment |
| Phonon band structure/DOS (DFPT) | cm^-1 | [Petretto phonon DB](https://doi.org/10.6084/m9.figshare.c.3938023) | Materials Project | ~1,521 | structure | DFT-PBEsol (DFPT) |
| Phonon DOS peak frequency (last PhDOS peak) | cm^-1 | [matbench_phonons](https://matbench.materialsproject.org/) | Matbench v0.1 | 1,265 | structure | DFT-PBEsol (DFPT) |
| Seebeck / power factor / effective mass | various | [boltztrap_mp](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 8,924 | structure | DFT-PBE |
| Spin-orbit spillage | unitless | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 16,003 | structure | mixed (per-method) |
| Spin-orbit spillage (topology) | - | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 11,377 | structure | DFT-SOC |
| Spin-orbit spillage (topology) | - | [JARVIS dft_2d (2022.12.12)](https://ndownloader.figshare.com/files/38521268) | JARVIS-DFT | 603 | structure | DFT-SOC |
| Thermal conductivity | W/m/K | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 7,710 | structure | mixed (per-method) |
| Thermal conductivity (experimental) | W/m/K | [citrine_thermal_conductivity](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 872 | composition | experiment |
| Thermoelectric properties (Seebeck, ZT, conductivity) | various | [ucsb_thermoelectrics](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 1,093 | composition | experiment |

### Mechanical

| Property | Unit | Dataset | Collection | Samples | Input | Fidelity |
| --- | --- | --- | --- | ---: | --- | --- |
| Bulk & shear modulus (superhard) | GPa | [brgoch_superhard_training](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 2,574 | composition | DFT-PBE |
| Bulk modulus (log10 K_VRH) | log10(GPa) | [matbench_log_kvrh](https://matbench.materialsproject.org/) | Matbench v0.1 | 10,987 | structure | DFT-PBE |
| Bulk modulus (Voigt) | GPa | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 23,824 | structure | DFT-OptB88vdW |
| Bulk modulus K_VRH | GPa | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 184,040 | structure | mixed (per-method) |
| Elastic moduli / elastic tensor | GPa | [elastic_tensor_2015](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 1,181 | structure | DFT-PBE |
| Elastic properties (MAX phases) | GPa | [m2ax](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 223 | composition | DFT |
| Elastic tensor | GPa | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 25,513 | structure | DFT-OptB88vdW |
| Elastic tensor | GPa | [Materials Project](https://next-gen.materialsproject.org/) | Materials Project | ~12,000 | structure | DFT-PBE |
| Piezoelectric modulus | C/m^2 | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 8,663 | structure | mixed (per-method) |
| Poisson ratio | - | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 23,597 | structure | DFT-OptB88vdW |
| Shear modulus (log10 G_VRH) | log10(GPa) | [matbench_log_gvrh](https://matbench.materialsproject.org/) | Matbench v0.1 | 10,987 | structure | DFT-PBE |
| Shear modulus (Voigt) | GPa | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 23,824 | structure | DFT-OptB88vdW |
| Shear modulus G_VRH | GPa | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 181,088 | structure | mixed (per-method) |
| Yield & tensile strength (steels) | MPa | [steel_strength](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 312 | composition | experiment |
| Yield strength (steels) | MPa | [matbench_steels](https://matbench.materialsproject.org/) | Matbench v0.1 | 312 | composition | experiment |

### Dielectric, optical and piezoelectric

| Property | Unit | Dataset | Collection | Samples | Input | Fidelity |
| --- | --- | --- | --- | ---: | --- | --- |
| Dielectric constant (DFPT, max) | - | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 4,706 | structure | DFPT |
| Dielectric constant (total) | unitless | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 148,795 | structure | mixed (per-method) |
| Dielectric function (OptB88vdW, x) | - | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 52,168 | structure | DFT-OptB88vdW |
| Dielectric function (OptB88vdW, x) | - | [JARVIS dft_2d (2022.12.12)](https://ndownloader.figshare.com/files/38521268) | JARVIS-DFT | 887 | structure | DFT-OptB88vdW |
| Dielectric function (TBmBJ, x) | - | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 18,293 | structure | DFT-TBmBJ |
| Dielectric tensor | unitless | [Materials Project](https://next-gen.materialsproject.org/) | Materials Project | ~7,000 | structure | DFT-PBE (DFPT) |
| Dielectric tensor / refractive index | unitless | [dielectric_constant](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 1,056 | structure | DFT-PBE (DFPT) |
| Max IR mode | cm^-1 | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 4,805 | structure | DFPT |
| Phonon & dielectric properties | various | [phonon_dielectric_mp](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 1,296 | structure | DFT-PBEsol (DFPT) |
| Piezoelectric coefficient d_ij (max) | pC/N | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 3,347 | structure | DFPT |
| Piezoelectric coefficient e_ij (max) | C/m^2 | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 4,799 | structure | DFPT |
| Piezoelectric tensor | C/m^2 | [Materials Project](https://next-gen.materialsproject.org/) | Materials Project | ~3,000 | structure | DFT-PBE (DFPT) |
| Piezoelectric tensor | C/m^2 | [piezoelectric_tensor](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 941 | structure | DFT-PBE (DFPT) |
| Refractive index | unitless | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 13,287 | structure | mixed (per-method) |
| Refractive index | unitless | [matbench_dielectric](https://matbench.materialsproject.org/) | Matbench v0.1 | 4,764 | structure | DFT-PBE (DFPT) |
| SLME | % | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 12,430 | structure | mixed (per-method) |
| SLME (solar efficiency) | % | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 9,770 | structure | DFT-TBmBJ |

### Thermal and vibrational

| Property | Unit | Dataset | Collection | Samples | Input | Fidelity |
| --- | --- | --- | --- | ---: | --- | --- |
| Debye temperature | K | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 18,914 | structure | mixed (per-method) |
| Phonon max frequency | THz | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 39,491 | structure | mixed (per-method) |
| Phonon properties (harmonic) | THz | [Togo phonondb (MDR)](http://phonondb.mtl.kyoto-u.ac.jp) | phonondb | ~10,000 | structure | DFT-PBEsol |

### Thermoelectric and transport

| Property | Unit | Dataset | Collection | Samples | Input | Fidelity |
| --- | --- | --- | --- | ---: | --- | --- |
| Power factor (n) | uW/(mK^2) | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 23,218 | structure | DFT-BoltzTraP |
| Seebeck coefficient | muV/K | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 31,097 | structure | mixed (per-method) |
| Seebeck coefficient (n) | uV/K | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 23,218 | structure | DFT-BoltzTraP |
| Seebeck coefficient (n) | uV/K | [JARVIS dft_2d (2022.12.12)](https://ndownloader.figshare.com/files/38521268) | JARVIS-DFT | 806 | structure | DFT-BoltzTraP |
| Thermoelectric properties (experimental) | various | [Starrydata / Citrine TE](https://www.starrydata2.org) | Starrydata | ? | structure | experiment |

### Magnetic and superconducting

| Property | Unit | Dataset | Collection | Samples | Input | Fidelity |
| --- | --- | --- | --- | ---: | --- | --- |
| Magnetic moment | mu_B | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 71,320 | structure | DFT-OptB88vdW |
| Magnetic moment / Heusler properties | muB | [heusler_magnetic](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 1,153 | composition | DFT |
| Magnetic ordering / moment | muB | [Materials Project](https://next-gen.materialsproject.org/) | Materials Project | ~170,000 | structure | DFT-PBE |
| Superconducting Tc | K | [SuperCon (NIMS)](https://mdr.nims.go.jp/collections/4c428a0d-a5d0-41e5-bc1c-6b9a5a3e8bb3) | SuperCon | ~33,000 | structure | experiment |
| Superconducting Tc | K | [superconductivity2018](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 16,414 | composition | experiment |
| Superconducting Tc (BCS-inspired) | K | [JARVIS dft_3d (2022.12.12)](https://ndownloader.figshare.com/files/38521619) | JARVIS-DFT | 1,058 | structure | DFPT/Eliashberg |
| Superconductor class | category | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 1,918 | structure | mixed (per-method) |
| Total magnetization | muB | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 6,048,431 | structure | mixed (per-method) |

### Structural and other

| Property | Unit | Dataset | Collection | Samples | Input | Fidelity |
| --- | --- | --- | --- | ---: | --- | --- |
| CO2 uptake (MOFs) | mol/kg | [MateriaViva-Open](https://huggingface.co/datasets/AI4QC/MateriaViva-Open) | MateriaViva (HF, AI4QC) | 415,108 | structure | mixed (per-method) |
| Contributed property sets | various | [MPContribs](https://contribs.materialsproject.org) | Materials Project | ? | structure | various |
| Glass-forming ability | bool | [glass_ternary_landolt](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 7,191 | composition | experiment |
| Glass-forming ability | bool | [glass_binary](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 5,959 | composition | experiment |
| Glass-forming ability (classification) | bool | [matbench_glass](https://matbench.materialsproject.org/) | Matbench v0.1 | 5,680 | composition | experiment |
| Glass-forming ability (HiTp sputtering) | bool | [glass_ternary_hipt](https://hackingmaterials.lbl.gov/matminer/dataset_summary.html) | matminer datasets | 5,170 | composition | experiment |
| Mixed DFT outputs | various | [NOMAD](https://nomad-lab.eu) | NOMAD | ? | structure | various DFT |
| Multiple (11 properties) | various | [LLM4Mat-Bench](https://github.com/vertaix/LLM4Mat-Bench) | LLM4Mat-Bench | ~1,900,000 | structure | various |
| Pore geometry (MOFs) | A; m^2/g | [CoRE MOF 2019](https://zenodo.org/records/3677685) | CoRE MOF | ~14,000 | structure | geometric |

## Leaderboard Snapshot

Rankings change often; the values below are what each live site showed on the stated date. Check the site before quoting them.

### [Matbench Discovery](https://matbench-discovery.materialsproject.org/)

Checked 2026-11-08. Tasks: Stability discovery on WBM test set (~257k structures) + geometry optimization (RMSD) + thermal conductivity (kappa_SRME, PhononDB subset) + MD/diatomic diagnostics. Metrics: CPS, F1, DAF, Precision, Accuracy, MAE, R2, RMSD, kappa_SRME, CMDS, CDS.

| Rank | Model | Metric | Value |
| ---: | --- | --- | --- |
| 1 | DPA-4.1-Max-OAM-PFT | CPS | 0.913 |
| 2 | Prophet-OAME-MBD | CPS | 0.912 |
| 3 | DPA-4.1-Max-OAM | CPS | 0.91 |

Ranking by default CPS on the compliant+non-compliant combined table as displayed on the landing page; values read via page fetch.

### [Matbench](https://matbench.materialsproject.org/)

Checked 2026-11-08. Tasks: 13. Metrics: MAE (regression tasks, 10), ROC-AUC (classification tasks, 3).

| Rank | Model | Metric | Value |
| ---: | --- | --- | --- |
| 1 | coGN | matbench_mp_e_form mean MAE (eV/atom) | 0.017 |
| 2 | coNGN | matbench_mp_e_form mean MAE (eV/atom) | 0.0178 |
| 3 | ALIGNN | matbench_mp_e_form mean MAE (eV/atom) | 0.0215 |

No single overall ranking shown; top-3 given for the flagship mp_e_form task. Per-task leaders counted: MODNet leads 5 tasks, coGN 3, coNGN 2.

### [JARVIS-Leaderboard](https://pages.nist.gov/jarvis_leaderboard/)

Checked 2026-11-08. Tasks: 322. Metrics: MAE, RMSE, accuracy/ROC-AUC, multi-MAE (spectra).

| Rank | Model | Metric | Value |
| ---: | --- | --- | --- |
| 1 | kgcnn_coGN | dft_3d_formation_energy_peratom MAE (eV/atom) | 0.0271 |
| 2 | kgcnn_coNGN | dft_3d_formation_energy_peratom MAE (eV/atom) | 0.0291 |
| 3 | potnet | dft_3d_formation_energy_peratom MAE (eV/atom) | 0.0293 |

322 benchmarks, 2087 contributions, 503 methods; categories AI 1034, ES 741, FF 282, EXP 25, QC 6 contributions. Top-3 shown for the representative dft_3d formation-energy task.

### [MLIP Arena](https://huggingface.co/spaces/atomind/mlip-arena)

Checked 2026-11-08. Tasks: Diatomics, EOS, MD stability, phonon, NEB, elasticity, structure optimization. Metrics: physical-consistency metrics (e.g., diatomic smoothness, conservation, MD stability), runtime.

Hugging Face Space is a dynamic app; neither the Space metadata nor the GitHub README (github.com/atomind-ai/mlip-arena) exposed a ranking via fetch, so top models were not recorded.

## Contributing

Contributions are welcome. Read [CONTRIBUTING.md](CONTRIBUTING.md) for the entry format, then open a pull request or an issue.

## Citation

If this list is useful, please cite the accompanying survey once it is available:

```bibtex
@unpublished{Hu2026PropertySurvey,
  author = {Hu, Jianjun and others},
  title  = {Machine Learning for Materials Property Prediction: Features, Models, Generalization and Benchmarks},
  note   = {In preparation},
  year   = {2026}
}
```

## License

[MIT](LICENSE). Linked resources keep their own licences.
