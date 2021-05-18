# Setup Instructions

This guide will take you through the steps required to begin training the model. 

**Table of Contents**
- [Setup Instructions](#setup-instructions)
  - [1. Download the dataset](#1-download-the-dataset)
    - [About the Data](#about-the-data)
  - [2. Log in to AWS](#2-log-in-to-aws)
    - [Have an account?](#have-an-account)
    - [Don't have an account?](#dont-have-an-account)
  - [3. Upload the dataset](#3-upload-the-dataset)
    - [Create a Bucket](#create-a-bucket)
    - [Upload Files to Bucket](#upload-files-to-bucket)
  - [4. Create an instance in sagemaker](#4-create-an-instance-in-sagemaker)
    - [Create a new Notebook Instance](#create-a-new-notebook-instance)

## 1. Download the dataset

Download the dataset [here]().

### About the Data

For more information about the format and creation of our dataset in see our [project overview](PROJECT.md).

## 2. Log in to AWS

### Have an account?
- [Sign in](https://signin.aws.amazon.com)

### Don't have an account?

- Follow [these steps](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/) to create one. 

- **Note:** It may take up to 24 hours for a new account to activate.

After you sign in to your AWS account you will be brought to the AWS management console. From here you can access a ton of different Amazon services. The first service we will need is Amazon Simple Storage aka. S3. To learn more about S3 see the [official S3 documentation](https://docs.aws.amazon.com/s3/index.html).

## 3. Upload the dataset

### Create a Bucket
- From the AWS console select:
        
        services->S3

- Select the button labeled:
        
        Create bucket
- Name the bucket *sagemaker-multi-label-data*
- Choose an AWS region and be sure to remember it
- Scroll to the bottom and select the button labeled: 
  
        Create bucket

### Upload Files to Bucket
- Navigate into the bucket you created and create a folder named: *ic-multi-label*
- Navigate into *ic-multi-label* create three folders named:
  - *training* 
  - *validation*
  - *output*
- Navigate into the training folder and select:
        
        Upload
  - Find the **train.rec** file and wait until it uploads
- Navigate into the validation folder and select:

        Upload
  -  Find the **val.rec** file and wait until it uploads

You should now have an S3 bucket named *multi-label-data* with the following structure:

        sagemaker-multi-label-data/
                ic-multi-label/
                        training/
                                train.rec
                        validation/
                                val.rec
                        output/
                        

## 4. Create an instance in sagemaker
With the training and validation data in the right spot you are now ready to create a sagemaker instance. Within this instance you will be able to train and deploy the model. See the [official Sagemaker documentation](https://docs.aws.amazon.com/sagemaker/index.html) to learn more about the service.

### Create a new Notebook Instance

- From the AWS console select: 
        
        Services->Amazon Sagemaker

- On the sidebar select: 
        
        Notebook->Notebook Instances

- Select the orange button labeled: 

        Create notebook instance
- Name the instance whatever you want.
- Set the instance type to 
    
        ml.t2.medium
  - **Note**: Price varies based on the instance type see [Sagemaker Pricing](https://aws.amazon.com/sagemaker/pricing/)
- Under IAM role select: 
        
        create new role->create role 
    - Or if you have an existing role select it.
  
- Select: 
        
        Create Notebook Instance
    
    - Wait for the instance to be created.
  
- When the instance is ready select:
  
        start 
  - Wait until it says **open jupyter**
- Select: 
        
        open jupyter 
        
  - You will be redirected to the notebook instance
- Inside the notebook select:
        
        upload
    
    - Upload the files train.ipynb tune.ipynb and deploy.ipynb to the notebook instance.
  
**NOTE**: make sure you stop the instance when you aren't using it, or you will be charged for the time it sits idle.
  
Now you should be ready to go! Head back to [README.md](README.md) to see whats next.
