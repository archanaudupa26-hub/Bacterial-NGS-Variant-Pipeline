# Automated Bacterial NGS Variant Calling Pipeline

An automated, end-to-end command-line pipeline designed to process raw Next-Generation Sequencing (NGS) data, map sequences against a structural reference framework, and isolate genetic variations (SNPs/Indels). 

This repository demonstrates the configuration of scalable computational workflows for genomics data processing outside traditional high-performance computing (HPC) environments using open-source bioinformatics tools.

## Pipeline Architecture
```text
[Raw FASTQ Reads] ──► [FastQC Quality Control]
                             │
 [Reference Genome] ──► [BWA-MEM Alignment] ──► [SAM Mapping Alignment File]
                                                       │
                                               [Samtools Processing]
                                                       │
                                             [Sorted & Indexed BAM]
                                                       │
                                               [Bcftools Calling]
                                                       │
                                                       ▼
                                             [Final Annotated VCF]
```

## Technical Core & Toolset
* **Environment:** Linux / Bash Shell Scripting
* **Package Management:** Conda (Bioconda Distribution)
* **Quality Control:** FastQC v0.12.1 (Assessment of base quality distributions)
* **Sequence Alignment:** BWA-MEM v0.7.17 (High-fidelity mapping to reference genome templates)
* **Alignment Processing:** Samtools v1.17 (Format conversion, structural sorting, and index building)
* **Variant Discovery:** Bcftools v1.17 (Mpileup likelihood scoring and genotype determination)

## Key Project Deliverable
The pipeline successfully condenses high-throughput raw sequence reads into a structured Variant Call Format (`.vcf`) matrix containing high-confidence nucleotide polymorphisms. This implementation highlights computational workflow reproducibility, clean terminal automation, and infrastructure readiness for enterprise cloud architectures.
  
