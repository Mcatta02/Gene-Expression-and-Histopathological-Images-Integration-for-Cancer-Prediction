# Gene-Expression-and-Histopathological-Images-Integration-for-Cancer-Prediction

This repository contains various scripts and tools used in the analysis and processing of gene expression and image data for the thesis. Below is an overview of each file and its functionality:

1. Autoencoder.ipynb:
   This file contains the structure of the autoencoder model and is responsible for extracting bottleneck features from the input images.

2. Correlation analysis.ipynb:
   This script takes gene expression data and the bottleneck features extracted by the autoencoder as input. It identifies genes that exhibit a high correlation with the autoencoder features.

3. CutTiles.ipynb:
   This file is used to cut large images into smaller tiles of size 512x512 pixels. It excludes tiles with too much white space and saves the valid tiles into a new directory.

4. Dataset comparison.ipynb:
   This script processes input images through the autoencoder and calculates the Mean Squared Error (MSE), Structural Similarity Index Measure (SSIM), and Peak Signal-to-Noise Ratio (PSNR) metrics to evaluate image reconstruction quality.

5. Gene expression Case ID name.ipynb:
   This script renames the columns containing gene expression data to their unique case IDs using a TSV connector.

6. Graphs.ipynb:
   This file generates graphs for the thesis, illustrating the performance metrics (MSE, SSIM, PSNR) and the impact of skip layers on the autoencoder's performance.

7. Remove useless columns and rows.ipynb:
   This script removes columns from the autoencoder bottleneck layer that have more than half of their values as zeros, cleaning the dataset for better analysis.
   Does the same for the rows where more than half the values are smaller than zeros in the gene expression data.

8. Spearman Rank Final.ipynb:
   This script computes the Spearman rank correlation on the available tiles connected to patients, saving the correlations greater than 0.6 for further analysis.

9. standard deviation.ipynb:
   This file calculates the standard deviation for each dataset and each column in the autoencoder bottleneck layer.

10. TSVmerge.ipynb:
    This script merges multiple TSV files into a single file.

11. TXT to CSV.ipynb:
    This script converts text files (TXT) to comma-separated values files (CSV).

12. 11_model.pth:
    Contains the pretrained weights for the autoencoder model used in this project.
    The weights come from the work of Kata Kriszta Keresztesi.
    
