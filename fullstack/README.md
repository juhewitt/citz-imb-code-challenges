# citz-imb-code-challenges

## Instructions for IS-X Full Stack Developer Position

Build a modern Web Application that tracks and manages Web Applications developed by the Province of BC as described by the User Stories below.

In order to move forward to an interview, you must demonstrate intermediate development knowledge in the following categories included in your solution:

* Modern Frontend Web Application Framework
* Modern Backend API Framework 
* Basic Documentation on how to effortlessly run your solution components on a local development machine
* BONUS - Swagger Documentation for all API endpoints created

### Important!

Read the Code Challenge Context, User Stories and Assessment Scoring for this challenge carefully. Development of the functionality described in these sections is the required outcome of this exercise.

Only working solutions will be considered, or solutions that take minimal effort to troubleshoot and resolve errors at build/runtime to move forward in this interview process.

This code challenge does not require a database to accomplish your solution. In memory data storage or mock-data is highly encouraged.

### Opportunity to Score Additional Points if a Working Solution is Submitted
Swagger Documentation that allows developers to consume all of the API endpoints that you create for your solution

### Solution Presentation in Interview Stage
If you are selected to proceed to the interview stage of this competition, you will be asked to demostrate your solution in a Sprint Review style demo (5-10 minutes in length) to a panel of stakeholders. This demo will include all major architectural components developed to create your solution, and the functionality that those components provide in the form of user value.

## What to Submit

Firstly, create a GitHub repository using your GitHub Account. The name of the repository should use the following convention:

your_first_name-your_last_name_-IS24-full_stack_competition_requisition_number

Your working solution should be present on the **main** branch of the repository. Please trim or remove any extraneous branches prior to submission.

### API Component

This component should use a modern framework or language (of your choice) to create API endpoints utilized by the Frontend component. All endpoints should originate from http://localhost:3000/api

**Example** A GET endpoint to retrieve a user with a specfic user id

http://localhost:3000/api/user/:userId

**User Authentication/Authorization is not required for the purposes of your solution.**

Your API should include at minimum the following functionality:
* A health endpoint that returns a http 200 reponse indicating your component is healthy
* All GET, POST, PUT, PATCH and DELETE endpoints return the proper response codes when consumed
* Basic error handling within the endpoints is present when required

**BONUS**

All API endpoints that created in order to develop the required frontend application functionality should be documented via Swagger.

The Swagger documentation should be consumed by anyone building the project on their local workstation at http://localhost:3000/api/api-docs.

### Frontend Component

This component should be developed using a modern javascript framework (of your choice). This component should utilize endpoints developed in your API solution to
provide your Frontend component with basic CRUD actions described in the user stories provided. 

## Code Challenge Context

The BC Government Ministry of Citizens' Services Information Management Branch (IMB) is currently trying to catalog current modern web applications in GitHub, as well as new projects that are coming up in the future. Currently there are 40 projects marked for modernization that need to be cataloged, as well as 3 projects that are either actively being developed or in a maintainence lifecyle.

Product owners have expressed the desire to communicate to the branch where these projects are housed (GitHub Repository) as well as the resources (Developers, DevOps, etc.) that are allocated to the project. As IMB is currently driving a common component practice as well, Senior leadership would like to tag or label which projects use common component services like keycloak, gc-notify, redis, rabbitmq for example.

The user base for this application will include a wide array of technical skills, therefore making this application as simple as possible to display, create and edit information is being stressed by the IMB Senior Leadership Team (SLT).

## Personas

**Berenice** A director within IMB that is fairly new to the branch, but has worked with BC Government for 10+ years. She has experience with software development projects as she was previously a Product Owner for a project that had a successful production launch. She currently manages Service Design and SCRUM Master resources, and would like to know at a glance who is resourced on what project. She understands Agile philosophy and knows that a solution may take many iterations to achieve a desired state of functionality.

**Alan** A DevOps resource that has worked for IMB for the last 3 Years. He has worked on many projects, including from inception to maintainance lifecycles for IMB, setting up deployment pipelines and integrating technologies into projects that help increase developer velocity. He actively engages the developer community to understand their ever changing needs from project to project. Alan is currently looking to build a tool that allows product owners/stakeholders within IMB to understand resource utilization across all projects within IMB to help avoid developer/resource burn-out.

**Both IMB Employees** are looking for a tool that offers all users within IMB easily digestible data based on the bredth and depth of the many projects they currently develop and maintain, as well as projects that are on the horizon for IMB. Displaying exactly the right amount of information at a glance is paramount to both Berenice and Alan.


## User Stories

### One

As Berenice, I want to be able to add a project to the list of projects that IMB is developing or maintaining.

**Acceptance Criteria**
* Given that I am Berenice
* And I am aware of a new development project within IMB
* When I go to the project dashboard
* I can click a button 
* And the application takes me to a basic "Create Project" form
* And I can click a submit button to save basic product data

### Two

As Berenice, I want to see a list of all projects that IMB currently develops or maintains in a dashboard

**Acceptance Criteria**
* Given that I am Berenice
* And I am trying to see a list of all projects within IMB
* When I navigate to the application landing page
* I can see a list of all projects within IMB
* And all relevant information related to each project

### Three

As Alan I want to be able to add/edit project related information

**Acceptance Criteria**
* Given that I am Alan
* And I want edit details related to a specific project
* When I click on an edit button found at the end of a row within a dashboard
* I am redirected to a simple form that displays all of a given projects details
* And allows me to edit and submit those such that they are persistent

## Questions

Further clarification on project details can be directed to the following email addresses
* marker1@gov.bc.ca
* marker2@gov.bc.ca
* marker3@gov.bc.ca

Emails should be responded to within an hour of being received during business hours (9am-5pm).
Outside of normal business hours will be best effort, hopefully before end-of-day.

## Assessment Scoring

The following tables will be provided to you via email after marking of your solution is complete.

### Backend API Component
| Rating                  | Criteria                                                               |
|-------------------------|------------------------------------------------------------------------|
| Pass/Acceptable         | * RESTful                                                              |
|                         | * Endpoints return http responses required for given CRUD actions      |
|                         | * Basic commenting of your solution                                    |
| Fail/Unacceptable       | * More than one requirement of Pass/Acceptable are not met             |

### Frontend Component
| Rating                  | Criteria                                                                                            |
|-------------------------|-----------------------------------------------------------------------------------------------------|
| Pass/Acceptable         |                                                                                                     |
|                         | * Microservice component                                                                            |
|                         | * Functional or Class based component design based on requirement                                   | 
|                         | * Appropriate naming of components, elements, classes, etc.                                         |
|                         | * Basic error handling when interacting with API (ex// API is not present or healthy)               |
|                         | * Basic commenting of your solution                                                                 | 
|                         | * Utilizes API to perform required GET, PUT, POST or DELETE actions when required                   |
| Fail/Unacceptable       | * More than one requirement of Pass/Acceptable are not met                                          |

### BONUS - API Swagger Documentation

| Rating                  | Criteria                                                                                                      |
|-------------------------|---------------------------------------------------------------------------------------------------------------|
| Pass/Acceptable         | * Swagger documentation present for all endpoints developed, and served at http://localhost:3000/api/api-docs |
| Fail/Unacceptable       | * Swagger Documentation is incomplete or not present                                                          |