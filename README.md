![status/exprimental](https://img.shields.io/badge/STATUS-EXPERIMENTAL-%237C3AED?style=flat-square)
###### TSKLABS • AWS
#  AWS Codecommit Trigger Pipeline <!-- omit in toc -->

AWS Serverless Application that triggers an AWS Codepipeline pipeline on CodeCommit Repository State Change.

<br>

## Contents <!-- omit in toc -->

- [1. Overview](#1-overview)
- [2. Quickstart](#2-quickstart)
  - [2.1. Prerequisites](#21-prerequisites)
  - [2.1. Deploy](#21-deploy)
  - [2.2. Usage](#22-usage)
  - [2.3. Demo](#23-demo)
  - [2.4. Uninstall / Unsubscribe](#24-uninstall--unsubscribe)
- [3. Learning](#3-learning)
  - [3.1. How-tos](#31-how-tos)
  - [3.2. Tutorials](#32-tutorials)
  - [3.3. Resources](#33-resources)
- [4. Roadmap](#4-roadmap)
  - [4.1. Now](#41-now)
  - [4.2. Next](#42-next)
  - [4.3. Later](#43-later)
- [5. References](#5-references)
  - [5.1. Concepts](#51-concepts)
  - [5.2. Motivation](#52-motivation)
  - [5.3. Testing](#53-testing)
  - [5.4. FAQ](#54-faq)
- [6. Contributing](#6-contributing)
  - [6.1. Instructions](#61-instructions)
  - [6.3. Build](#63-build)
  - [6.4. Package](#64-package)
  - [6.4. Deliver](#64-deliver)
  - [6.4. Deploy](#64-deploy)
  - [6.4. Delete](#64-delete)
  - [6.2. Styleguide](#62-styleguide)
- [7. Feedback \& Support](#7-feedback--support)
  - [7.1. Feedback](#71-feedback)
  - [7.2. Help](#72-help)
- [8. Maintainer(s)](#8-maintainers)
- [9. License](#9-license)

<br>

## 1. Overview

**AWS Codecommit Trigger Pipeline** is an  AWS Serverless Application which is configured to trigger an AWS Codepipeline pipeline as a result of an AWS CodeCommit Repository State Change.

It supports the following AWS Codecommit change events:

* [ReferenceCreated](https://docs.aws.amazon.com/codecommit/latest/userguide/monitoring-events.html#referenceCreated)
* [ReferenceUpdated](https://docs.aws.amazon.com/codecommit/latest/userguide/monitoring-events.html#referenceUpdated)
* [ReferenceDeleted](https://docs.aws.amazon.com/codecommit/latest/userguide/monitoring-events.html#referenceDeleted)
* [UnreferencedMergeCommitCreated](https://docs.aws.amazon.com/codecommit/latest/userguide/monitoring-events.html#unreferencedMergeCommitCreated)

<br>

## 2. Quickstart

### 2.1. Prerequisites

For the application to work, you need:

* An AWS Account to deploy the application
* An AWS IAM Role with the necessary permissions to trigger the targetted AWS Codepipeline pipeline.

> [!NOTE]
> The built-ins role and permissions provided is, wanted, permissive to ease integration; but make sure to provide another one the the right set of permissions following the Least Priviledge principle.


### 2.1. Deploy

Before using this application as a trigger for codepipeline, you must deploy the application to the AWS Serverless Application Repository within your AWS Account.

> [!NOTE]
> Replace `<tag-version>` by the release tag version you want to deploy. For instance `tag-version` should be replaced by `A.B.C` if you want to deploy the version `A.B.C`.

<br>

**Step 1: Download release archive**

Go to [Releases](/releases) and download the assets matching the version you want to deploy. 
Eg:  `aws-codecommit-trigger-pipeline-v<tag-version>.zip`

**Step 2: Extract archive**

```sh
unzip aws-codecommit-trigger-pipeline-vA.B.C.zip
cd $_
```


**Step 3: Authenticate to your AWS Account**

Use `aws configure` to provide the AWS Credentials to the AWS CLI.

**Step 4: Deploy the application w/ AWS SAM**

```sh
sam deploy
```


### 2.2. Usage

< Provide instructions on how to use the component >

< Includes releavant commands and code snippets >

< Link 2 to 3 main use cases from 'learning/how-tos or tutorials' to help users understant how to use the component >


### 2.3. Demo

< Add a short video to demo how it works in a real scenario >

### 2.4. Uninstall / Unsubscribe

< Add instruction to uninstall the component or unsubscribe to services provided by the component>
<details><summary><b>Show instructions</b></summary>

<br>

**Step 1:**

**Step 2:**

</details>

<br>

## 3. Learning

### 3.1. How-tos
< Describe by task basis how to use the component to do one thing >

### 3.2. Tutorials

< End to end guide to walk you through the steps involved in accomplishing a complete use case >

### 3.3. Resources


<br>

## 4. Roadmap

< List of Now | Next | Future features planned to improved the component >

### 4.1. Now
### 4.2. Next
### 4.3. Later


<br>

## 5. References
### 5.1. Concepts
### 5.2. Motivation
### 5.3. Testing
### 5.4. FAQ

<details><summary><b>FAQ-001</b>: &nbsp; Question <code>code</code></summary>

sample answer

```sh
  code
```
</details>
<details><summary><b>FAQ-002</b>: &nbsp; Question <code>code</code></summary>

sample answer

```sh
  code
```
</details>
<details><summary><b>FAQ-003</b>: &nbsp; Question <code>code</code></summary>

sample answer

```sh
  code
```
</details>



<br>

## 6. Contributing

### 6.1. Instructions

Fork it (yourname/yourproject/fork)
Create your feature branch (git checkout -b feature/fooBar)
Commit your changes (git commit -am 'Add some fooBar')
Push to the branch (git push origin feature/fooBar)
Create a new Pull Request

### 6.3. Build

To build the application, run the following commands

```sh
# Install dependencies
pdm install

# Activate virtual env
eval $(pdm venv activate)

#
# Building
#

# Generate requirements.txt with the application dependencies
pdm export --production  -f requirements -o src/aws_codecommit_trigger_pipeline/requirements.txt 

# Build using docker container
sam build --base-dir src --template src/template.yaml --use-container  --no-cached

```

### 6.4. Package

```sh
zip -r aws-codecommit-trigger-pipeline-vA.B.C-preview.N.zip .aws-sam/build 
```


### 6.4. Deliver

```sh
Upload `aws-codecommit-trigger-pipeline-vA.B.C-preview.N.zip ` to your artificat repository
```

### 6.4. Deploy

1. Download the artifact from your artifact repositiory `aws-codecommit-trigger-pipeline-vA.B.C-preview.N.zip` 
2. Run the following command to start de deployment 
    
    ```sh
    sam deploy --stack-name awsctp-aws-codecommit-trigger-pipeline --resolve-s3 --on-failure DELETE --capabilities CAPABILITY_AUTO_EXPAND CAPABILITY_IAM
    ```

    with profile:

    ```sh
    sam deploy aws-codecommit-trigger-pipeline-vA.B.C-preview.N.zip --profile sdbx --stack-name awsctp-aws-codecommit-trigger-pipeline --resolve-s3 --on-failure DELETE  --capabilities CAPABILITY_AUTO_EXPAND CAPABILITY_IAM
    ```

### 6.4. Delete

```sh
sam delete --profile sdbx --stack-name awsctp-aws-codecommit-trigger-pipeline --no-prompts
```

### 6.2. Styleguide


<br>

## 7. Feedback & Support
Tell people where they can go to for help. It can be any combination of an issue tracker, a chat room, an email address, etc.

### 7.1. Feedback

* Ask a question on Stack Overflow
* Request a new feature
* Upvote popular feature requests
* File an issue
* Follow @code and let us know what you think!

### 7.2. Help

<br>

## 8. Maintainer(s)

Tsklabs Support Team <[lktslionel+team/tsklabs@trueskil.co](mailto:lktslionel+team/tsklabs@trueskil.co)>

<br>

## 9. License

See [LICENSE](./LICENSE)