# Covid-19 Strain Classification using Convolutional Neural Networks

This package implements a convolutional neural network to predict COVID lineage (Alpha, Beta, Delta, Omicron) based on the cDNA sequence of the S-glycoprotein.

1000 genome FASTA files from each of the four lineages (4000 total) were randomly sampled using [random_sampling.ipynb](https://github.com/alexchen1999/covid-19-sample-strain-classification/blob/main/random_sampling.ipynb) and downloaded from [NCBI Virus](https://www.ncbi.nlm.nih.gov/labs/virus/vssi/#/sars-cov-2) using this [ncbi-accession-download script](https://github.com/kblin/ncbi-acc-download). 

csv files of sample names can be found in the data folder.

The convolutional neural network was designed and trained following [Deep Learning DNA Sequence Classification by CNN](https://www.youtube.com/watch?v=pst4gdwaHEo) and by following the architecture outlined in the publication [DNA Sequence Classification by Convolutional Neural Network](https://www.researchgate.net/publication/301703031_DNA_Sequence_Classification_by_Convolutional_Neural_Network). The neural network is defined in [cnn.ipynb](https://github.com/alexchen1999/covid-19-sample-strain-classification/blob/main/cnn.ipynb).

## Results: 
Based on a 90/10% train/test split the highest performing model achieved a 98.9% train accuracy and 98.5% train accuracy using a kernel size of 8 and a learning rate of 0.01.

## Limitations and Future Considerations

Although a dropout layer was included in the architecture, increasing the sample size of the experiment and regularization are further improvements to reduce any potential overfitting. Additionally, k-fold cross validation could be used in place of a simple train-test split for better validation of results.
