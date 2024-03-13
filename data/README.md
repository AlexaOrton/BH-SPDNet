Data for training and validating both SPDNet and U-SPDNet models. 
The data in the U-SPDNet directories are in .npy format and so need to be processed into .mat format.
This may be acheived by the .ipynb file for both the JSE Top 60 and synthetic data.

INITIAL EXPERIMENTATION
The original JSE Top 60 data is processed and augmented to comprise 18,000 correlation matrices. 
These matrices are stored across three classes in the SPDNet initial experiment sub-directory (6000 matrices per class) - 'stressed', 'normal' and 'rally' - according to the Sharpe Ratio.
The Sharpe Ratio is calculated on the contemporaneous 252-day moving window and divided amidst the three classes according to boundaries SR < -0.5; -0.5 < SR < 2; SR > 2.
18,000 matrices are constructed synthetically using the Yelibi and Gebbie (2021) adaptation of Tuminello's (2008) approach.

These .npy files are randomly allocated to 'train' and 'val' directories containing classes 1, 2, 3, corresponding to 'stressed', 'normal' and 'rally' classes.
This division is 75-25%.
These need to be converted into .mat format to be used by the Matlab scripts for U-SPDNet learning.

BACKTESTING
The original JSE Top 60 data are purged and embargoed (Lopez de Prado, 2021). 
The training data are augmented to 18,000 matrices, as in the initial experimentation, whilst the validation, or test, data are left in chronologocal order.
These data are constructed in the .ipynb file executing the SPDNet backtested regime-dependent portfolio optimisation.
In the case of the U-SPDNet, these data are allocated to sub-directories within the 'train' and 'val' folders according to the same labelling as above: 1, 2 and 3.


