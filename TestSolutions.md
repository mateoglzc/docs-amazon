# Test Solution
- ## Objectives

    Our main objective in this section is to assure that during the development cycle we do not encounter a critical system errors that forces us to redefine or redevelop any component as this will be a setback during the development stage, while also assuring the quality of our application. We intend to achive this by following the Testing Strategy and Testing Process Management defined below.   

- ## Scope

    For this project we have identified a set of critical components that allows us to test the overall performance of the system. These components are directly tied to our functional requirements, and testing them is a necessary step in assuring the quality of our development.

    These components are: 
    - Screen and Audio Recordings
    - Merge Screen and Audio Recordings
    - Dashboard View
    - Storage and Data Upload

- ## Requirements for Testing

    Our testing requirements can be divided into 3 subsections
    - Backend Testing
    - Frontend Testing
    - Overall Testing

    The most common testing is going to be in both Frontend and Backend testing; as for the Overall testing, this means the integration of both Frontend and Backend sections to fully finish either a function, module or component. We could call Overall testing as the Testing integration process

    Our specific requirements are:
    - We will be using a specific format for documenting our testing 
    - Have a minimum RAM capacity in order to test our app
    - Having the same version throughout the testing team in order to mantain testing performance
    - All testers should have similar specs when it comes to hardware
    - Developers must specify each testing input and output in detail, this will be shown as a comment in the code

- ## Dependencies
  


| ID    | Name of Activity/Component                              | Description and notes                                                                  | Responsible       | Initial Date | End Date    | Depende ncies |
| ----- | ------------------------------------------------------- | -------------------------------------------------------------------------------------- | ----------------- | ------------ | ----------- | ------------- |
| 1\. 1 | Capture of business requirements                        | Remote session with Amazon to capture business requirements                            | Every team member | Week 1       | Week 1      |               |
| 1\. 2 | Business Requirements Revision with Amazon              | Remote session with Amazon to ask final questions about the business requirements      | Carolina Ortega   | 23/02/22     | 23/02/22    | 1.1           |
| 1\. 3 | Business Requirements Revision with Advisors (teachers) | Session with teachers to correct details                                               | Every team member | 7/03/22      | 11/03/22    | 1.1           |
|       | Presentation Tier Implementation (Front-end)            |                                                                                        |
| 2\. 1 | User Interface Design                                   | Proposal design of app interfaces and navigation with Canva                            | Sebastián Juncos | 22/02/20 22  | 22/02/22    | 1.3           |
| 2\. 2 | Start page interface                                    | Implementatio n of Start page interface                                                | Carolina Ortega   | 22/03/20 22  | 28/03/202 2 |               |
| 2\. 3 | Start/Stop and Save Recording component                 | Implementatio n of the screen recording tool with Angular                              | Matías Méndez   | 22/03/20 22  | 08/04/22    |               |
| 2\. 3 | Admin interface to add video information                | Implementatio n of interface to edit the information of the stored videos with Angular | Ximena González  | 22/03/22     | 08/04/22    |               |
| 2\. 5 | Integration of all the components                       | Integration of all of the front-end                                                    | Every team member | 31/03/22     | 14/04/22    | 2.2 , 2.3,2.4 |
- ## Testing Strategy

    Our testing strategy consists in various testing levels:
    - Function Level
        - Tests whether each application feature works as per the software requirements.
    - Module Level
        - Tests each unit of these modules, we can say that it tests the smaller building blocks of the program.
    - Component Level
        - Test objects can be tested independently as components, without integrating with other components.

    For these testing levels, we will use either Black Box or White Box tests.
    Black box tests make sure of the functionality in these testing levels, wich means there is no attention to how the code works, as long as the result is the expected one.
    Black box tests will be used for Function and Module Levels.

    White box tests on the other hand, do focus on the way the conde is written without caring much for each testing result.
    White box tests will be used for Module and Component Levels.

    The normal flow of our testing process is:
    Informal Revision -> Technical Revision -> Inspection

    If any of these tests fail, we would take a step backwards to the previous testing stage, but if there's a case where technical revision fails two times, this component or module will be directly sent to inspection.

- ## Testing Management Process
   
    - Informal Revision

        This will take place everytime a code function is completed. During this revision the developer assigned will only be performing black box tests. This revision does not require any documentation, but it is extremely important for the module that this function takes part to have all their internal functions informally revised. This is a requisite for the module to be considered for a Technical Revision. 

    - Technical Revision

        This will take place everytime a code module is completed. A team consisting of at least 3 or 5 internal members and 1 or 2 external members without surpassing the 6 total members, must meet to perform this revision. During it, mostly black box tests are meant to be done, but there is the possibiliy of making white box tests as well. For this revision it is necessary to fill out a document defined in the appendix. This is extremly important because in order for the component that this module belongs to, it is necessary that every module that takes part of it has passed this revision.  

    - Inspection

        This will take place everytime a code component is completed. A tema consisting of at least 7 or 14 internal members and 1 or 2 external members without surpassing 15 total members, must meet to perform this revision. During it, mostly white box tests are meant to be done, but there is the possibility to performing other high definition tests. For this revision it is necessary to fill out a document defined in the appendix. This is extremy important because in order to mark as our component completed and deployed it must have passed this revision. 

- ## Testing Environment

    As mentioned in Testing Requirements (19.3), all testers need personal computers with similar hardware specifications, certain RAM space and the same software version. The input and output format will also be included as comments within the code, as diferent data types may be needed for specific procedures.

- ## Testing Results

    To be done in next development chapter.

- ## Conclusions

    At this stage of the project we comprehended and reflected about the basic and important requirements to be carried out, we have identified the objectives that our socio domador (in this case Amazon) has asked us to implement, and the initial stage has been completed. When we start developing the different parts like front-end and back-end of the web application, doubts will arise about the Amazon services and how we can use APIs and documentation, as well as what will be more functional and efficient to implement in the application.

- # Appendix

    [Business Meetings Recaps](https://docs.google.com/document/d/1YVaDb1OCT77fJ3wEzoixPjSeQdUWo7MZLTo0cw4uvn8/edit?usp=sharing)

    [Technical Revision](./Diagrams/Technical%20Revision%20Template.pdf)
    
    [Inspection](./Diagrams/Inspection%20Revision%20Template.pdf)
 