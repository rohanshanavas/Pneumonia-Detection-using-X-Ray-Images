# Pneumonia-Detection-using-X-Ray-Images

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
