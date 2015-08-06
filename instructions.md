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

### First assignment
Try to write some pseudocode for this script. What are the basic steps this code will have to do? You don't need to know any particulars about the bash programming language to do this. Just write your pseudocode in plain english like so:

Step 1) Read in command line arguments   
Step 2) Set a variable for each transcription factor family given in the command line
etc, etc...

### Second assignment

Using your pseudocode, try to write code for one or two steps in your pseudocode. 
Write down what problems you encounter and what steps you expect the challenges to be.

### Next step

Try to put together a full working script. This can either contain all the commands you want to call. Alternatively, you can write a number of small scripts, one for each step. Then you can write a master script that calls each small script in turn.

### Extra credit

Learn about [CASE online](http://ryanstutorials.net/bash-scripting-tutorial/bash-if-statements.php). Try to use CASE to modify your scripts and allow for your script to be called in different orders.

>**generateFactorFastas.sh -organism** *\<organism\>* **-families** *\<TFfamily1\>,[TFfamily2],[TFfamily3]*

OR

>**generateFactorFastas.sh -families** *\<TFfamily1\>,[TFfamily2],[TFfamily3]* **-organism** *\<organism\>* 


