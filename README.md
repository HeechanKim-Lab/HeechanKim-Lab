# Heechan Kim
**Undergraduate Researcher | Molecular Engineering & Computer Science, Dong-A University**

Undergraduate researcher in computational biology. Experience in RNA-seq and amplicon sequencing (16S rRNA, ITS2) analysis with scripted workflows and dated analysis logs, and molecular bench work (nucleic acid extraction, qPCR, amplicon library PCR).

* **Email:** 2218160@donga.ac.kr
* **Location:** Busan, South Korea
* **Affiliation:** [Plant Immunity & Epigenetics Laboratory](https://web.donga.ac.kr/hwjung/page02.htm), Department of Molecular Genetics, Dong-A University

---

## Research projects

### [arabidopsis-microplastic-rnaseq](https://github.com/HeechanKim-Lab/arabidopsis-microplastic-rnaseq)
*RNA-seq of Arabidopsis thaliana roots grown in soil containing low-density polyethylene (LDPE) mulching-film residues (≥ 5 mm), a source of microplastics in soil.*

* **Upstream processing (six-library pilot):** paired-end alignment to the TAIR10 genome with HISAT2, coordinate sorting with samtools, and reference-guided assembly, merging and quantification with StringTie.
* **Differential expression (pilot):** edgeR. One control library was an outlier in quality control: it had the lowest alignment rate and separated from the other five on PC1 (49% of variance; PC2, 18%). Quasi-likelihood F-tests found 1, 12 and 0 genes at FDR < 0.05 with six, five and four libraries. A likelihood ratio test on all six libraries gave 865 genes (FDR < 0.05, |log2FC| > 1), used as an exploratory list.
* **Functional enrichment (pilot):** StringTie gene IDs mapped to TAIR loci; volcano plot and row Z-score heatmap; GO (BP, MF, CC) and KEGG enrichment with clusterProfiler. Compared with the 0% plastic control, roots in 5% plastic soil pre-incubated for 120 days had higher expression of genes for cell wall organisation, root hairs and phenylpropanoid biosynthesis, and lower expression of genes for starvation and hypoxia responses.
* **Factorial experiment (27 libraries):** 0, 1 or 5% plastic × 0, 30 or 120 days of soil pre-incubation, three replicates. edgeR likelihood ratio tests for plastic, pre-incubation and interaction contrasts on a count matrix provided by the lab; PCA, PERMANOVA and two-way ANOVA on PC scores.
* **Stack:** R (edgeR, clusterProfiler, vegan, ggplot2, pheatmap), Python, Bash, HISAT2, StringTie, samtools.

**Prior work:** [Lee et al. (2025), *Journal of Experimental Botany* 76: 7003–7025](https://academic.oup.com/jxb/article/76/22/7003/8213809) describes this soil and plastic system and its effects on plant growth, the rhizosphere bacterial community and the leaf transcriptome.

### [microtom-rhizosphere-amplicon](https://github.com/HeechanKim-Lab/microtom-rhizosphere-amplicon)
*16S rRNA (V3–V4) and ITS2 amplicon sequencing of the tomato (Solanum lycopersicum cv. Micro-Tom) rhizosphere after treatment with soil suspensions from two sites.*

* **Environment:** QIIME 2 and PICRUSt2 in `osx-64` conda environments under Rosetta 2 on Apple Silicon.
* **Processing:** six MiSeq batches imported separately (Casava 1.8 format); primers and 0–3 nt spacers removed with cutadapt; DADA2 run per batch (16S truncated at 260/200 bp; ITS2 not truncated).
* **Taxonomy and phylogeny:** naive Bayes classification against SILVA 138 (16S) and UNITE v10 (ITS2); mitochondrial, chloroplast and other non-target features removed from 16S; only fungal features kept for ITS2; midpoint-rooted 16S tree with MAFFT and FastTree.
* **Diversity:** rarefaction to 27,000 (16S) and 8,600 (ITS2) reads; PCoA and NMDS; PERMANOVA and dispersion tests (`betadisper`) on Bray–Curtis, Jaccard and weighted/unweighted UniFrac distances.
* **Design checks:** the two control groups, grown at different times, differed in composition (PERMANOVA R² 0.08–0.11), so each treatment was compared with its own control. One batch whose sample labels could not be verified was removed; the final set has 110 samples from five batches.
* **Differential abundance and function:** LinDA for ASVs (each treatment against its own control; FDR < 0.05, |log2FC| ≥ 1); MetaCyc pathway abundances predicted with PICRUSt2 (EPA-ng, castor, MinPath) and compared with LinDA.
* **Stack:** QIIME 2, DADA2, cutadapt, MAFFT, FastTree, PICRUSt2, R (qiime2R, vegan, MicrobiomeStat, ggpicrust2, pheatmap), Python (pandas).

### [plant-epigenomics-wetlab](https://github.com/HeechanKim-Lab/plant-epigenomics-wetlab)
*Bench records of molecular biology and plant work, May–September 2026.*

* **Amplicon libraries for genotyping:** three-step PCR (locus, nested and dual-index) on 15 *SlUPF3a* CRISPR knockout candidate lines of tomato cv. Micro-Tom; gel extraction and NanoDrop quality checks.
* **qPCR:** expression of *UPF2* and *SRRM1-like* relative to *Actin* in cDNA from 24 F1 plants of the multi-generation soil experiment (384-well plate, SYBR Green, technical triplicate).
* **Extraction:** total RNA (TRIzol, TURBO DNase, PCI clean-up) and protein from 64 tomato leaf samples ground in liquid nitrogen (TissueLyser); genomic DNA by CTAB with drill grinding, using a smaller initial buffer volume to limit splashing; plasmid pGEX-5X-1 from *E. coli* DH5α.
* **Plant work:** Arabidopsis seed sterilization, stratification and sowing; a *Pseudomonas syringae* leaf-infiltration assay with bacterial counts (method test on untreated plants); 1/2 MS medium; GUS staining and tissue clearing (course practical).

---

## Skills

* **Computational biology:** bulk RNA-seq, 16S/ITS2 amplicon sequencing, functional prediction from 16S data (PICRUSt2), differential expression (edgeR), differential abundance (LinDA), rarefaction and ordination (PCoA, NMDS).
* **Bioinformatics software:** QIIME 2, DADA2, HISAT2, StringTie, samtools, FastTree, MAFFT, cutadapt.
* **Languages and systems:** Python, R, C/C++, Bash, Git, Conda, Linux, macOS (Rosetta 2).
* **Data analysis and visualization:** Bioconductor, clusterProfiler, vegan, ggplot2, pheatmap, NumPy, SciPy.
* **Wet lab:** amplicon library preparation (three-step PCR), 384-well SYBR Green qPCR (ΔΔCt), CTAB/PCI DNA extraction, TRIzol/DNase RNA extraction, tissue grinding in liquid nitrogen, sterile plating on MS and B5 media, *P. syringae* infection assay.

---

## Education

* **B.S. in Molecular Engineering and Computer Science (Double Major)**  
  Dong-A University, Busan, South Korea (Junior, Expected Graduation: 2028)
