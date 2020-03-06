
# project-ml-microservice-kubernete
Created for Udacity Nanodegree

[![CircleCI](https://circleci.com/gh/Adrian1690/project-ml-microservice-kubernete.svg?style=svg)](https://circleci.com/gh/Adrian1690/project-ml-microservice-kubernete)

## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

---

## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl

### Explanation files 

* .circleci: Folder the contents circleci config file
* model_data: Folder the contents files to train the algorithm
* output_txt_files: Folder the contents outputs from docker and kubernetes.
* app.py: Main file to create the host
* Dockerfile: File contents docker build configuration
* make_predictions.sh: Contens call to host to get predictions
* Makefile: The Makefile includes instructions on environment setup and lint tests
* requirements.txt: List of dependencies needed
* run_docker: Contains commands to build, list and run docker image.
* run_kubernetes: Contains commands to run the Docker Hub container with kubernetes, list kubernetes pods and forward the container port to a host
* upload_docker.sh: Contains commands to push the build image to Docker Hub. 