# Pneumonia-Detection-using-X-Ray-Images

## Introduction

Pneumonia is one of the leading causes of death among children and elderly people around the world. It is an infection caused by a virus, bacteria, or other germs, leading to inflammation in the lungs, which can be life-threatening if not diagnosed in time. Chest X-ray is a crucial method for pneumonia diagnosis worldwide. However, X-ray image analysis is a tedious and critical task for radiology experts. Using machine learning algorithms for pneumonia detection through X-ray images can significantly ease the diagnosis process.

### Objectives
1. To develop a pneumonia detection model using deep learning.
2. To validate the proposed detection technique on an existing dataset.
3. To develop a standalone web application for the pneumonia detection system using X-ray images.

## Preprocessing
The images are of varying length and width and are all resized to 224X224 , all black and whites converted to RGBs, normalized the pixels, segementation all so proves to be useful for the model in simplifying the image. Since, we have imbalanced data the most important preprocessing step is Image augmentation which I have done using *imgaug*.

## Training
For Training we have used pretrained VGG-16, frozen the initial layers, that learn abstract features and retrained the top most layers, to fit our data. We have trained the model for 5 epochs.

## Evaluation 
The model's performance is evaluated on test data and accuracy is not a trustworthy measure since the data is Imbalanced, so we use precision and recall instead.Since there is a trade-off between precision and recall , which means one increases at the cost of other , our main motive will be to have a high recall for our model and a relatively low but good precision as well.

## How to Run the Project

1. **Install Required Packages**:
   - Navigate to the root directory of the project.
   - Run the command:
     ```bash
     pip install -r requirements.txt
     ```

2. **Download and Prepare Dataset**:
   - Download the X-Ray image dataset from Kaggle: [Chest X-Ray Images (Pneumonia)](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia).
   - Extract the downloaded dataset.
   - Store the extracted folder in the `data` directory.

3. **Train the Model**:
   - Open the `notebook.ipynb` Jupyter notebook.
   - Run and compile the notebook to create the model required for the web application.

4. **Start the Backend Server**:
   - Run the command:
     ```bash
     python app.py
     ```

5. **Use the Web Application**:
   - Once the application starts running, go to [http://localhost:5000](http://localhost:5000).
   - Upload an X-ray image of your choice and let the model predict the result.
