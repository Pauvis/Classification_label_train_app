# Classification_label_train_app
MATLAB application that was used to label, train and classify behaviour videos in Viskaitis et al. 2022

Recommended Matlab version: 2021a.
Tested versions 2018-2021.


Before running, from Matlab "Get More Apps" tab download and install:

Image Processing Toolbox
Deep Learning Toolbox
(optional) To use drop down network selection (in training tab) get: resnet18/resnet50/resnet101.
(optional) To use GPU for network training get: Parallel Computing Toolbox
Get network training functions from Google net example by typing into the matlab command line:
"openExample('nnet/TransferLearningUsingGoogLeNetExample')"

Add matlab path to the google net example by going to Home tab --> Set path --> Add with Subfolders.

Credit:

Training dataset balancing functions (https://uk.mathworks.com/matlabcentral/fileexchange/78020-oversampling-for-deep-learning-classification-example)
