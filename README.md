# Introduction
This repository contains the NML script used in the Amazon SageMaker Training video prepared by DimensionalMechanics®, Inc.

This is an example exercise to run on Amazon SageMaker demonstrating the use of the NeoPulse® Modeling Language and the AI oracle availble in the NeoPulse® Framework, now available to run on both [CPU](https://aws.amazon.com/marketplace/pp/prodview-die5a2b34vjii) and [GPU](https://aws.amazon.com/marketplace/pp/prodview-7fngm7wimrfwy) instances.

# Tutorial Files
This tutorial contains the following files, the use of which will be explained in the directions below.

**README.md:** This file.

**LICENSE:** The license under which this code is made available.

**train.nml:** Features full use of the auto keyword to automatically generate the entire architecture for a model, as well as several hyper parameters.

# Requirements

To use this tutorial, you will need an [AWS account](https://aws.amazon.com/free/) with access to [Amazon SageMaker](https://aws.amazon.com/sagemaker/). You will need to have generated [AWS IAM credentials](https://aws.amazon.com/iam/) that allow programmatic access via the [AWS Command Line Interface](https://aws.amazon.com/cli/) or you will need upload the data to Amazon S3 using the console.

Documentation for how to use the NeoPulse® Framework Algorithm on AWS SageMaker from the AWS console is [available here.](https://docs.neopulse.ai/NP-SageMaker/)

# Instructions

First download the dataset described in the video. You can get it here:

https://www.kaggle.com/oumaimahourrane/imdb-reviews

Next, download the file **train.nml** from this repository by [clicking here](https://raw.githubusercontent.com/DimensionalMechanics/SageMakerVideo/master/train.nml) and copying and pasting the code.

<b>NOTE: if you copy/paste the code into a file, you MUST name that file train.nml for it to run using the SageMaker Algorithm.<b>

Now, make sure these two files are in the same directory.

Finally, upload the files to your Amazon S3 bucket using the AWS CLI. Instructions for installing and using the AWS CLI can be found here: https://aws.amazon.com/cli/

```bash
$ cd <path/to/directory/containing/train.nml>
$ aws s3 sync . s3://<your_bucket_name>
```

<b>NOTE: You can also use the AWS console to sync the directory as shown in the [documentation](https://docs.neopulse.ai/NP-SageMaker/).

Now you are ready to use Amazon SageMaker to train your model. Head to the SageMaker console, and follow the rest of the [instructions](https://docs.neopulse.ai/NP-SageMaker/).

# License
Tutorial materials are published under the MIT license. See LICENSE for terms for commercial, academic, and personal use.
