
# This is the fork of Kingsford-Group/hictda

# Usage
```
python HiC_TDA.py -i input_file_name -o output_file_name -p output_path -r resolution
```
This will generate distance matrix of HiC data and output persistence pairs and all the simplices appeared during the persistent homology. 

Option Tag | Description
----------------------- | -----------------------------
-i \<inputfile>| the input file, a normalized HiC contact matrix
-p \<path> | the directory containing output files 
-o | the name of output files
-r | The resolution of HiC data

Here is an example:
```
python HiC_TDA.py -i example/input/RUES2_CM_combined_100000_iced_chr22.matrix -p example/output/ -o RUES2_CM_combined_100000_iced_chr22 -r 100000
```
Run this command line, and we will get three output files:

1: RUES2_CM_combined_100000_iced_chr22_distmat.txt
This file saves the distance matrix generated from original HiC contact matrix. 

2: RUES2_CM_combined_100000_iced_chr22_persisdiagram.txt
This file contains all the persistent diagram generated from persistent homology
- the first column: the dimension of a homology class
- the second column: birth time
- the third column: death time
- the fourth column: persitence pairs

3: RUES2_CM_combined_100000_iced_chr22_skeleton.txt
This file contains all the sinmplices generated from persistent homology. 
- the first column: a set of nodes representing one simplex
- the second column: the birth time of the simplex