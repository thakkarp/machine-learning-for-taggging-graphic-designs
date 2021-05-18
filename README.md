# Machine Learning For Tagging Graphic Designs


## Table of contents
  - [Project Description](#project-description)
  - [Getting Started](#getting-started)
  - [Usage](#usage)
    - [Training and Tuning](#training-and-tuning)
    - [Deploying](#deploying)
  - [Additional Resources](#-additional-resources)


## Project Description

In this project we train and deploy a machine learning model to automatically predict the tags associated with a given image. 

Please read the [project overview](Docs/PROJECT.md) before continuing. It contains detailed information about: the purpose of our project, the creation of our dataset, the tools we used to accomplish the goal and more.

## Getting Started
  Follow the [set-up instructions](Docs/SETUP.md). After completing these steps you should have the following:
  1. An AWS account
  2. An S3 Bucket named *sagemaker-multi-label-data* with the following structure:
      
          sagemaker-multi-label-data/
                ic-multi-label/
                        training/
                                train.rec
                        validation/
                                val.rec
                        output/
  3. A notebook instance in sagemaker with three files.

## Usage

Now that you have everything in place you are ready to train, or tune the model. When you have a model that you're happy with you will be able to deploy it and see it in action.

### Training and Tuning

Two of the files that you previously uploaded to your notebook instance in sagemaker can be used in different ways to train new models.

- [train.ipynb]() can be used to train a single model. The training will use a set hyper-parameters defined in the file itself. These hyper-parameters can be manually adjusted to increase the model accuracy. To use this method open train.ipynb in your notebook instance and follow the instructions.
- [tune.ipynb]() utilizes the sagemaker hyper-parameter tuning service to automatically adjust hyper-parameters. In this file you can specify ranges of values for certain hyper-parameters and sagemaker will run multiple training jobs with different hyper-parameters in order to find what values produce the best model. To use this method open tune.ipynb in your notebook instance and follow the instructions.


### Deploying

To deploy a trained model to an endpoint open deploy.ipynb in the notebook instance and follow the instructions.

## Additional Resources


