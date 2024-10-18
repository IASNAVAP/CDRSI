Change Detection in Remote Sensing Images
This project implements a change detection system using machine learning techniques integrated with a Django web application. The system processes two remote sensing images taken at different times from the same geographical area and highlights areas where changes have occurred.

Table of Contents
Introduction
Features
Requirements
Installation
Usage
Project Structure
Model Information
Screenshots

Introduction
Change detection in remote sensing images is crucial for monitoring environmental changes, urban expansion, disaster management, and agricultural analysis. This project uses a Convolutional Neural Network (CNN) model to detect changes between two images taken from satellites or aerial views.

The application has a user-friendly interface developed with Django, where users can upload two images and the model processes these images to output the difference or changes detected.

Features
Upload and process two images (before and after) for change detection.
Machine learning model (.h5) for image processing.
Display of the difference image highlighting changes.
Django-based web interface for user interaction.

Requirements
Python Dependencies
Python 3.x
Django 3.x+
TensorFlow or Keras (for loading the ML model)
OpenCV (for image processing)
Pillow (for handling image formats)
Git LFS (for managing large model files)
You can install the required Python packages by running:

bash
pip install -r requirements.txt

Installation
Clone the Repository:

bash

git clone https://github.com/username/CDRSI.git
cd CDRSI

Set up the Virtual Environment: Create and activate a virtual environment (optional but recommended):

bash

python -m venv myenv
source myenv/bin/activate  # On Windows, use `myenv\Scripts\activate`

Install the Dependencies:

bash

pip install -r requirements.txt

Set up the Database: Run migrations to set up the database:

bash
Copy code
python manage.py migrate
Load the Pre-trained Model: Ensure the pre-trained model (final_cnn_model2.h5) is present in the correct directory. If it’s tracked using Git LFS, install Git LFS and pull the file:

Run the Development Server:

bash

python manage.py runserver

Access the Web Application: Open a web browser and go to http://127.0.0.1:8000/ to access the application.

Usage
Upload two remote sensing images.
Click on "Process" to detect changes between the images.
The output will display the difference image highlighting the detected changes.

Model Details:
Model File: final_cnn_model2.h5
Architecture: CNN with layers for feature extraction and comparison between the two input images.
Input: Two images (before and after) of the same geographical area.
Output: A difference image highlighting areas of change.
Screenshots
