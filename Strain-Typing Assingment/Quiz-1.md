## Quiz 1

> Download multiple E.coli fastq files from SRA NCBI Database and document the command(s) used ;

- To download multiple FASTQ files from the NCBI Sequence Read Archive (SRA), you can use the SRA Toolkit (SRA-Toolkit) tools provided by NCBI. These tools allow you to access and download data from the SRA efficiently. 
- Here are the general steps I folowed to download the files:

1. Install the SRA Toolkit:
   
   While there are other ways to download the SRA Toolkit, I used Conda to install the Toolkit,
   
```
conda create -y -n ncbi-tools -c conda-forge -c bioconda -c defaults sra-tools=2.10.1 entrez-direct=13.9
```
 This command creates a new Conda environment named "ncbi-tools" and installs specific packages with particular versions,`-c conda-forge -c bioconda -c defaults` ; these options define the Conda channels from which to search for packages.
 
`entrez-direct=13.9 `:  part of the command specifies that you want to install the "entrez-direct" package version 13.9. entrez-direct is a set of utilities for accessing and downloading data from NCBI's Entrez system, which is used for searching and retrieving biomedical literature and data.

2. Search for SRA Accessions:
   
Determine the SRA accessions for the data you want to download. You can find these accessions by searching the NCBI SRA database (https://www.ncbi.nlm.nih.gov/sra) or by using relevant keywords.
I used the accessions ;

 - SRR26466680
 - SRR26466681
 - SRR26466679
 - SRR26466678
 - SRR26478287

3. Download the SRA data and Covert the files to FASTQ
   
- Use the `prefetch` command to download the SRA data for the accessions you've chosen and `fasterq-dump` command to convert the SRA data into FASTQ format.
- While there are other ways to do this , You can use a for loop to download the files, Here's a loop I used to do this:
  
```
  #!/bin/bash
                                                                               
accessions=(SRR26466680 SRR26466681 SRR26466679 SRR26466678 SRR26478287)

for accession in SRR26466681 SRR26466679 SRR26466678 SRR26478287; do
    echo "Downloading $accession..."

    prefetch $accession

    fasterq-dump $accession

    echo "Downloaded and converted $accession to FASTQ"
done

```
    

    
