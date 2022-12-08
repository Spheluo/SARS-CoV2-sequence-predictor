# SARS-CoV-2 sequence predictor

we aimed to predict the sequence evolution of SARS-CoV-2 spike protein by using deep learning.
The pipeline, methods and codes here were modified from a flu-forecaster developed by Eric Ma. 
reference: https://github.com/ericmjl/flu-sequence-predictor

The SARS-CoV-2 sequence data come from the NCBI virus database. Sequences used here (May 1, 2020~ Dec 31, 2021) can be download via the link below. 
https://drive.google.com/file/d/1yuMTFq1k7kVaWoXslUJ2fD0oygG85qpJ/view?usp=sharing
Put the file "sequences_2020May_to_2021Dec.fasta" into the directory "data_covid19"

Some codes were rewritten so that they can be run on Google Colab.
