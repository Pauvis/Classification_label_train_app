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

Add Matlab path to the Google net example folder by going to Home tab --> Set path --> Add with Subfolders.

(Optional) Recommend to pre-process  videos in Handbrake to compress, crop and/or re-index frames: https://handbrake.fr

General workflow:

1)Inspect videos and clearly define classes. Make sure overlaps between classes are resolved in unambiguous manner: e.g. if example contains features of 2 or more classes, what is the dominant class.

2)Decide how much frame overlap is needed to accurately identify a behaviour if needed (set that as a number of prior and subsequent frames to be included in the frame RGB image).

3)Create sub-folders in the work directory with class names.

4)Label as many and as diverse non-ambiguous examples for each class as practically possible. Use key-bindings to speed up frame inspection and labelling. Use pixel difference to identify distinct aspects of the video.

5)Once enough frames are labelled train a network. Import a custom network or use one of the suggested resnet networks form the dropdown menu (make sure Matlab has those networks installed). Save trained network (avoid special characters in names).

6)Assess your trained network against human scorers.

7)Train videos in batch mode or only selected frames. Loading videos into memory is recommended to speed up batch labelling greatly. 

Credit:

Training dataset balancing functions (https://uk.mathworks.com/matlabcentral/fileexchange/78020-oversampling-for-deep-learning-classification-example)
