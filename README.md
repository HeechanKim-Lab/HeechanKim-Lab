# Heechan Kim
**Undergraduate Researcher | Molecular Engineering & Computer Science, Dong-A University**

Undergraduate researcher specializing in computational biology, high-throughput sequencing pipelines, and molecular biology. Experienced in designing reproducible bioinformatics workflows for transcriptomic and amplicon metagenomic systems, supported by rigorous hands-on wet-lab assay design.

* **Email:** 2218160@donga.ac.kr
* **Location:** Busan, South Korea
* **Affiliation:** [Plant Immunity & Epigenetics Laboratory](https://web.donga.ac.kr/hwjung/page02.htm), Department of Molecular Genetics, Dong-A University

---

## Featured Research Projects & Pipelines

### [arabidopsis-microplastic-rnaseq](https://github.com/HeechanKim-Lab/arabidopsis-microplastic-rnaseq)
*Transcriptomic profiling of Arabidopsis thaliana root responses to low-density polyethylene (LDPE) microplastic exposure.*

* **Upstream Processing:** Implemented an end-to-end RNA-seq workflow utilizing HISAT2 for paired-end alignment against the TAIR10 reference genome, samtools for coordinate sorting, and StringTie for reference-guided transcript assembly, transcriptome merging, and abundance estimation.
* **Statistical Modeling & Outlier Diagnostics:** Conducted differential expression analysis in edgeR. Diagnosed high biological dispersion caused by a technical outlier replicate in PCA space (PC1 49%, PC2 18%), systematically evaluated degrees-of-freedom penalties across nested sample cohorts, and transitioned from Quasi-Likelihood F-tests to Likelihood Ratio Tests (LRT) to recover 865 significant DEGs (FDR < 0.05, |log2FC| > 1).
* **Downstream Functional Enrichment:** Mapped assembled transcripts to TAIR loci, generated publication-quality volcano plots and row-scaled Z-score heatmaps, and conducted Gene Ontology (BP, MF, CC) and KEGG pathway enrichment using clusterProfiler to characterize stress-response activation and cell-wall suppression.
* **Stack:** R (edgeR, clusterProfiler, ggplot2, pheatmap), Python, Bash, HISAT2, StringTie, samtools.

### [microtom-rhizosphere-amplicon](https://github.com/HeechanKim-Lab/microtom-rhizosphere-amplicon)
*High-throughput 16S and ITS2 amplicon metagenomics profiling rhizosphere succession in Solanum lycopersicum cv. 'Micro-Tom'.*

* **Computational Infrastructure & Denoising:** Established an emulated osx-64 execution environment on Apple Silicon via Rosetta 2 to maintain toolchain compatibility. Ingested 12 discrete sequencing batches across Casava 1.8 formats, stripped heterogeneity N-spacers and degenerate primers using Cutadapt, and trained run-specific DADA2 error models with locus-specific truncation strategies (260/200 bp for 16S; non-truncated for ITS2).
* **Phylogenetic Inference & Taxonomic Decontamination:** Reconstructed midpoint-rooted phylogenetic trees for 16S using MAFFT and FastTree. Filtered non-target host plant organellar sequences against SILVA 138 (16S) and enforced positive fungal domain inclusion against UNITE v10 (ITS2).
* **Ecological Diversity & Experimental Auditing:** Standardized rarefaction depths (27,000 reads for 16S; 8,600 reads for ITS2). Performed PERMANOVA and multivariate dispersion audits (`betadisper`) across metric PCoA and non-metric MDS (NMDS) ordinations (Bray-Curtis, Jaccard, Weighted/Unweighted UniFrac). Identified and resolved batch asynchrony, proving the necessity of synchronous paired-control benchmarking.
* **Differential Abundance & Functional Metagenomics:** Modeled continuous effect sizes and well-calibrated FDR thresholds using LinDA to decouple shared soil generalists from lineage-specific private consortia. Reconstructed MetaCyc metabolic pathway potentials using PICRUSt2 (EPA-ng, GAPPA, castor, MinPath) and ggpicrust2.
* **Stack:** QIIME 2, R (phyloseq, LinDA, ggpicrust2, vegan), Python, DADA2, FastTree, Cutadapt, PICRUSt2.

### [plant-epigenomics-wetlab](https://github.com/HeechanKim-Lab/plant-epigenomics-wetlab)
*Experimental protocols, quality assurance logs, and molecular assay optimization records.*

* **Targeted Deep Sequencing Preparation:** Developed a 3-step nested indexing PCR pipeline targeting CRISPR/Cas edit sites in *S1UPF3a* knockout candidate lines of *S. lycopersicum* cv. 'Micro-Tom'. Implemented spatial wall-isolation loading to eliminate premature non-specific amplification prior to thermal denaturation.
* **High-Throughput qPCR Assays:** Configured 384-well optical real-time PCR arrays tracking target transcripts against *Actin* controls across transgenerational cohorts. Engineered a bottom-up loading protocol with progressive adhesive photo-shielding to prevent SYBR Green photobleaching during prolonged manual setup.
* **Nucleic Acid & Protein Biochemistry:** Executed high-throughput extraction protocols including TRIzol/TURBO DNase total RNA isolation, modified CTAB genomic DNA extraction with reduced initial lysis volume to control splashing during mechanical drilling, detergent-reducing protein extractions coupled with cryogenic TissueLyser disruption, and bacterial plasmid vector recovery (pGEX-5X-1 in *E. coli* DH5α).
* **Plant Cultivation Systems:** Standardized cold stratification, hydrodynamic wide-bore seed singulation, and pathogen inoculation preparation for *Arabidopsis thaliana*, along with Murashige & Skoog (0.5× MS) aseptic media formulations.

---

## Technical Proficiencies

* **Computational Biology:** Bulk RNA-Seq, 16S/ITS Amplicon Sequencing, Functional Metagenome Inference (PICRUSt2), Differential Expression (edgeR), Differential Abundance Testing (LinDA), Rarefaction & Ordination (PCoA, NMDS)
* **Bioinformatics Software:** QIIME 2, DADA2, HISAT2, StringTie, samtools, FastTree, MAFFT, Cutadapt
* **Languages & Systems:** Python, R, C/C++, Bash/Unix Shell, Git, Conda, Linux, macOS (Rosetta 2 emulation)
* **Data Science & Visualization:** Bioconductor, phyloseq, clusterProfiler, ggplot2, pheatmap, vegan, NumPy, SciPy
* **Wet-Lab Molecular Biology:** Targeted Deep Sequencing Library Prep, 384-Well qPCR (Delta-Delta Ct), CTAB/PCI DNA Extraction, TRIzol/DNase RNA Isolation, Cryogenic Tissue Pulverization, Plant Tissue Culture

---

## Education

* **B.S. in Molecular Engineering and Computer Science (Double Major)**  
  Dong-A University, Busan, South Korea (Junior, Expected Graduation: 2028)
