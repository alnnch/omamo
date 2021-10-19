OMAMO is an orthology-based tool for finding the best model organism to study a biological process in human. 

The user can consider several species as potential model organisms and the algorithm will rank them and report the output for a given biological process (searched as a GO term or a GO ID) is produced in the dataframe format.

**Pipeline**

Firstly, download the OMA Server (caution: a GB file):

```wget  https://omabrowser.org/All/OmaServer.h5  -O data/OmaServer.h5```

Secondly, using the file 'data/oma-species.txt' find the five-letter UniProt code for species of interest. 

For example, consider three species _Dicdyostelium discodeium_ , _Neurospora crassa_ and _Schizosaccharomyces pombe_. Their UniProt codes are 'DICDI', 'NEUCR' and 'SCHPO', respectively.

For species in 'DICDI', 'NEUCR' and 'SCHPO', do:

```python3 one_sp.py OmaServer.h5 go_positive_annotations.tsv ${species}```

Once the code finished running, the outputs are combined to create a final dataframe using the code:

```python3 create_dataframe.py folder?```


