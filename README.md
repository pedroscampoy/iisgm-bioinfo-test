# iisgm-bioinfo-test
Aptitude test for IiSGM Microbial Genomics candidates

## Instructions

You are required to calculate SNP distance between those 26 *M. tuberculosis* isolates provided :microbe:.

The input files are in VCF 4.2 format, obtained with [GATK](https://gatk.broadinstitute.org/), but all information about the parameters are included within the file.

- [Python](https://www.python.org/) language **is required** to complete this test
- [Pandas](https://pandas.pydata.org/) is strongly adviced

## Submission

- You can send the asigment directly to pedroscampoy@gmail.com in whichever comprised format suits you
- Or you can create a pull request if you are familiar with github:

  - Fork this repo
  - Clone this repo
  - Upon completion, run the following commands:

    ```
    git add .
    git commit -m "done"
    git push origin master
    ```

  - Create Pull Request


### Iteration 0 | Download repository

You can download this repository with the data included using the terminal (CLI) or as .zip

### Iteration 1 | Parse VCF files to table/dataframe

In data folder you can find all VCF

Create a function to read a single VCF

### Iteration 2 | Extract relevant information from parsed VCF

*M. tuberculosis* in an haployd organism but those were called (variant calling step) as diploid, hence you will see the usual diploid genotyping (0/0, 0/1, 1/1).

With the correct information analysed, filter the SNPs actualy present on each sample, this can be a different function.

### Iteration 3 | Combine SNP presence into a presence matrix

Merge estracted information into a matrix to keep track of relecant info such as:
- sample name
- Position
- Mutation (Reference allele and Alternate allele)

The preferred format is a binary Presence/Absence matrix

### Iteration 5 | Calculate the SNP distance between all samples

Determine the pairwise distance between each pair of samples

### Iteration 6 | BONUS - Include INDELS

We have been using the term SNP distance but INDELS are also useful as phylogenetic marker

Add sutle changes to the functions to include INDELS in the distance calculation

### Iteration 7 | BONUS - Represent distance in a phylogenetic tree

You can represent this distance in a dendrogram.

To follow along with the matrix format and the use of python, you are encouraged to use [Scipy library](https://www.scipy.org/), specifically [linkage](https://docs.scipy.org/doc/scipy/reference/generated/scipy.cluster.hierarchy.linkage.html#scipy.cluster.hierarchy.linkage) and [dendrogram](https://docs.scipy.org/doc/scipy/reference/generated/scipy.cluster.hierarchy.dendrogram.html#scipy.cluster.hierarchy.dendrogram)
