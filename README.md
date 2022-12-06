# citz-imb-code-challenges

## Instructions for IS-X Full Stack Developer Position

Build a modern Web Application that tracks and manages Web Applications developed by the Province of BC as described by the User Stories below.

In order to move forward to an interview, you must demonstrate intermediate development knowledge in the following categories included in your solution:

* Modern Frontend Web Application Framework
* Modern Backend API Framework 
* Database for data storage, utilized by the API
* Containerization of the components included in your solution
* Basic Documentation on how to effortlessly run your solution on a local development machine
* (Bonus) Basic Quality Assurance Tasks (Unit Tests) using a Modern Testing Tool/Library
* (Bonus) A basic description or diagram that outlines how your solution would be built and deployed on a cloud platform like the BC Gov hosted Openshift cluster
* (Bonus) A wiki article outlining basic decision points or assumptions made during solution development

### Important!
Only working containerized solutions will be considered to move forward in this interview process (ie// A frontend and backend container that build and run without error on a Windows or Apple operating system)

### Opportunity to Score Additional Points if a Working Solution is Submitted
1) Basic unit tests for one or both of your API and Frontend solutions will be considered, along with a description of how to run the suite of tests your developed against your solution.

2) A piece of documentation that outlines the process of how your solution will be containerized and hosted in a cloud platform like BC Gov hosted Openshift.

3) Include decision points, diagrams and assumptions made during the development of your solution in a Wiki style article that could be potentially published to a public Github Repository.

### Solution Presentation in Interview Stage
If you are selected to proceed to the interview stage of this competition, you will be asked to demostrate your solution in a Sprint Review style demo (5-10 minutes in length) to a panel of stakeholders. This demo will include all major architectural components developed to create your solution, and the functionality that those components provide in the form of user value.

## What to Submit

Firstly, clone this repository to your local development machine. All of your work should be done in a feature branch named in the following convention:

```
yourFirstName-yourLastName-IS-x-competition 
```

Your solution should be submitted in the form of a pull request against the **main** branch of this repository. This pull request should utilize the pull request template provided.

### API Component

This component should use a modern framework or language (of your choice) to create API endpoints utilized by the Frontend component and that integrate with the chosen database for the solution.

User Authentication/Authorization is not required for the purposes of your solution.

Your API should include at minimum two pieces of functionality:
* a health endpoint that returns a http 200 reponse indicating your component is healthy
* basic swagger documentation of any/all endpoints that were developed over the course of your solution

### Frontend Component

This component should be developed using a modern javascript framework (of your choice). This component should utilize endpoints developed in your API solution to
provide your Frontend component with basic CRUD actions described in the user stories provided. 

Your frontend solution should interact with the API such that there are anywhere between 2-4 sample projects seeded in the database that the frontend will display.

### Database

This component should be a container of a modern relational database of your choice (MySQL, Postgres, etc.) that allows your API to perform CRUD actions against a basic schema.

### Containerization

This part of your solution should utilize docker, dockerfiles and/or docker-compose to create containers for your API, Frontend and database. The containers should be able to utilize a network configuration to allow for container-to-container communications without error. This solution should allow for your components to be developed, agnostic to the operating system of choice.

## Code Challenge Context

The BC Government Ministry of Citizens' Services Information Management Branch (IMB) is currently trying to catalog current modern web applications in Github, as well as new projects that are coming up in the future. Currently there are 40 projects marked for modernization that need to be cataloged, as well as 3 projects that are either actively being developed or in a maintainence lifecyle.

Product owners have expressed the desire to communicate to the branch where these projects are housed (Github Repository) as well as the resources (Developers, DevOps, etc.) that are allocated to the project. As IMB is currently driving a common component practice as well, Senior leadership would like to tag or label which projects use common component services like keycloak, gc-notify, redis, rabbitmq for example.

Future development iterations on data displayed per project could also include application health. In other words, are the containers in a given production environment in a basic healthy state.

The user base for this application will include a wide array of computer skills, therefore making this application as simple as possible to display, create and edit information is being stressed by the IMB Senior Leadership Team (SLT).

## Personas

**Berenice** A director within IMB that is fairly new to the branch, but has worked with BC Government for 10+ years. She has experience with software development projects as she was previously a Product Owner for a project that had a successful production launch. She currently manages UI/UX and SCRUM Master resources and would like to know at a glance who is resourced on what project. She understands Agile philosophy and knows that a solution may take many iterations to achieve a desired state of functionality.

**Alan** A DevOps resource that has worked for IMB for the last 3 Years. He has worked on many projects, including from inception to maintainance lifecycles for IMB, setting up deployment pipelines and integrating technologies into projects that help increase developer velocity. He actively engages the developer community to understand their ever changing needs from project to project. Alan is currently looking to build a tool that allows product owners/stakeholders within IMB to understand resource utilization across all projects within IMB to help avoid developer/resource burn-out.

**Both IMB Employees** are looking for a tool that offers all users within IMB easily digestible data based on the bredth and depth of the many projects they currently develop and maintain, as well as projects that are on the horizon for IMB. Displaying exactly the right amount of information at a glance is paramount to both Berenice and Alan.


## User Stories


### One

As Berenice, I want to be able to add a project to the list of projects that IMB is developing or maintaining.

**Acceptance Criteria**
Given that I am Berenice
And I am aware of a new development project within IMB
When I got to the project dashboard
I can click a button 
And the application takes me to a basic "Create Project" form
And I can click a submit button to save this data

### Two

As Berenice, I want to see a list of all projects that IMB currently develops or maintains in a dashboard

**Acceptance Criteria**
Given that I am Berenice
And I am trying to see a list of all projects within IMB
When I navigate to the application landing page
I can see a list of all projects within IMB
And all relevant information related to each project

### Three

As Alan I want to be able to add/edit project related information

**Acceptance Criteria**
Given that I am Adam
And I want edit details related to a specific project
When I click on an edit button found at the end of a row within a dashboard
I am redirected to a simple form that displays all of a given projects details
And allows me to edit and submit those such that they are persistent

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
| Pass/Accetable          | * RESTful                                                              |
|                         | * Container builds without error                                       |
|                         | * Endpoints return http responses required for given CRUD action       |
|                         | * Basic error handling present                                         |
|                         | * Can handle basic Create (POST), Read (GET), and update (PUT) actions |
|                         | * Basic swagger documentation of each end-point found at /api-docs     |
| Fail/Unacceptable       | * Container does not build, or builds with warnings/errors             |
|                         | * More than one requirement of Good/Acceptable are not met             |

### Frontend Component
| Rating                  | Criteria                                                                                            |
|-------------------------|-----------------------------------------------------------------------------------------------------|
| Pass/Accetable          | * Container builds without error                                                                    |
|                         | * Non-monolithic components                                                                         |
|                         | * Functional or Class based component design based on requirement                                   | 
|                         | * Appropriate naming of components, elements, classes, etc.                                         |
|                         | * Basic error handling when interacting with API                                                    |
|                         | * Comments when needed/appropriate                                                                  | 
|                         | * Utilizes API to perform required Create (POST), Read (GET) and update (PUT) actions when required |
| Fail/Unacceptable       | * Container does not build, or builds with warnings/errors                                          |
|                         | * More than one requirement of Good/Acceptable are not met                                          |

### Database Component
| Rating                  | Criteria                                                                                            |
|-------------------------|-----------------------------------------------------------------------------------------------------|
| Pass/Accetable          | * Utilizes Docker/Docker Compose to instantiate local database container                            |
|                         | * Basic migration script is applied via automation to create basic schema for implemented solution  |
|                         | * Create, Read and Update actions are reflected in database                                         |
| Fail/Unacceptable       | * Any of the requirements of Good/Acceptable are not met                                            |

### Documentation 
| Rating                  | Criteria                                                                                                    |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| Pass/Acceptable         | * Utilizes repository root level README.md to document commands to get project running on local environment |
|                         | * Component based documentation is found within the README.md found within /src/backend or /src/frontend    |
| Fail/Unacceptable       | * No documentation is provided with solution                                                                |

### BONUS - Quality Assurance
| Rating                  | Criteria                                                                                                        |
|-------------------------|-----------------------------------------------------------------------------------------------------------------|
| Points awarded if       | * (One point) API comes with one or more unit tests and relevant documentation on how to run the suite of tests |
|                         | * (One points) Frontend contains one or more unit tests that proove that components render correctly, and 
|                         |    relevant documentation required to run the suite of tests                                                    |
| Points not awarded if   | * Criteria for either API or Frontend is not met                                                                |

### BONUS - CI/CD Strategy into Cloud Platform
| Rating                  | Criteria                                                                                                        |
|-------------------------|-----------------------------------------------------------------------------------------------------------------|
| Points awarded if       | * (Two points) Documentation provided with solution outlines a basic CI/CD strategy of how to build, tag push   |
|                         |   and deploy a container image into a cloud platform. Documentation can include diagrams when required.         |
| Points not awarded if   | * Documentation is not provided or does not accurately portray actions/technologies required to create a basic  |
|                         |   CI/CD pipeline                                                                                                |

### Wiki Documentation
| Rating                  | Criteria                                                                                                        |
|-------------------------|-----------------------------------------------------------------------------------------------------------------|
| Points awarded if       | * (One points) Basic decisions outline development process are documented and placed within the repository to be|
|                         |   consumed by other developer resources. Documentation is clear and concise, using plain language when possible |
|                         |   and diagrams if/when necessary                                                                                |
| Points not awarded if   | * Documentation is not provided or is overly verbose and not easily consumable                                  |
