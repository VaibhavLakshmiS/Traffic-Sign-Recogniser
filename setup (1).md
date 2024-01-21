
# Setup Instructions for Running the Traffic Sign Classification Code - ABTV

## Prerequisites
- Google Colab or a similar Jupyter Notebook environment
- A Kaggle account and API token (kaggle.json)

## Steps

### 1. Setting Up Kaggle API
- Open a new notebook in Google Colab.
- Install the Kaggle package using the command:
  ```
  !pip install kaggle
  ```
- Upload your `kaggle.json` file containing your API credentials. 
  ```
  from google.colab import files
  uploaded = files.upload() # This will prompt you to upload the kaggle.json file
  ```

### 2. Configuring Kaggle API Access
- Setup the Kaggle API access by running the following commands:
  ```
  !mkdir -p ~/.kaggle
  !cp kaggle.json ~/.kaggle/
  !chmod 600 ~/.kaggle/kaggle.json
  ```

### 3. Downloading the Dataset
- Download the dataset from Kaggle using:
  ```
  !kaggle competitions download -c ds3-datathon-traffic-signs
  ```
- Unzip the downloaded dataset:
  ```
  !unzip -q ds3-datathon-traffic-signs.zip -d /content/traffic_signs
  ```

### 4. Installing Required Libraries
- Ensure the following Python libraries are installed (these are usually pre-installed in Colab):
  - numpy
  - pandas
  - matplotlib
  - PIL (Pillow)
  - scikit-learn
  - tensorflow

### 5. Running the Code
- Copy the provided Python code into subsequent cells in the notebook.
- Run each cell in sequence.

### 6. Model Training
- The code will train a CNN model on the traffic sign dataset. Training progress will be displayed.
- The number of epochs and batch size can be adjusted as per your requirement.

### 7. Saving the Model
- After training, the model will be saved as `improved_traffic_classifier.h5`.
- This file can be downloaded from the Colab environment .

## Notes
- The training time will depend on the size of the dataset and the computing resources of your environment.
