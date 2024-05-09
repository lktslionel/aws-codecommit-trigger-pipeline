![status/exprimental](https://img.shields.io/badge/STATUS-EXPERIMENTAL-%237C3AED?style=flat-square)
###### TSKLABS • AWS
#  AWS Codecommit Trigger Pipeline <!-- omit in toc -->

AWS Serverless Application that triggers an AWS Codepipeline pipeline on CodeCommit Repository State Change.

<br>

## Contents <!-- omit in toc -->

- [1. Overview](#1-overview)
- [2. Quickstart](#2-quickstart)
  - [2.1. Prerequisites](#21-prerequisites)
  - [2.1. Install / Subscribe](#21-install--subscribe)
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
  - [6.2. Code of Conduct](#62-code-of-conduct)
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


### 2.1. Install / Subscribe

< describe how to setup or install the component >

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

### 6.2. Code of Conduct

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


<br>

## 8. Maintainer(s)

Team Code - Team Name <team@company.com](mailto:team@company.com)>

<br>

## 9. License

(c) `<year>` - `<company-name>`
Licensed under the `<license>` license.