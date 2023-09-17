# Galaxy-Classification-SDSS

The night sky is host to numerous celestial bodies. The Sloan Digital Sky Survey (SDSS) has searched about one-third of the sky and found around one billion objects, almost three million of which are galaxies. Having a software system to check photometric data and make a prediction can save time for astronomers and researchers in their efforts to classify galaxies. This analysis will determine if it is possible to use a DNN to predict a galaxy subclass using imaging data from the Sloan Digital Sky Survey. The hypothesis for this analysis is: A DNN classifier for galaxy subclass prediction can be constructed from the research dataset with a model accuracy greater than 70%.

The data needed for this analysis is contained in the SDSS image photometry and is limited to 100,000 rows of photometric image data and galaxy subclass data (Almeida et al., 2023). The data was obtained using SQL and saved as a csv file. The data for this analysis was then prepared using a Jupyter notebook in python. One disadvantage of python is slower performance compared to compiled languages like C or C++. The data model was developed using the python language for a couple of reasons. First advantage: python is known for its concise and clear code (Moteria, 2020). Second, python has the keras and tensorflow libraries that have many features to aid in the development of neural networks.

After the data was obtained, the cleaning process consisted of checking for duplicate values, null values, and outliers. Next the data was normalized, and some visualizations were made. The visualizations included boxplots, histograms, and distribution plots. The plots help show the relationship between some variables and determine if there are patterns or trends that can be shown. Next the model data was split using an 80/20 training/testing data set. After that, the DNN model was setup using tensorflow. It has six layers and 19,073 total parameters. In the DNN model each layer applies weights and biases to the data that are learned in the training process. This process is what allows the model developed to accurately detect the subclass.

The model was compiled using Binary Cross-Entropy as the loss function and Adam (Adaptive Moment Estimation) as the optimizer. The model developed uses accuracy as the metric to evaluate how well it classifies the galaxy subclass.

The model developed appears to perform well; it is nearing optimal as noted by the loss graph descending to near zero. Also, the model is not overfitting since in the loss graph both values are decreasing to near zero.

The trained model has an accuracy of 88.71%. Since the data set is imbalanced, the F1 score was also calculated, 0.884. The F1 score is the harmonic mean of precision and recall and is a good metric for use on imbalanced data sets like this one (Czakon, 2019).

The model developed was able to detect galaxy subclass with a high accuracy and F1 score.

References:
Almeida, A., Anderson, S. F., Argudo-Fernández, M., Badenes, C., Barger, K., Barrera-Ballesteros, J. K., Bender, C. F., Benitez, E., Besser, F., Bizyaev, D., Blanton, M. R., Bochanski, J., Bovy, J., Brandt, W. N., Brownstein, J. R., Buchner, J., Bulbul, E., Burchett, J. N., Cano Díaz, M., & Carlberg, J. K. (2023, January 1). The Eighteenth Data Release of the Sloan Digital Sky Surveys: Targeting and First Spectra from SDSS-V. NASA ADS. https://doi.org/10.48550/arXiv.2301.07688.

Czakon, J. (2019, November 4). F1 Score vs ROC AUC vs Accuracy vs PR AUC: Which Evaluation Metric Should You Choose? Neptune.ai. https://neptune.ai/blog/f1-score-accuracy-roc-auc-pr-auc

Moteria, D. (2020, February 18). Python vs R: Which Language to Choose for Deep Learning? Data Science Blog. https://data-science-blog.com/blog/2020/02/18/python-vs-r-which-language-to-choose-for-deep-learning/.


Copyright 2023 by Bryan Cimo see LICENSE.txt for terms.