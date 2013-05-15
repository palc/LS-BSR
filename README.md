LS-BSR is a method to compare all coding regions in a large set of genomes.
Each peptide is compared against it's nucleotide sequence in order to obtain
the maximum BLAST bit score.  Each peptide is then aligned against each genome
in order to find the query BLAST bit score.  The query dividied by the reference
provides one with the BSR, which can range from 0 to 1.

To run the program, the following dependencies are required:

<<<<<<< HEAD
1.  USearch (tested version is 6.0.307), must be in path and called "usearch6"
2.  BioPython, must be in PythonPath
3.  blastall (tested version is 2.2.25), must be in path
4.  Prodigal (tested version is 2.60), must be in path
=======
1.  USearch (currently only works with v6)
2.  BioPython (tested version is 0.16)
3.  blastall (tested version is 2.2.25)
4.  Prodigal (tested version is 2.60)
>>>>>>> c4f99bf2a7093d93374e9f21154b544dd26a7e76

Command line options include:

-d DIRECTORY, --directory=DIRECTORY : the directory to your fasta files, all must end in 
".fasta"
-i ID, de-replication clustering value for USEARCH, defaults to 0.9 (range from 0.0-1.0)
-f FILTER, whether to use BLAST filtering, default is "F" or filter, turn off with "T"
-p PROCESSORS, number of processors to use, defaults to 2
-g GENES, if you have a list of genes to screen, supply a nucleotide fasta file.  If this 
flag is not envoked, then the de novo gene prediction method is applied 