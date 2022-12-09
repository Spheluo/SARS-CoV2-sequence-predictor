# SARS-CoV-2 sequence predictor

COVID-19 is a serious global health problem and producing vaccines against evolved SARS-CoV-2 virus is an important issue. We thus aim to predict the sequence evolution of SARS-CoV-2 spike protein by using deep learning.
The pipeline, methods and codes here were modified from a [flu-forecaster](https://github.com/ericmjl/flu-sequence-predictor) developed by Eric Ma. 

The SARS-CoV-2 sequence data came from the [NCBI virus database](https://www.ncbi.nlm.nih.gov/labs/virus/vssi/#/virus?SeqType_s=Nucleotide&VirusLineage_ss=taxid:2697049&CollectionDate_dr=1950-01-01T00:00:00Z%20TO%20NOW&CreateDate_dt=1950-01-01T00:00:00Z%20TO%20NOW). 
Download the sequence file ["sequences_2020May_to_2021Dec.fasta"](https://drive.google.com/file/d/1yuMTFq1k7kVaWoXslUJ2fD0oygG85qpJ/view?usp=sharing) and put it in folder "data_covid19" before executing the code.

Some codes were rewritten so that they can be run on Google Colab.
