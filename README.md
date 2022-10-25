### 16SrRNA Analysis with USEARCH
The data used in the analysis was obtained from NCBI under bioproject number : PRJEB28175 
### WORKFLOW
1.Overall quality check \
2.Preparing to stitch the reads (or merge) (Note that in the UPARSE documentation it is now recommended to merge without quality filtering, then remove primers, then quality filter in a separate step)\
3.Filtering;adapther-primer-low quality base\
4.Converting to FASTA\
5.Concatenate the high-quality FASTA files for each sequencing run\
6.Split the file into parts, each file needs to be under ~2GB\
7.Dereplicate each part. Dereplication: is the process where all of the quality filtered sequences are collapsed into a set of uniques reads, which are then clustered into OTUs\
8.Combine the outputs of the dereplicated parts, and then ran derep on this file\
9.Remove human reads (optional)\
10.OTU clustering or picking **If you use usearch command which is using UPARSE algorithm, no need to run a separate chimera-checking step\
11.Creating OTU table\
12.Assigning taxanomy to the OTU table\
13.Cleaning up the OTU table and creating a phylogenetic tree\

[For more information go to USEARCH web site](https://www.drive5.com/usearch/)
