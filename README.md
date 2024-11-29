# Blood-Cell-Segmentation-with-OpenCV-and-SVM

# Project Description
This project aims to classify white blood cells in a microscopic image using an SVM (Support Vector Machine) classifier.
By applying color-based segmentation with HSV color space, we identify white blood cells (highlighted in purple) and classify
pixels as either white blood cells or the background. This approach leverages machine learning to differentiate between areas of interest based on color properties.

#Steps Performed
Image Upload and Preprocessing

Uploaded a microscopic image using Google Colab's file upload functionality.
The image was loaded into the project using OpenCV and converted to the HSV color space for better color segmentation.
Color Segmentation

Defined a range of HSV values to identify purple areas, corresponding to white blood cells.
Created a binary mask where pixels within the purple range were assigned the label 1 (white blood cell) and others were labeled 0 (background).
Data Preparation

Flattened the HSV image into a 2D array where each pixel is represented by its HSV values.
Flattened the binary mask to create a label array.
Split the data into training and testing sets using a 70/30 split.
Training the SVM Classifier

Used a linear kernel SVM classifier from scikit-learn to train on the HSV pixel data and corresponding labels.
Trained the model to differentiate between white blood cells and the background.
Model Evaluation

Predicted the labels for the test data and calculated the accuracy score of the classifier.
Generating the Result Mask

Applied the trained SVM model to classify all pixels in the image.
Created a mask of detected white blood cells and overlaid it onto the original image to highlight the areas of interest.
Visualization

Used Matplotlib to display the original image alongside the processed image with highlighted white blood cells.


#Requirements
To run this project, ensure the following dependencies are installed:

Python 3.x
OpenCV (cv2)
scikit-learn
NumPy
Matplotlib

Install the required libraries using:
pip install opencv-python scikit-learn numpy matplotlib
