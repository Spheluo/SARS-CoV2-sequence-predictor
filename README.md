# SARS-CoV-2 sequence predictor

COVID-19 is a serious global health problem and producing vaccines against evolved SARS-CoV-2 virus is an important issue. We thus aim to predict the sequence evolution of SARS-CoV-2 spike protein by using deep learning.
The pipeline, methods and codes here were modified from a [flu-forecaster](https://github.com/ericmjl/flu-sequence-predictor) developed by [Eric Ma](https://github.com/ericmjl). Some codes were partly rewritten so that they can be run on Google Colab.

## Data

The SARS-CoV-2 sequence data came from the [NCBI virus database](https://www.ncbi.nlm.nih.gov/labs/virus/vssi/#/virus?SeqType_s=Nucleotide&VirusLineage_ss=taxid:2697049&CollectionDate_dr=1950-01-01T00:00:00Z%20TO%20NOW&CreateDate_dt=1950-01-01T00:00:00Z%20TO%20NOW)(IRD). Search parameters were as follows:

- Species: Severe acute respiratory syndrome coronavirus 2
- Sequence Length: 1273
- Nucleotide completeness: complete
- Protein: Surface glycoprotein
- Colletion date: 2020/5/1~2021/12/31
- Graphic regions: North America
- isolation source: oronasopharynx
- Host: Homo (humans)

Or you can download the sequence file ["sequences_2020May_to_2021Dec.fasta"](https://drive.google.com/file/d/1yuMTFq1k7kVaWoXslUJ2fD0oygG85qpJ/view?usp=sharing) and put it in folder "data_covid19" before executing the code.

## Structure 

1. Use variational autoencoders, a deep learning method, to learn a latent manifold on which sequence evolution is taking place. 
1. Simultaneously construct a genotype network of SARS-CoV-2 evolution.
    1. Nodes: SARS-CoV-2 protein sequences.
    1. Edges: Sequences differ by one amino acid.
1. Sanity checks:
    1. Plot edit distance between any two random pairs of protein sequences against their manifold distance. There should be a linear relationship between the two.
1. Validation:
    1. MVP validation will be done by doing one round of "back testing" - we hold out data from 2021/8/1 to 2021/12/31, and predict whether data shows up or not.
