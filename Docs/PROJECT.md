# Project Overview

## Table of Contents
- [Project Overview](#project-overview)
  - [Table of Contents](#table-of-contents)
  - [Project Description](#project-description)
    - [Our Partner](#our-partner)
    - [The Problem](#the-problem)
    - [The Solution](#the-solution)
  - [Types of Image Classification](#types-of-image-classification)
    - [1. Binary](#1-binary)
    - [2. Multi-class](#2-multi-class)
    - [3. Multi-label](#3-multi-label)
  - [Our Dataset](#our-dataset)
    - [Processing](#processing)
    - [Recordio Data Format](#recordio-data-format)
  - [Tools](#tools)
    - [Amazon S3](#amazon-s3)
    - [Amazon Sagemaker](#amazon-sagemaker)
    - [mxnet](#mxnet)
    - [Boto3](#boto3)
  - [In Hindsight](#in-hindsight)
    - [What Went Right?](#what-went-right)
    - [What Went Wrong?](#what-went-wrong)

## Project Description
### Our Partner
### The Problem
### The Solution

## Types of Image Classification

### 1. Binary

In binary classification either an image belongs to a single class or not. 

Example:
      
      Classes: Dog
      Prediction: Does the image represent a dog or not?

### 2. Multi-class

Multi-class image classification differs from binary classification because there are multiple classes and an image can belong to any a single class. 

Example:
  
      Classes: Dog, Cat, Tree
      Prediction: Which single class is represented in image?

### 3. Multi-label

In multi-label classification an image can belong to any number of classes. 

Example:

      Classes: Dog, Cat, Tree
      Prediction: What classes are represented in the image?

## Our Dataset
We created our data set with approximately 150,000 multi-label images.

### Processing
### Recordio Data Format

## Tools
### Amazon S3
### Amazon Sagemaker
### mxnet
### Boto3

## In Hindsight
### What Went Right?
### What Went Wrong?