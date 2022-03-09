# NextFlow-Genomics-Processing

# Format Conversion + Variant calling in one-step (BAM-to-VCF). Single Sample Variant Calling

A single workflow that combines Paired-fastqs to uBAM and Per-Sample Variant Calling.

Takes fastq files as inputs and outputs vcf files.

```
  nextflow run aws-nextflow-gatk/fastq_to_variant_calls.nf \
  -work-dir s3://<your_bucket>/work \
  --outdir s3://<your_bucket>/results/fastq-to-ubam/ \
  --input_fofn s3://<your_bucket>/input_files/fastq_manifest.txt \
  --projectId my-project 
  
  ```
 # Inputs:

- work-dir: nextflow work directory. Must be a location in s3
- outdir: location in s3 where outputs are saved
- input_fofn: an input manifest file of tab-delimited values as in Paired-fastqs to uBAM 
- projectId: used as directory name for output vcf files 

# To Do

- Implement GVCF genotyping (using JointGenotyping.nf)
- Implement CNN-based caller?
- Variant Annotation 
