  ### Quiz 001
  > Download the FastQ file; Nanopore FASTQ Accession number: SRR24415235 from SRA, NCBI
  and Generate a FastQC Report

. Fast QC is a tool used for quality control on raw sequence data coming from high throughput sequencing pipelines.
. The Sequence Read Archive (SRA) is the National Center for Biotechnology Information (NCBI) database that stores sequence data obtained from next generation sequence technology.

. To generate a FastQC report ; input 
```
conda activate qc{ name of env. where Fastqc is installed}
```
```
fastqc seq.fastq {name of fastq file downloaded from SRA}
```
 . For each individual FASTQ file that is input to FastQC, there are two output files that are generated.
 
 1.The first is an HTML file which is a self-contained document with various graphs embedded into it. Each of the graphs evaluate different quality aspects of  data,
 
 2.Alongside the HTML file is a zip file (with the same name as the HTML file, but with .zip added to the end). This file contains the different plots from the report as separate image files but also contains data files.

 Viewing the data - The fastqc report can be viewed using a web browser.
 
