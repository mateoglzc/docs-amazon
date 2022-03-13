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
3

# TO DO
- **Test Solutions** 
- Endings
- Budget for Kinesis and Connect Services
- **Data Requirements**
- Implement non-functional requirements
- **Data Acquisition, Integrity, Retention, and Disposal**
- **Architecture Diagram**
- **Put a better description in communicated Interfaces**

 

## Content Table

1. [Template Change History](#template-change-history)
2. [General Project Information](#general-project-information)
3. [Scope Statement](#scope-statement)
4. [Introduction](#introduction)
5. [Description/Objectives](#description/objectives)
6. [Governance Model](#governance-model)
7. [Budget/Costs](#budget/costs)
8. [S.W.O.T](#s.w.o.t)
9. [Justification](#justification)
10. [Constraints](#constraints)
11. [Dependencies](#dependencies)
12. [Risks](#risks)
13. [Product Acceptance Criteria](#product-acceptance-criteria)
14. [Business Requirements](#business-requirements)
- 14.1 [System Features](#system-features)
- 14.2 [Data Requirements](#data-requirements)
- 14.2.1 [Logical Data Model](#logical-data-model)
- 14.2.2 [Data Dictionary](#data-dictionary)
- 14.2.3 [Reports](#reports)
- 14.2.4 [Data Acquisition, Integrity, Retention, and Disposal](#data-acquisition,-integrity,-retention,-and-disposal)
- 14.3 [External Interface Requirements](#external-interface-requirements)
- 14.3.1 [User Interfaces](#user-interfaces)
- 14.3.2 [Software Interfaces](#software-interfaces)
- 14.3.3 [Hardware Interfaces](#hardware-interfaces)
- 14.3.4 [Communication Interfaces](#communication-interfaces)
- 14.4 [Quality Attributes](#quality-attributes)
- 14.4.1 [Usability](#usability)
- 14.4.2 [Performance](#performance)
- 14.4.3 [Security](#security)
- 14.4.4 [Safety](#safety)
- 14.5 [Internationalization and Localization Requirements](#internationalization-and-localization-requirements)
15. [FlowChart](#flowchart)
16. [Define & Design Solution](#define-&-design-solution)
17. [Proposed Architecture](#proposed-architecture)
18. [Implementation Plan](#implementation-plan)
19. [Test Solution](#test-solution)
- 19.1 [Objectives](#objectives)
- 19.2 [Scope](#scope)
- 19.3 [Requirements for Testing](#requirements-for-testing)
- 19.4 [Dependencies](#dependencies)
- 19.5 [Testing Strategy](#testing-strategy)
- 19.6 [Testing Management Process](#testing-management-process)
- 19.7 [Testing Environment](#testing-environment)
- 19.8 [Testing Results](#testing-results)
- 19.9 [Conclusions](#conclusions)
- 19.10 [Appendix](#appendix)
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

### 8. S.W.O.T

- #### Strengths
    - Experience making friendly UI
    - Experience developing web applications
    - Experience hosting web services
- #### Weaknesses
    - No Amazon API or Amazon services knowledge
    - Never managed a team this big
- #### Opportunities
    - Ability to use Amazon API's and services to facilitate development
    - Code Review
    - Amazon support and supervision
- #### Threats
    - Poor communication with Amazon
    - Surpass cost budget
    - Poor time management

### 9. Justification

In  this day and age, customer support is extremely important for any company.  Amazon Connect is already helping their clients provide top of the line service to their customers, but as each company grows their clientele gets bigger and the necessity to hire call center agents increases. Our project aims to facilitate the training of these new call center agents by providing call center managers a platform to teach each agent with real world scenarios. This platform will facilitate and expedite training new agents assuring they maintain the quality of customer service experience. 


### 10. Constraints

- Amazon services exclusivity 
- A 300 dollar budget for all Amazon services used during the development
- Limited contact with Amazon representatives
- A 10 week development period
- A 5 week planning period

### 11. Dependencies

- Amazon services and API's

### 12. Risks

- Low Level Risks
    - Exceed the expected database storage.
    - Low video quality recordings.
    - Unintelligable audio recordings.
    - Exceeding budget cost estimate.

- Medium Level Risks 
    - Video Recordings not being saved properly.
    - Data leaks.
    - Failure to encrypt user information.

- High Level Risks
    - Failure to record screen recording.
    - Failure to merge audio and video recodings.
    - Choosing a wrong Amazon service to develop the solution.
    - Incorrect management of users permissions.
    - Sensitive data leak.


### 13. Product Acceptance Criteria

- The web app should only give access to the video catalog if the user is a call center manager.
- The security implemented should recognize personal data. 
- The recordings should download correctly into our databse following the tags given.
- The call center manager should be able to see all the recordings that were made.


### 14. Business Requirements
- ### 14.1 System Features
    - **Voice and Screen Recording**
        
        Our application should be able to record the call center agent screen, gather the voice recording from a Amazon cConnect database and merge audio and video.

        - **Description**
            
            For the fulfillment of this requirement, we will introduce two components:

            **Video and Audio Recording Component**

            ![Video and Audio Screen Recording Component Use case level 0](./Diagrams/VACN1.png)
            ![Video and Audio Screen Recording Component Use case level 1.1](./Diagrams/VACN2-1.png)
            ![Video and Audio Screen Recording Component Use case level 1.2](./Diagrams/VACN2-2.png)

            **Merge Video and Audio Recording Component**
            
            ![Merge Video and Audio Recordings Component Use case level 0](./Diagrams/MAVCN1.png)
            ![Merge Video and Audio Recordings Component Use case level 1](./Diagrams/MAVCN2-1.png)
            ![Merge Video and Audio Recordings Component Use case level 2](./Diagrams/MAVCN2-2.png)

        
        - **Stimulus/Response Sequence**

            **Video and Audio Recording Component**

            ![Video and Audio Screen Recording Component Flow Diagram](./Diagrams/VAFD1.png)

            **Merge Video and Audio Recording Component**

            ![Merge Video and Audio Recordings Component Flow Diagram](./Diagrams/MAVFD1.png)

        - **Functional Requirements**

        | ID | VACN1 |
        | --- | --- |
        | Name |  Global Screen and Audio Recording Component.  |
        | Description | Defintion of top level functionality of this component.|
        | Scenery | A customer calls a Amazon Connect Client Call Center. |
        | Exceptions | Call Lasts less that 10 seconds. |
        | Pre-conditions | Call Recieved. |
        | Post-Contitions| Agents categorizes call. |
        | Acceptance Criteria | Call Recieved and correctly started recording process. |

        | ID | VACN2-1 |
        | --- | --- |
        | Name |  Voice Recording Detailed  |
        | Description | Definition of how we use Amazon Connect to record a call. |
        | Scenery | A customer calls a Amazon Connect Client Call Center. |
        | Exceptions |  Call Lasts less that 10 seconds. |
        | Pre-conditions | Call Recieved and correctly started recording process. |
        | Post-Contitions| Audio Stored in S3 Storage and path sent to Amazon Amplify. |
        | Acceptance Criteria | Voice recording correctly stored and path correctly sent to Amazon Amplify. |

        | ID | VACN2-2 |
        | --- | --- |
        | Name |  Screen Recording Detailed  |
        | Description | Definition of how we use the Screen Recording Component to record the agent's screen |
        | Scenery | A customer calls a Amazon Connect Client Call Center. |
        | Exceptions | Call Lasts less that 10 seconds. |
        | Pre-conditions | Call Recieved and correctly started recording process. |
        | Post-Contitions| Video Stored in S3 Storage and path sent to Amazon Amplify. |
        | Acceptance Criteria | Screen recording correctly stored and path correctly sent to Amazon Amplify. |

        | ID | MAVCN1 |
        | --- | --- |
        | Name | Merge Audio and Screen Recording Component |
        | Description | Defintion of top level functionality of this component. |
        | Scenery | Both Audio and Screen recordings have been correctly stored, and are ready to be merged. |
        | Exceptions | Either Screen or Audio Recording is missing. |
        | Pre-conditions | A call has been made and both Audio and Screen recordings have been correctly stored. |
        | Post-Contitions| Storage must have sufficent space to store new recording. |
        | Acceptance Criteria | New recording correctly merged. Audio and Screen synchronisation. |

        | ID | MAVCN2-1 |
        | --- | --- |
        | Name |  Merge Audio and Video Screen Recording Architecture  |
        | Description | Definition of the Amazon Service we are going to use for our component. |
        | Scenery | Both Audio and Screen recordings have been correctly stored, and are ready to be merged. |
        | Exceptions | Either Screen or Audio Recording is missing. |
        | Pre-conditions | A call has been made and both Audio and Screen recordings have been correctly stored. |
        | Post-Contitions| Storage must have sufficent space to store new recording. |
        | Acceptance Criteria | New recording correctly merged. Audio and Screen synchronisation. |

        | ID | MAVCN2-2 |
        | --- | --- |
        | Name | Merge Audio and Screen Recording Component Functionality  |
        | Description | Definition of how the functionality of this component. |
        | Scenery | Both Audio and Screen recordings have been correctly stored, and are ready to be merged. |
        | Exceptions | Either Screen or Audio Recording is missing. |
        | Pre-conditions | A call has been made and both Audio and Screen recordings have been correctly stored. |
        | Post-Contitions| Storage must have sufficent space to store new recording. |
        | Acceptance Criteria | New recording correctly merged. Audio and Screen synchronisation. |



    - **Storage and Data Upload**

        Our application should be able to store and upload data inside an Amazon Connect S3 Bucket. The data stored can be filtered by the used video metadata. (Tags, Day, Hour, etc.)

        - **Description**

        ![Storage and Data Upload Component Use case Diagram Level 0](./Diagrams/SDCN1.png)

        - **Stimulus/Response Sequence**

        ![Storage and Data Upload Component Flow Diagram](./Diagrams/SDFD1.png)

        - **Functional Requirements**

        | ID | SDCN1 |
        | --- | --- |
        | Name | Storage and Data Upload Component |
        | Description | Definition of how this component will work. |
        | Scenery | Voice and Screen recordings have been made and are in need of storage and categorization. |
        | Exceptions | Voice and Screen recording has failed. |
        | Pre-conditions |  A customer calls a Amazon Connect Client Call Center, and the Audio and Screen Recording Component has succesfully recorded and stored the customer's voice and the agent's screen. |
        | Post-Contitions| |
        | Acceptance Criteria | Recordings correctly stored and are available to be retrieved. |

    - **Dashboard View**

        Our application should be able to show and filter the catalog of recordings stored in our database. From this screen the administrator should be able to view, edit tags, review, and delete each video shown.

        - **Description**

        ![Dashboard Component Use Case Diagram Level 0](./Diagrams/DCN1.png)
        ![Dahsboard Component Use Case Diagram Level 1](./Diagrams/DCN2-1.png)
        
        - **Stimulus/Response Sequence**

        ![Dashboard Component Use Case Diagram](./Diagrams/DFD1.png)

        - **Functional Requirements**

        | ID | DCN1 |
        | --- | --- |
        | Name | Dashboard Component  |
        | Description | Definition of how this component is going to work. |
        | Scenery | A call center manager access our application platform with the right credentials. |
        | Exceptions | The call center manager doesn't have the right credentials. |
        | Pre-conditions | Both the Video and Audio Recording component and the Storage and Data Upload component are working correctly. |
        | Post-Contitions| |
        | Acceptance Criteria | The call center manager is able to interact with each video in the database. |

        | ID | DCN2-1 |
        | --- | --- |
        | Name | Retrieve merge video. |
        | Description | Definition of how our dashboard component communicates with the Storage and Data Upload component to retrieve a specific video. |
        | Scenery | A call center manager access our application platform with the right credentials. |
        | Exceptions | The call center manager doesn't have the right credentials. |
        | Pre-conditions | Both the Video and Audio Recording component and the Storage and Data Upload component are working correctly. |
        | Post-Contitions| |
        | Acceptance Criteria | The call center manager is able to interact with each video in the database. |

- ### 14.2 Data Requirements
    - #### 14.2.1 Logical Data Model
    - #### 14.2.2 Data Dictionary
    - #### 14.2.3 Reports
    - #### 14.2.4 Data Acquisition, Integrity, Retention, and Disposal
    Data is going to be aquired through our application integration with various Amazon AWS Services such as: Amazon Connect, Amazon DynamoDB, Amazon Amplify, and many others. As estated above our application is divided in various components in which the data is going to be distributed. 
    
    **Example**
    *Data will be acquired through the integration of Amazon Connect to the app using AWS RDS, of both the agent / supervisor and the recording of calls done by agents, as described within the above sections. By using a relational database, the application is able to keep track of all recordings without saturating the "recording" object itself by only storing the agentId within it, and keep agent data separate from it.*

    *The necessary techniques to protect the app's data integrity are: backups of database; so that not all information is lost if any fatal error happens regarding the app, mirroring of all compressable software; which should always keep up with the latest release of the application and be used only when the backup fails, checkpointing of application; which provide the progress of the app trhough the course of the project to the stakeholders via its snapshots of each version released, and data accuracy verification; in order to be able to analyze all data recollected and remove any inconcistency that produces said error so that data quality is consistent.*

- ### 14.3 External Interface Requirements
    - #### 14.3.1 User Interfaces
        - Call Center Manager

            **Log In Screen**
        ![Call Center Manager Log In](./Diagrams/ManagerLogIn.png)
            **Dashboard**
        ![Call Center Manager Dashboard](./Diagrams/ManagerDashboard.png)
        - Call Center Agent

            **Topic Selection**
        ![Call Center Agent's Screen](./Diagrams/AgentScreen.png)
    - #### 14.3.2 Software Interfaces
        - **Amazon Amplify**

            Amazon Amplify serves as the heart of our application. Here our frontend and our backend is going to be hosted. Also, Amplify allows us to connect our app to Amazon lambda functions, Amazon S3 storage, and our Amazon DynamoDB database. 

            Amazon Amplify allows us to connect all these services by using their CLI, and on top of that it let’s us create a continuous integration and continuous development workflow.

            Through the Amplify API we will be able to connect all our application components with ease.
        
        - **Amazon Connect**

            Amazon Connect is a critical component of our application because it connects us directly with the call center. Here we can see how calls are rooted, how agents interact with customers and most importantly it allows us to save the voice recording of the call into an S3 bucket instance. 

        - **Amazon Lambda**

            The Amazon Lambda API will serve as our merge component. Through this service and their respective API’s, we will be able to connect to Amazon Amplify and our storage hosted in Amazon S3. This completes a critical part in our business logic tier, which in this case will allow us to implement the appropriate solution.
        
        - **Amazon S3**

            The Amazon S3 API component is going to allow the team to store the screen and audio recording files. This Amazon Component will be accessed through the business logic tier.

        - **Amazon DynamoDB**

            The Amazon DynamoDB will be used as our primary database. Here we will store all our business data, audio and video recording paths, tags, and reviews. This service API will help us to connect it to Amazon Amplify so all our app components can access this service with ease. 
        
        - **Amazon Cognito**

            Amazon Cognito will serve as our authentication layer. It allows us to give access to the right people at the right time. With this, it gives our app an extra layer of security, assuring our clients that their information is secure.

        - **Amazon Kinesis**

            Amazon Kinesis plays an important role in our app, because it will allow us to start a screen recording as soon as a call is initiated. Through this service and their respective API, we will be able to connect it to Amazon Amplify and Amazon S3 which allows us to store and categorize the video recordings

    - #### 14.3.3 Communication Interfaces

        We will use HTTPS for all requests between amazon services and SSH for connecting to GitHub.

- ### 14.4 Quality Attributes
    - #### 14.4.1. Usability
    - #### 14.4.2 Performance
    - #### 14.4.3 Security
    - #### 14.4.4 Safety
- ### 14.5 Internationalization and Localization Requirements
### 15. FlowChart
### 16. Define & Design Solution
For this project we have identified a set of critical components that allows us to test the overall performance of the system. These components are directly tied to our functional requirements, and testing them is a necessary step in assuring the quality of our development.

These components are:
- Screen Recording
- Dashboard
- Storage

### 17. Proposed Architecture
The chosen architecture for this project is the Layers Architecture, which will allow the team to implement this project by layers in such a way that the organization and distribution of the workload will be managed in the following layers:
- **Presentation Tier:** Data visualization, User interface and interactions.
- **Logic Tier:** Business logic layer.
- **Data Tier:** Access and management of the database implemented in Amazon DynamoDB.

Thanks to this architecture, it will be easier to develop our web application with a Model-View-Controller pattern allowing the implementation of a system of components with the desired frameworks. 

### 18. Implementation Plan
| ID                           | Name of Activity/Component                              | Description and notes                                                                 | Responsible                                     | Initial Date | End Date   | Dependencies   |
| ---------------------------- | ------------------------------------------------------- | ------------------------------------------------------------------------------------- | ----------------------------------------------- | ------------ | ---------- | -------------- |
| 1.1                          | Capture of business requirements                        | Remote session with Amazon  to capture business requirements                          | Every team member                               | 16/02/22     | 17/02/22   |                |
| 1.2                          | Business Requirements Revision with Amazon              | Remote session with Amazon  to ask final questions about the business requirements    | Carolina Ortega                                 | 23/02/22     | 23/02/22   | 1.1            |
| 1.3                          | Business Requirements Revision with Advisors (teachers) | Session with teachers to correct details                                              | Every team member                               | 7/03/22      | 11/03/22   | 1.1      |


**Presentation Tier Implementation (Front-end)**


| ID                           | Name of Activity/Component                              | Description and notes                                                                 | Responsible                                     | Initial Date | End Date   | Dependencies   |
| ---------------------------- | ------------------------------------------------------- | ------------------------------------------------------------------------------------- | ----------------------------------------------- | ------------ | ---------- | -------------- |
| 2.1                          | User Interface Design                                   | Proposal design of app interfaces and navigation with Canva                           | Sebastián Juncos                                | 22/02/2022   | 22/02/22   | 1.3            |
| 2.2                          | Start page interface                                    | Implementation of Start page interface                                                | Carolina Ortega                                 | 22/03/2022   | 28/03/2022 |                |
| 2.3                          | Start/Stop and Save Recording component                 | Implementation of the screen recording tool with Angular                              | Matías Méndez                                   | 22/03/2022   | 08/04/22   |                |
| 2.3                          | Admin interface to add video information                | Implementation of interface to edit the information of the stored videos with Angular | Ximena González                                 | 22/03/22     | 08/04/22   |                |
| 2.5                          | Integration of all the components                       | Integration of all of the front-end components                                        | Every team member                               | 31/03/22     | 14/04/22   | 2.2 , 2.3,2.4  |
| 2.6                          | Front-end testing                                       | Test all of the interface components                                                  | Mateo Gónzalez                                  | 14/04/22     | 18/04/22   | 2.5            |
| 2.6                          | Team meeting                                            | Team meeting to discuss advances and areas of opportunity                             | Every team member                               | 6/04/22      | 6/04/22    |                |

**Data Tier Implementation**

| ID                           | Name of Activity/Component                              | Description and notes                                                                 | Responsible                                     | Initial Date | End Date   | Dependencies   |
| ---------------------------- | ------------------------------------------------------- | ------------------------------------------------------------------------------------- | ----------------------------------------------- | ------------ | ---------- | -------------- |
| 3.1                          | Database planning and design                            | Identify the required tables, relations, and columns for the database                 | Every team member                               | 22/03/22     | 23/03/22   |                |
| 3.2                          | Database implementation                                 | Implement the design of the database with the desired language and server             | Carolina Ortega, Matías Méndez, Ximena Gonzalez | 24/03/22     | 29/03/22   | 3.1            |
| 3.3                          | Database Testing                                        | Test the functionality of the database with the appropriate tools                     | Mateo Gonzalez and Sebastián Juncos             | 30/03/22     | 2/04/22    | 3.2            |
| 3.4                          | Team meeting                                            | Team meeting to discuss advances and areas of opportunity                             | Every team member                               | 6/04/22      | 6/04/22    |                |


**Back-end Tier Implementation**

| ID                           | Name of Activity/Component                              | Description and notes                                                                 | Responsible                                     | Initial Date | End Date   | Dependencies   |
| ---------------------------- | ------------------------------------------------------- | ------------------------------------------------------------------------------------- | ----------------------------------------------- | ------------ | ---------- | -------------- |
| 4.1                          | API                                                     | API to connect the Front-end interaction with the database                            | Every team member                               | 19/04/22     | 25/04/22   | 3.3, 2.5       |
| 4.2                          | API Testing                                             | Test the functionality of the API with the appropriate tools                          | Mateo Gonzalez and Sebastián Juncos             | 26/04/22     | 30/04/22   | 4.1            |
| 4.3                          | Team meeting                                            | Team meeting to discuss advances and areas of opportunity                             | Every team member                               | 31/04/22     | 31/04/22   | 4.2            |

**Final stage**

| ID                           | Name of Activity/Component                              | Description and notes                                                                 | Responsible                                     | Initial Date | End Date   | Dependencies   |
| ---------------------------- | ------------------------------------------------------- | ------------------------------------------------------------------------------------- | ----------------------------------------------- | ------------ | ---------- | -------------- |
| 5.1                          | Complete integration of the application                 | Complete integration of backend, frontend and database.                               | Every team member | 01/05/22     | 10/05/22   | 4.1, 3.2, 2.5 |
| 5.2                          | Testing of the complete application                     | Testing of all the components of the application                                      | Every team member | 11/05/22     | 20/05/22   | 5.1            |
| 5.3                          | Final software revision                                 | Final software revision and correction with advisors and Amazon if possible           | Every team member                               | 21/05/22     | 30/05/22   | 5.1 , 5.2      |
| 5.4                          | Team meeting                                            | Team meeting to discuss advances and areas of opportunity                             | Every team member                               | 31/05/22     | 31/05/22   |                |
| 5.5                          | Final presentation                                      | Final presentation with Amazon                                                        | Every team member                               | 3/06/22      | 3/06/22    |          |

### 19. Test Solution
- ####  19.1 Objectives
- #### 19.2 Scope
- #### 19.3 Requirements for Testing
- #### 19.4 Dependencies
- #### 19.5 Testing Strategy
- #### 19.6 Testing Management Process
- #### 19.7 Testing Environment
- #### 19.8 Testing Results
- #### 19.9 Conclusions
- #### 19.10 Appendix
### 20. Endings
### 21. Glossary of Term and Acronyms
