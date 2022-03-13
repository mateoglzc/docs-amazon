![](https://i.imgur.com/gzkJPmi.png)

### Team: 
3

### Version: 
1.0

### Date: 
02/03/2022

### Team Name: 
APD

### Business / Operations Sponsor:
Amazon & Tecnológico de Monterrey

### Project Number:
1

## Content Table

### [Template Change History](#template-change-history)
### [General Project Information](#general-project-information)
### [Scope Statement](#scope-statement)
### [Introduction](#introduction)
### [Description/Objectives](#description/objectives)
### [Governance Model (IN PROGRESS)](#governance-model)
### [Budget/Costs](#budget/costs)
### [S.W.O.T](#s.w.o.t)
### [Justification](#justification)
### [Constraints](#constraints)
11. [Dependencies](#dependencies)
12. [Risks](#risks)
13. [Product Acceptance Criteria](#product-acceptance-criteria)
14. [Business Requirements (IN PROGRESS)](#business-requirements)
- 14.1. [System Features](#system-features)
- 14.2. [Data Requirements](#data-requirements)
- 14.2.1. [Logical Data Model](#logical-data-model)
- 14.2.2. [Data Dictionary](#data-dictionary)
- 14.2.3. [Reports](#reports)
- 14.2.4. [Data Acquisition, Integrity, Retention, and Disposal](#data-acquisition,-integrity,-retention,-and-disposal)
- 14.3. [External Interface Requirements](#external-interface-requirements)
- 14.3.1. [User Interfaces](#user-interfaces)
- 14.3.2. [Software Interfaces](#software-interfaces)
- 14.3.3. [Hardware Interfaces](#hardware-interfaces)
- 14.3.4. [Communication Interfaces](#communication-interfaces)
- 14.4. [Quality Attributes](#quality-attributes)
- 14.4.1. [Usability](#usability)
- 14.4.2. [Performance](#performance)
- 14.4.3. [Security](#security)
- 14.4.4. [Safety](#safety)
- 14.5. [Internationalization and Localization Requirements](#internationalization-and-localization-requirements)
15. [FlowChart](#flowchart)
16. [Define & Design Solution](#define-&-design-solution)
17. [Proposed Architecture (IN PROGRESS)](#proposed-architecture)
18. [Implementation Plan](#implementation-plan)
19. [Test Solution (IN PROGRESS)](#test-solution)
- 19.1. [Objectives](#objectives)
- 19.2. [Scope](#scope)
- 19.3. [Requirements for Testing](#requirements-for-testing)
- 19.4. [Dependencies](#dependencies)
- 19.5. [Testing Strategy](#testing-strategy)
- 19.6. [Testing Management Process](#testing-management-process)
- 19.7. [Testing Environment](#testing-environment)
- 19.8. [Testing Results](#testing-results)
- 19.9. [Conclusions](#conclusions)
- 19.10. [Appendix](#appendix)
20. [Endings](#endings)
21. [Glossary of Term and Acronyms](#glossary-of-term-and-acronyms)

## Template Change History

| Date of Change | Owner of Change | Description |
| -------------- | --------------- | ----------- |
| 02/03/2022     | Team 3          | First version |

## General Project Information


### 1. List of project Reviewers

| ID | Role | Name |
| -------------- | --------------- | ----------- |
| 1    | Professor          | Gilberto Echeverria |
| 2    | Professor          | Esteban Castillo |
| 3    | Professor          | Alan ROjas |
| 4    | Professor          | David Iturriaga |
| 5    | Professor          | Jose Eslava |

### 2. List of Approvals

| ID | Role | Name |
| -------------- | --------------- | ----------- |
| 1    | Professor          | Gilberto Echeverria |
| 2    | Professor          | Esteban Castillo |
| 3    | Professor          | Alan ROjas |
| 4    | Professor          | David Iturriaga |
| 5    | Professor          | Jose Eslava |

### 3.  Scope Statement

The main goal of this project is to provide Amazon Connect Customers a platform that will facilitate training of new call center employees. This will be done by gathering critical information about everyday agent and client interactions, so it can later be revised and used to teach new employees based on real world scenarios. 

### 4. Introduction

In the following document we will describe how this project is going to be developed, outlining the business requirements, system requirements, objectives, architecture, roadmap, risks, dependencies, implementation, tests, and maintenance of the application.

### 5. Description/Objectives

Our main goal for this project is to be able to gather the screen and audio recording of an agent interacting with a client, for it to later be stored. From there, these recordings should be merged creating a video where you can see and hear how the agent works as he’s interacting with the client.

The merged recordings should be available to the call center manager by means of a web app dashboard. Through this dashboard the manager should be able to see, review and categorize each video.

### 6. Governance Model

- **Sponsor:** Amazon & ITESM
- **Supervisors:** All Professors of the Software Planning Course
- **Project Manager:** Carolina Ortega
- **Business Analyst:** Ximena Gonzalez
- **Architect:** Matías Ricardo Méndez Sandoval
- **Developer:** Sebastian Juncos
- **Tester:** Mateo González Cosío Ríos y Valles

### 7. Budget/Costs

For the development of this project our sponsor, Amazon, has given us 600 dollars. Knowing that there will be two development groups working on a solution, **we have estimated that our budget is 300 dollars.** 

- #### **Infrastructure**
    - Amazon Amplify
        
        This service is charged by the amount of build minutes we are going to utilize, as well as how much data we will be storing and serving a month. We are estimating that at most our build time should be between 15 and 20 hours each month, and storing and serving about 1GB of data. **Our cost estimate is 12.17 dollars per month**.
    
    - Amazon DynamoDB

        This service is charged by the amount of storage we are going to be using, as well as how many writes and reads we will do. Estimating we will be using about 25 GB of storage and making about a million consistent writes and read to our database, **our cost estimate is 7.75 dollars a month**.

    - Amazon S3 Storage

        This service is charged by the amount of storage we are going to use to store our video and audio recordings. As well, we are charged for the amount of requests we make to this storage. This is one of the most critical components of our infrastructure, so estimating we would need about 1TB of storage a month, and about 20,000 requests per month. **Our cost estimate is 26.37 dollars per month.**

    - Amazon Lambda

        This service is charged by the amount requests and length of such requests we are going to make per month. Estimating we should be making around 10,000 requests a month, each one taking about 5 minutes to complete. **Our cost estimate is 17.75 dollars per month.**

    - Amazon Cognito
    
        This service charges you for the amount of monthly active users are signing into your application. For the moment we are planning to use the free tier of this service that allows us to manage 50,000 active users. **Our cost estimate is 0 dollars per month.**

    - Amazon Kinesis

    - Amazon Connect

    **Our total monthly cost is 64.04.**

8. [S.W.O.T](#s.w.o.t)
9. [Justification](#justification)
10. [Constraints](#constraints)
11. [Dependencies](#dependencies)
12. [Risks](#risks)
13. [Product Acceptance Criteria](#product-acceptance-criteria)
14. [Business Requirements (IN PROGRESS)](#business-requirements)
- 14.1. [System Features](#system-features)
- 14.2. [Data Requirements](#data-requirements)
- 14.2.1. [Logical Data Model](#logical-data-model)
- 14.2.2. [Data Dictionary](#data-dictionary)
- 14.2.3. [Reports](#reports)
- 14.2.4. [Data Acquisition, Integrity, Retention, and Disposal](#data-acquisition,-integrity,-retention,-and-disposal)
- 14.3. [External Interface Requirements](#external-interface-requirements)
- 14.3.1. [User Interfaces](#user-interfaces)
- 14.3.2. [Software Interfaces](#software-interfaces)
- 14.3.3. [Hardware Interfaces](#hardware-interfaces)
- 14.3.4. [Communication Interfaces](#communication-interfaces)
- 14.4. [Quality Attributes](#quality-attributes)
- 14.4.1. [Usability](#usability)
- 14.4.2. [Performance](#performance)
- 14.4.3. [Security](#security)
- 14.4.4. [Safety](#safety)
- 14.5. [Internationalization and Localization Requirements](#internationalization-and-localization-requirements)
15. [FlowChart](#flowchart)
16. [Define & Design Solution](#define-&-design-solution)
17. [Proposed Architecture (IN PROGRESS)](#proposed-architecture)
18. [Implementation Plan](#implementation-plan)
19. [Test Solution (IN PROGRESS)](#test-solution)
- 19.1. [Objectives](#objectives)
- 19.2. [Scope](#scope)
- 19.3. [Requirements for Testing](#requirements-for-testing)
- 19.4. [Dependencies](#dependencies)
- 19.5. [Testing Strategy](#testing-strategy)
- 19.6. [Testing Management Process](#testing-management-process)
- 19.7. [Testing Environment](#testing-environment)
- 19.8. [Testing Results](#testing-results)
- 19.9. [Conclusions](#conclusions)
- 19.10. [Appendix](#appendix)
20. [Endings](#endings)
21. [Glossary of Term and Acronyms](#glossary-of-term-and-acronyms)
