# Instructions for the bash small group final project

### Instructions

Write a script called generateFactorFastas.sh

This script should be executed in the following manner:

>**generateFactorFastas.sh -organism** *\<organism\>* **-families** *\<TFfamily1\>,[TFfamily2],[TFfamily3]*

For our first attempt at this assignment, we'll stick to the organism Saccharomyces cerevisiae, so the script will be executed:

>**generateFactorFastas.sh -organism yeast -families** *\<TFfamily1\>,[TFfamily2],[TFfamily3]*

The following parts of the command line will indicate the following things:
+ **generateFactorFastas.sh** the name of the script.
  + **-organism** a flag that is currently static but that later we will be able to alter to different organisms.
  + **-families** a flag that accepts a comma-separated list of different transcription factor families.

### Input:  
+ Scerevisiae_TFs.csv file
+ the *S. cerevisiae* genome
+ the *S. cerevisiae* gtf annotation file

### Output:
For each TF family that is supplied the script should output a fasta file entitled Scer_TFfamily1_CDS.fa that contains the coding sequence of each transcription factor DNA sequence like so:

```
$ more Scer_GATA_CDS.fa
>YAL1348C
ATGACTCTACAAGAATCTGATAAATTTGCTACCAAGGCCATTCATGCCGGTGAACATGTGGACGTTCACGGTTCCGTGATCGAACCCATTTCTTTGTCCACCACTTTCAAACAATCTTCTCCAGCTAACCCTATCGGTACTTACGAATACTCCAGATCTCAAAATCCTAACAGAGAGAACTTGGAAAGAGCAGTTGCCGCTTTAGAGAACGCTCAATACGGGTTGGCTTTCTCCTCTGGTTCTGCCACCACCGCCACAATCTTGCAATCGCTTCCTCAGGGCTCCCATGCGGTCTCTATCGGTGATGTGTACGGTGGTACCCACAGATACTTCACCAAAGTCGCCAACGCTCACGGTGTGGAAACCTCCTTCACTAACGATTTGTTGAACGATCTACCTCAATTGATAAAGGAAAACACCAAATTGGTCTGGATCGAAACCCCAACCAACCCAACTTTGAAGGTCACCGACATCCAAAAGGTGGCAGACCTTATCAAGAAGCACGCTGCCGGCCAAGACGTGATCTTGGTTGTCGACAACACCTTCTTGTCCCCATATATCTCCAATCCATTGAACTTCGGTGCAGACATCGTTGTCCACTCCGCTACAAAGTACATCAACGGTCACTCAGACGTTGTGCTCGGTGTCCTGGCCACTAATAACAAGCCATTGTACGAGCGTCTGCAGTTCTTACAAAACGCCATTGGTGCTATCCCATCTCCTTTCGATGCTTGGTTGACCCACAGAGGTTTGAAGACTTTGCATCTACGTGTCAGACAAGCTGCCCTCAGCGCCAACAAAATCGCTGAATTCTTGGCAGCAGACAAGGAAAACGTTGTCGCAGTCAACTACCCAGGTTTGAAGACACACCCTAACTACGACGTAGTGTTAAAGCAACACCGTGATGCCCTTGGTGGTGGTATGATCTCCTTCAGAATCAAGGGTGGTGCTGAAGCTGCTTCCAAGTTCGCCTCCTCCACAAGACTGTTCACATTGGCCGAATCCCTTGGTGGTATCGAATCTCTATTGGAAGTGCCCGCTGTGATGACCCACGGTGGTATCCCAAAGGAGGCCAGAGAGGCCTCTGGTGTTTTTGACGACTTGGTTAGAATCTCTGTCGGTATTGAAGACACTGACGATCTTTTGGAAGACATCAAGCAAGCCTTGAAACAAGCCACCAAC
>YCAJ348C
ATGATCGTAAATAACACACACGTGCTTACCCTACCACTTTATACCACCACCACATGCCATACTCACCCTCACTTGTATACTGATTTTACGTACGCACACGGATGCTACAGTATATACCATCTCAAACTTACCCTACTCTCAGATTCCACTTCACTCCATGGCCCATCTCTCACTGAATCAGTACCAAATGCACTCACATCATTATGCACGGCACTTGCCTCAGCGGTCTATACCCTGTGCCATTTACCCATAACGCCCATCATTATCCACATTTTGATATCTATATCTCATTCGGCGGTCCCAAATATTGTA
>YAL3843C
ATGCACGGCACTTGCCTCAGCGGTCTATACCCTGTGCCATTTACCCATAACGCCCATCATTATCCACATTTTGATATCTATATCTCATTCGGCGGTCCCAAATATTGTATAACTGCCCTTAATACATACGTTATACCACTTTTGCACCATATACTTACCACTCCATTTATATACACTTATGTCAATATTACAGAAAAATCCCCACAAAAATCACCTAAACATAAAAATATTCTACTTTTCAACAATAATACA
```