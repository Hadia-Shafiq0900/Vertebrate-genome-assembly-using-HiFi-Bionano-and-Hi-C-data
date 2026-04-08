# Vertebrate Genome Assembly using Galaxy (VGP Pipeline)

## 📌 Overview
This project demonstrates a complete **de novo genome assembly workflow** using the Galaxy platform, following the Vertebrate Genomes Project (VGP) pipeline.

The goal is to generate a **high-quality genome assembly** using multiple sequencing technologies including:
- HiFi (PacBio long reads)
- Hi-C data
- Bionano optical maps

---

## 🎯 Objectives
- Perform genome assembly using HiFi reads
- Analyze genome characteristics using k-mer profiling
- Generate haplotype-resolved assemblies
- Evaluate assembly quality using multiple metrics

---

## 🧬 Workflow Summary

### 1. Data Upload
- Uploaded HiFi reads (`.fasta`)
- Uploaded Hi-C reads (`.fastq.gz`)
- Organized datasets in Galaxy history

---

### 2. Preprocessing
- Used **Cutadapt** to clean HiFi reads

---

### 3. Genome Profiling
- Generated k-mer spectra using **Meryl**
- Estimated genome size, heterozygosity using **GenomeScope2**

---

### 4. Assembly (Core Step)
- Performed assembly using **Hifiasm**
- Generated:
  - Hap1 contigs
  - Hap2 contigs

---

### 5. Format Conversion
- Converted GFA → FASTA using **gfastats**

---

### 6. Assembly Evaluation
Used:
- **gfastats** → contig stats (N50, length, count)
- **BUSCO** → completeness
- **Merqury** → k-mer based validation

---

### 7. Purging (Optional)
- Removed duplicate regions using **purge_dups**

---

### 8. Scaffolding
- Performed hybrid scaffolding using:
  - **Bionano optical maps**
  - **Hi-C data (YaHS)**

---

### 9. Final Output
- Chromosome-level genome assembly
- Improved contiguity and accuracy

---

## 📊 Key Concepts

- **Contigs**: Continuous DNA sequences
- **Scaffolds**: Ordered contigs with gaps
- **N50**: Assembly quality metric
- **HiFi Reads**: Long and highly accurate reads
- **Phasing**: Separating maternal and paternal genomes

---

## 🛠️ Tools Used

- Galaxy Platform
- Cutadapt
- Meryl
- GenomeScope2
- Hifiasm
- gfastats
- BUSCO
- Merqury
- purge_dups
- YaHS

---

## 📈 Results
- Generated haplotype-resolved genome assembly
- Improved scaffold length and continuity
- Evaluated completeness and accuracy

---

## 📚 Reference
Galaxy Training Network Tutorial:
https://training.galaxyproject.org/training-material/topics/assembly/tutorials/vgp_genome_assembly/tutorial.html

---

## 🧑‍💻 Author
Hadia Shafiq
