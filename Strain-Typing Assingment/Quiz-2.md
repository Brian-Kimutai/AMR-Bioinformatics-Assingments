### Quiz 2

> Using a loop,use MLST to do strain typing of the downloaded Files in Question 1, save the results as a tsv file with only the first two columns of the output of mlst;

- Multi-Locus Sequence Typing (MLST) is a molecular genotyping method used to characterize and classify microorganisms,mostly bacteria, based on sequence variations in multiple housekeeping genes.
- To do this, I used the folowing Bash Script;
  
```
#!/bin/bash

output_file="strain_typing_results.tsv"

for Accessions in  ; do

  mlst $Accessions > tmp_output.txt
  
  awk {print $1 "\t" $2} tmp_output.txt >> $output_file
  
done

```
