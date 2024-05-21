# Overview

This ASL Detector is a cutting-edge AI-powered application that uses computer vision and deep learning to recognize and classify American Sign Language (ASL) characters in real-time. This application utilizes the device's camera to capture hand landmarks and coordinates, which are then processed by a deep learning model to identify the corresponding ASL character.

# Table of Contents

1. Introduction
2. Features
3. Installation
   Usage
   Model Training
   Contributing
   License
   Acknowledgements

# Features

- **Real-time ASL detection using the device's camera.**
- **Accurate classification of ASL characters using a deep learning model.**
- **Hand landmark tracking for precise gesture recognition.**
- **Support for a wide range of ASL characters and phrases.**
- **High accuracy and robustness in varying lighting conditions.**

# Requirements:

- OpenCV
- MediaPipe
- Pillow
- NumPy
- Pandas
- Seaborn
- Scikit-learn
- Matplotlib
- Tensorflow

> [!IMPORTANT]
> If you face an error during training from the line converting to the tflite model, use TensorFlow v2.16.1.

# Installation:

1. Clone the Repository:

```
git clone https://github.com/AkramOM606/American-Sign-Language-Detection.git
cd American-Sign-Language-Detection
```

3. Install Dependencies:

```
pip install -r requirements.txt
```

4. Run the Application:

```
python main.py
```

# Directory (Project Layout)

# Model Training
If you wish to train the model on your dataset, follow these steps:

1. Data Collection

   * Manual Key Points Data Capturing

Activate the manual key point saving mode by pressing "k", which will be indicated as “MODE: Logging Key Point”.<br>
If you press any uppercase letter from “A” to “Z”, the key points will be recorded and added to the “model/keypoint_classifier/keypoint.csv” file as demonstrated below.

<p align="center">
   <img src="https://github.com/AkramOM606/American-Sign-Language-Detection/assets/162604610/e0393472-f7c6-41f7-b5a6-3814dc4b7044">
<p/>

> [!NOTE]
> Each time you press the uppercase letter a single entry point is appended to keypoint.csv.

   * Automated Key Points Data Capturing

Activate the automatic key point saving mode by pressing "d", which will change the content of the camera window to an image of OM606.
<p align="center">
   <img src="https://github.com/AkramOM606/American-Sign-Language-Detection/assets/162604610/f4b11849-7fd9-423b-aee3-efa31f300159" width="70%"><br>
<p/>

> [!NOTE]
> You need to specify the dataset directory in ```app.py```

2. Training

Launch the Jupyter Notebook "[keypoint_classification.ipynb](keypoint_classification.ipynb)" and run the cells sequentially from the beginning to the end.<br>
If you wish to alter the number of classes in the training data, adjust the value of "NUM_CLASSES = 26" and make sure to update the labels in the "[keypoint_classifier_label.csv](model/keypoint_classifier/keypoint_classifier_label.csv)" file accordingly.

<p align="center>
   <img src="https://github.com/AkramOM606/American-Sign-Language-Detection/assets/162604610/0a4c4ce9-4afa-4852-a410-2b9bb280e4b8"><br>
<p/>

![confusion_matrix](https://github.com/AkramOM606/American-Sign-Language-Detection/assets/162604610/0a4c4ce9-4afa-4852-a410-2b9bb280e4b8)


# Usage ?

# Contributing

We welcome contributions to enhance this project! Feel free to:

1. Fork the repository.
2. Create a new branch for your improvements.
3. Make your changes and commit them.
4. Open a pull request to propose your contributions.
5. We'll review your pull request and provide feedback promptly.

# License

This project is licensed under the MIT License: https://opensource.org/licenses/MIT (see LICENSE.md for details).
