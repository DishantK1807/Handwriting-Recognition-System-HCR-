# Handwriting-Recognition-System-HCR-
+author  : Dishant Khanna  : dishant.khanna1807@gmail.com, this folder contains m-files i created for extracting features from a image containing a SINGLE
character. The code converts the image to binary and extracts features from it. There is a pdf explaining
the algorithm for feature extraction. The feature vector so extracted can be used for training pattern recognition 
engines which have learning capabilities like Neural Networks and Support Vector Machines. I have used feature vectors
so generated to train neural networks and thereby recognise characters. Soon I will be uploading them too.

READ THE PDF INCLUDED FOR THE EXPLANATION OF THE ALGORITHM
--------------------------------------------------------------------------------------------------------------
There are two functions for feature extraction.

feature_extractor_2d.m----

this m-file divides the image first into 3 sub images by dividing it vertically in a 1x3 fashion. It then extracts the features 
for each individual image(referred as zone). Then it again divides the orginal image in a 3x1 fashion and extracts features for each region.
Catenates this into a single vector.
---------------------------------------------------------------------------------------------------------------------
feature_extractor.m---

this m-file divides the image in a 3x3 fashion and extracts features for each zone.
---------------------------------------------------------------------------------------------------------------------

FOR MY PURPOSE, I USED BOTH FUNCTIONS AND CATENATED THE RESULTANT VECTORS TO FORM A SINGLE FEATURE VECTOR
-----------------------------------------------------------------------------------------------------------------------


NOTE THAT FOR FEATURE EXTRACTION, THE IMAGE HAS TO BE BINARIZED. THE CODE INSIDE THE M-FILES HANDLES THIS, BUT THE MOST IMPORTANT 

POINT TO NOTE THAT IS THE CODE ASSUMES THAT CHARACTER  SKELETON IS MADE UP OF ONES AND BACKGROUND PIXELS OF ZEROS AFTER BINARIZATION.

SO FOR FEATURE EXTRACTION, IMAGES WITH WHITE LETTERS ON A BLACK BACKGROUND CAN BE USED. BUT THE STANDARD CASE IS THE REVERSE. I DID IT THE STANDARD

WAY AND COMPLEMENTED THE IMAGE TO GET IT THE WAY I WANTED IT.

---------------------------------------------------------------------------------------------------------------------------

Load the mat file letter_skel.mat, it includes samples of training set, i used for feature extraction.

>>load letter_skel.mat

%after this try the command 'who', you can see the variables.
>>imshow(matA1);
%matA1 is one among the variables.
------------------------------------------------------------------------------------------------------------------------------

for any queries mail me at: dishant.khanna1807@gmail.com
