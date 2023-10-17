### Quiz 002 : Genome Assembly Using Flye
- Flye is a tool used to assemble long reads of data such as those of Oxford Nanopore Sequencing or Pacbio sequencing platforms, its a Denovo assembler for single molecule reads;
- To install Flye , Create a Conda Environment  where the packages will be installed, activate the environment and use the syntax;

  ```
  conda install -c bioconda flye
  ```
- To check the version of flye;
  ```
  flye --version
  ```
  ```
  flye --help
  ```
- To do Assembly of raw data,{seq.fastq} ; input 
  
  ```
   flye --nano-raw seq.fastq --genome-size 5.5m --threads 12 -o Assembly
  ```
   
![Flye Image](https://github.com/Brian-Kimutai/AMR-Bioinformatics-Assingments/blob/main/Images/Flye_Image001.png)
