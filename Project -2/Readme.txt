This is the Statoil/C-Core Iceberg Classifier Challenge from Kaggle competition.
You Can get the data from the competition if you sign up.

Data:

We are provided with 3 files viz. train.json, test.json and sample_submission
files. All images are 75 X 75 with two bands as mentioned above and are in list
form. In train data we are provided with 5 columns viz id - the ID of image,
band_1 and band_2 - the flattened image data.
Each band has 75 X 75 values in list so list has 5625 values, inc_angle - incident
angle at which image was taken which is explained in the above given
background and is_iceberg - classifies if it is iceberg or not. 0 for not an iceberg
and 1 for an iceberg.
Band_1 and band_2 are float numbers with unit being dB. The signals are
characterized by polarization's at particular incident angle.
There are 1604 rows in train data and 8424 rows with first 4 columns of train
data in test data.
The data is extracted using json and pandas library and converted into a
dataframe. By simply using 'dataframe.info()' it cannot be identified if there are
missing or na values in the dataset. So by seeing the full dataset it can be
observed that the na values in inc_angle column.
In is_iceberg column of train data there are 851 values of not an iceberg and 753
values of the image as an iceberg.
All the values in the ID column are unique values and there are some common
values in the inc_angle column.
Since it is binary classification in images, CNN is the basic model as the
algorithm.
The training data is of just 187 MB with 1604 data points whereas test data is of
1.41 GB with 8424 data points.

The files are Jupyter notebooks:
"EE 258 project 2 new 2.ipynb" is the best model and its submission file is attached.
"Project 2 new - Copy (2).ipynb" is the basic model in which hyperparameters were changes 
and results were observed.
