# ImageClassification

Classifies images through a structured pipeline that begins with data preprocessing, including loading images, extracting features and combining these with raw pixel data to create a comprehensive feature set. The features are then standardized to ensure uniform scaling, followed by dimensionality reduction using Principal Component Analysis to retain essential information. Finally, classifier models are trained using the processed features from the training dataset and applied to predict labels for the test dataset.

 1. Data Preprocessing
 
Data Loading: The image datasets from the training and testing data are loaded and flattened into one-dimensional arrays
Feature Extraction of these images are done by : 
Gray Level Co-occurrence Matrix (GLCM): Textural features such as contrast, dissimilarity, homogeneity, ASM, energy, and correlation are extracted from grayscale representations of the images.
Edge Detection: Edges are identified using the Canny algorithm to capture boundary characteristics.
Corner Detection: Features are generated by applying the Harris corner detection algorithm.
Histogram of Oriented Gradients (HOG): HOG features capture shape and structural details of the image.
Then the extracted features are combined with the raw pixel data to create a more comprehensive representation of the images.
 
2. Feature Standardization
All features are then standardized using StandardScaler model to ensure uniform scaling and to enhance the performance of subsequent dimensionality reduction and machine learning models.
 
3. Dimensionality Reduction
Dimensionality is reduced using the PCA (principal component analysis) to three principal components, retaining essential variance while minimizing computational complexity. This step enhances model efficiency by focusing on the most informative aspects of the data.
 
4. Model Training
A classifier model is trained using the combined standardized features 
HistGradientBoostingClassifier model is chosen in the final solution as it gives a higher accuracy for the prediction

5. Prediction and Output
The trained model predicts labels for the test dataset using the processed feature set and gets saved in a CSV file called submit.csv 
 
