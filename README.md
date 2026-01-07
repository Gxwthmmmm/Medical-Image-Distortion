           24.06.2025
MEDICAL IMAGE DISTORTION:
The most common medical image distortions are blurry, contrast and noise distorted images.
Medical pictures that are distorted may influence the doctors’ clinical judgements resulting in missed diagnosis and other related inaccuracies.
Traditional medical imaging methods may include X-ray, computed tomography, magnetic resonance imaging (MRI), ultrasound imaging and radionuclide imaging.
Cardiology, pathology is well known medical imaging specialties.
Medical pictures created by medical imaging methods can vividly depict the interior structure of a specific organ or tissue in relation to a patient.
In the field of computer science image quality assessment (IQA)is a critical technique for determining the image’s quality.
IQA is subdivided into 2 components:
1.Subjective image quality assessment:
Prior research shows that Subjective IQA is the most trustworthy technique to assess the quality of a picture as the eventual users of most multimedia applications are human beings. Specifically in Subjective IQA the selected observers are needed to evaluate the quality of the provided pictures, within a defined duration. The previous researches have studied two primary categories are under Subjective IQA, including Single Stimulus Methods and Multi Stimulus Methods. In Single Stimulus Methods, just one incentive can be supplied to observers, i.e. one test picture. In Multi Stimulus Methods, two incentives can be provided to observers, which comprise a reference picture and corresponding test image.
Additionally, numerous researches are consistent with that Subjective IQA is a costly and time-consuming technique Indeed, the human observers are necessarily required in Subjective IQA makes the approach expensive; it takes time for observers to complete the assessment causes the technique time-consuming. Even so, Subjective IQA plays a vital part in IQA research, as the final consumers of it are completely human people.
2. Objective Image quality assessment:
Objective IQA is meant to deliver the numerical score values created by mathematical models, which should function similarly with human observers. Objective IQA may be classified into three categories, which are Full-Reference IQA (FR-IQA), Reduced-Reference IQA (RR-IQA), and No-Reference IQA (NR-IQA).
FR-IQA indicates reference pictures are accessible fully, which can be considered as ”high-quality” or ”distortion free”. Under FR-IQA, the algorithms firstly perceive the reference pictures and then assess the test images. 
RR-IQA implies reference pictures are partially accessible, midway between FR-IQA and NR-IQA. For example, there are some watermarks on the photos. There are three types of RR-IQA techniques, including the models of source pictures, the models of distortion of recorded images and the models of Human Visual System
NR-IQA indicates reference pictures are absent totally, meaning the image quality solely may be assessed by the corresponding test images. NR-IQA is matching most of the situations that transpired in actuality.
NR-IQA is more difficult than FR-IQA and RR-IQA, as the models need to consider numerous unexpected distortion types.Most commonly adopted NR-IQA models include Blind/Referenceless Image Spatial Quality Evaluator (BRISQUE) .and Naturalness Image Quality Evaluator (NIQE). Single Stimulus Methods and NR-IQA were chosen for Subjective IQA and Objective IQA, respectively.
METHODOLOGY:
Before generating a dataset, we must properly evaluate the following factors:
1.Image files: This refers particularly to the JPG/PNG images. However, using solely statistical data is unacceptable since it is difficult for human observers to judge the picture quality in Subjective IQA by reading a sequence of numbers.
2.Distortion free: The medical images used should be of the highest quality. The image is distortion-free. These images are then considered reference images and can be processed further to create various types of distortion images.
3.Currency: The medical images used should be recent, which implies they should not have been generated ”a long time” before.
4. Annotations: When a lesion arises in a medical image, we must at the very least know its precise position and size. Medical specialists’ instruction on how to assess lesions is critical.

SUBJECTIVE IMAGE QUALITY ASSESSMENT:
STAGE 1:
In this assessment a questionnaire is essential.
” The distortion” topic: personal background information and medical imaging related ques tions. We firstly ask numerous questions regarding position and experience, then ask them questions concerning the distortion according to their perspectives.
STAGE 2:
The observers shall evaluate the quality of the medical im age in the dataset during the formal evaluation of Subjective IQA. Considering a general image quality 4 questions can be asked:
1) Can you get useful information from this image? 
2) Do you think there is at least a lesion in this image? 
3) To what extent do you think the quality of this image is good enough for you to get the above answer? 
4) To what extent do you think the quality of this image is similar to the images you actually encountered during your work?

Q1 and Q2 are of YES/NO TYPE whereas the Q3 and Q4 are evaluated on a 5 point Linkert scale.
OBJECTIVE IMAGE QUALITY ASSESSMENT:
MATLAB image processing toolbox has been chosen.
1.Image quality score: All medical images in FYP Dataset have been scored using the relevant mathematical model. In every No Reference IQA, the lower score indicates the greater quality. The score can vary from 0 (the greatest quality) to 100 (the least quality).
2.Initial Check: For the scores provided by the model aforementioned, a first check is necessary. The goal of the initial check is to make sure the findings are logical. In the initial check, the quality of the original image should be better than deformed images. One of the probably acceptable conditions is the score of the original image is lower than the score of the distorted image for the identical original image set.
3. Confirm the ultimate result of objective IQA: We ex amine the outcomes across all mathematical models utilised and then pick the optimal performance model. The matching assessment scores are considered as the Objective IQA findings, which are used in analysis.

ANALYSIS:
Acc to analysis properties the results are divided into 3 subsections:
1.	Main results: Here the main and significant findings are demonstrated.
2.	Clinical Results In this section, the finding relevant to the clinical area (e.g. clinicians and radiologists) are demonstrated.
3.	Computational Results In this section, the findings relevant to the mathematical models and computing discipline are demonstrated.
Clinical and computational outcomes are equally essential, as are the results that address the research issues.
For the testing sample of Subjective IQA and Objective IQA, we first build a new testing dataset of 20 medical images, and then practise IQA using the medical images in this dataset. This new dataset comprises 8 original medical images, 7 medical images as blur distorted, 4 medical images as contrast distorted, and 1 medical image as noise distorted, which matches the proportion of distortion kinds in the   Dataset.


25.06.2025
https://pmc.ncbi.nlm.nih.gov/articles/PMC3653420/
https://www.sciencedirect.com/topics/engineering/image-distortion

https://ieeexplore.ieee.org/abstract/document/8746775
https://ieeexplore.ieee.org/document/10698529

National Library Of Medicine.
Geometric distortion: https://pmc.ncbi.nlm.nih.gov/articles/PMC7796777/

Which medical images show geometric distortion during analysis?
1.LUNGS
2.BRAIN
3. KIDNEY
4. BONES


26.06.2025

For a NR-IQA the following methods are used.
1.BRISQUE
2. NIQE
3. PIQE

1.	BRISQUE method is used where in BRISQUE uses a normalisation approach names Mean Subtracted Contrast Normalisation approach will be adopted.
I(i,j) = I(i,j) – nu(i,j)/sigma(I,j) + c
I(i,j): image intensity at the pixel.
nu(i,j): local mean field
sigma(i,j):local variance field
An image scored by BRISQUE will usually follow the below methodology: 
1. Extract NSS: Calculate MSCN coefficients 
2. Extract NSS: Calculate the pairwise products by using MSCN coefficients to find neighbourhood relationships (Horizontal, Vertical, Left Diagonal, Right Diagonal)
3. Calculate Feature Vectors: Fit the MSCN image to Generalized Gaussian Distribution (GGD), which can get the first two elements of feature vectors (size of 36-by-1)
4. Calculate Feature Vectors: Fit the pairwise products images to Asymmetric Generalized Gaussian Distribution (AGGD), which can get all other 16 elements of feature vectors
5. Repeat: Downsize another image as 50% as original one and repeat all same steps above to generate other 18 elements
6. Score: With training by datasets in Support Vector Machine, by the feature vectors calculated above, the ultimate score of BRISQUE can be generated for the image.

2.	NIQE method is different from BRISQUE, NIQE uses measurable deviations from statistical regularities observed in natural images to perceive the quality of images, without prior knowledge to the human-rated distorted images.

An image scored by NIQE will usually follow the below methodology 
 1. Extract NSS: Calculate MSCN coefficients
2. Patch Selection: Divide the image to P × P patches, calculate the average variance of the patches, and choose those patches which contain the richest information
3. Characterising Image Patches: Calculate the feature vectors by GGD and AGGD to get 18 elements, and to yield another 18 elements by downsizing with a factor of 2.
4. Score: Fit the 36 features to multivariate Gaussian (MVG) model and compare this with a natural MVG model, then the ultimate score of NIQE can be generated for the image.

3.	PIQE can perceive the image quality without any training data. To predict the quality of the image, PIQE extracts the local features and focus on the significant spatial regions perceived.
PIQE also adopts a 5point Linkert scale where the quality of the image can be evaluated.
An image scored by PIQE will usually follow the below methodology 
1. For each image pixel, MSCN coefficient will be computed
2. Divide the image into blocks with a size of 16-by-16.
3. According to the variance of the value computed in the Step 1 (MSCN coefficient), the high spatially active blocks will be confirmed.
4. According to the MSCN coefficients in each block, decide the distortion level of noise and blocking artifacts
5. According to a suitable threshold, the blocks will be classified as distorted blocks (further classified based on distorted types) and undistorted blocks
6. Among those distorted blocks classified in the previous step, "noticeableArtifactsMask" and "noiseMask" will be generated automatically as from distorted blocks with blocking artifacts and with noise respectively
7. The average score of all distorted blocks will be the ultimate score of PIQE for this image. The corresponding level of quality can be found on the aforementioned scale with this PIQE score.

Dataset link: https://github.com/beamandrew/medical-data


NOISE ISSUES IN DIFFERENT MEDICAL IMAGES AND METHODS TO REDUCE THEM:

1.	X-RAY: 
ISSUE: contrasting
SOLUTION: using several techniques like adjusting image parameters applying image processing techniques like histogram equalisation and contrast stretching.

2.	CT AND ECT (Computed tomography and emission computed tomography):
ISSUE: GAUSSIAN NOISE
SOLUTION: using linear filters like Gaussian and Wiener filters.

3.	MRI:
ISSUE: GAUSSIAN NOISE
SOLUTION: using linear filters like gaussian and wiener filters.

4.	ULTRASOUND:
ISSUE: GAUSSIAN and SPECKLE NOISE
Solution: using linear filter for gaussian and spatial filters for speckle noise.

For a distorted image to be corrected the following image processing techniques can be used
For errors such as Contrasting in X-RAY 
histogram equalisation and contrast stretching can be used to adjust the intensity distribution if image by enhancing the contrast either by increasing or decreasing the contrast.
For errors such as Gaussian noise, speckle noise
Spatial filtering can be used to modify the image by altering the values of pixels based on their spatial relationship with the neighbouring pixels.

Operations on random medical images:
1.	Adding gaussian noise
2.	Adding motion blur
3.	Applying radial/ lens distortion
4.	Adding salt and pepper noise (simulating random black and white pixels.)
5.	Geometric transformations/Affine transformation


Dataset creation including various body organs 
1.	Abdomen(kidney)
2.	Brain
3.	Chest
4.	Bones(hand)




