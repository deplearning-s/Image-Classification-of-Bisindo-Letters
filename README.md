# Image-Classification-of-Bisindo-Letters
Sign language is a language that uses body movements, such as hand and facial gestures. Each country has its own unique sign language. In Indonesia, there are two types: Bahasa Isyarat Indonesia (BISINDO) and Sistem Isyarat Bahasa Indonesia (SIBI). BISINDO is a practical and effective communication system for the deaf in Indonesia because it was developed by the deaf community themselves. This project aims to detect BISINDO letters through hand images.


## Method
![image](https://github.com/user-attachments/assets/d00ee06f-a57b-4f51-a8e0-fe5183562e32)

#### Dataset
The image data used in this project is sourced from Kaggle, containing hand images representing each letter. Each letter has 12 different images. In this project, the letters serve as the classes, and the images are the features.
[Kaggle Dataset Link](https://www.kaggle.com/datasets/achmadnoer/alfabet-bisindo/data)
#### Preprocessing
1.	RGB to BGR: Converts the entire image dataset from RGB format to BGR format.
2.	Resize: Resizes all images to 80x80 pixels for uniformity and efficient processing.
#### Split Data
The dataset was split into training and testing sets. Using test_size=0.3, 30% of the data was reserved for testing, while the remaining 70% was used for training the model.
#### Build Model
1.	HOG (Histogram of Oriented Gradients): HOG features were calculated for each image. These features capture information about the gradient direction and distribution in the image, which helps with recognition.
2.	GridSearchCV with SVM: GridSearchCV was used to find the best parameters for the Support Vector Machine (SVM) model by trying multiple configurations.
#### Best Model
The best parameters found by GridSearchCV were generated, and the accuracy was calculated by comparing the predicted results with the actual labels.
#### Prediction
Images were captured via camera, converted to a processable format, and predictions were made using the trained model.

## Result and Conclusion
Detection of BISINDO letters based on hand images using HOG and SVM with the best parameters: {'C': 10, 'gamma': 1, 'kernel': 'linear'} resulted in an accuracy of 77%. When tested with new images, the prediction results showed that the processed images using the best model could be accurately predicted.
