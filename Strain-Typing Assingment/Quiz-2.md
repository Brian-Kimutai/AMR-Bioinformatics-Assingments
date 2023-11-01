### Quiz 2

> Using a loop,use MLST to do strain typing of the downloaded Files in Question 1, save the results as a tsv file with only the first two columns of the output of mlst;

- Multi-Locus Sequence Typing (MLST) is a molecular genotyping method used to characterize and classify microorganisms,mostly bacteria, based on sequence variations in multiple housekeeping genes.
- To do this, I used the folowing Bash Script;

   ```
  #!/bin/bash

output_file=mlst_results.tsv
echo -e "Sample\tMLST_Type" > "$output_file"

input_files=("file1.fasta" "file2.fasta" "file3.fasta")

for input_file in "${input_files[@]}"; do
    
    mlst_output=$(mlst "$input_file")
    
    sample_name=$(basename "$input_file" | cut -d. -f1)  # Extract sample name from the filename
    mlst_type=$(echo "$mlst_output" | awk '{print $1 "\t" $2}')


    echo -e "$sample_name\t$mlst_type" >> "$output_file"
done

echo "Strain typing results saved to $output_file"
