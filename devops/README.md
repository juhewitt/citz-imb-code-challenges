# citz-imb-code-challenges

## Instructions for IS-X DevOps Position

Create a dockerfile to build the Expressjs API included in a sample repository. Then create a docker-compose that utilizes the dockerfile you developed such that you can
run `docker-compose up --build [NAME_OF_API_CONTAINER]` in terminal.

Create a kubernetes manifest to deploy the Expressjs API included in a sample repository into a cloud container platform. Your manifest should include a readiness and liveness probe that utilizes the `/api/health` endpoint included in API. 

The kubernetes template should be accompanied by a deployment pipeline, using a technology of your choice.

In order to move forward to an interview, you must demonstrate deployment knowledge in the following areas included in your solution:

* Kubernetes templates for basic kubernetes objects like deployment configs, pods, services and routes
* Docker/Dockerfiles and how to utilize them at scale
* Deployment pipelines using technologies like Github Actions or Openshift Tekton pipelines

### Important!

**Your solution will not be evaluated if it works against a local working machine.**

Instead, if your solution passes evaluation criteria, you will be responsible for a working demo of how to deploy the API to a cloud container platform in a 15 minute block of the interview that will follow this technical assignment.

Points for a solution that is not able to be deployed without issue will be docked. Working solutions without issue that can resolve the Swagger documentation of the Express API to a publically exposted URL will receive 100% of the marks associated to this demo.

### Opportunity to Score Additional Points if a Working Solution is Submitted

There will be no opportunities for bonus points after the submission of your solution.

### Solution Presentation in Interview Stage

If you are selected to proceed to the interview stage of this competition, you will be asked to demostrate your solution in a Sprint Review style demo (10-15 minutes in length) to a panel of stakeholders. You will be expected to demonstrate the automated pipeline you developed to push a deployed image of the Expressjs API to an environment. Stakeholders should be provided with the URL of where to reach the API's Swagger documentation online. 

## What to Submit

Firstly, create a GitHub repository using your GitHub Account. The name of the repository should use the following convention:

your_first_name-your_last_name_-IS24-full_stack_competition_requisition_number

Your working solution should be present on the **main** branch of the repository. Please trim or remove any extraneous branches prior to submission.

### Dockerfile Component

The Dockerfile created for this assignment should produce a working image of the Expressjs API that accompanies this README. The Dockerfile should be utilized by a docker-compose file found at the root of your submission. The name of the container should be simple and easy to read.

### Pipeline Component

Your pipeline should have the following steps:

* A build, tag and push step that places your docker image into a repository. This repository could come in the form of the following:
    * Artifactory repository
    * Docker hub repository
    * Imagestream within a Tools Namespace in an Openshift cluster
* A step that deploys the image into a cloud container environment
* A stage that utilizes the readiness and liveness probes on your kubernetes manifest to return the pod/container status when they are running post-deployment

## Questions

Further clarification on project details can be directed to the following email addresses
* marker1@gov.bc.ca
* marker2@gov.bc.ca
* marker3@gov.bc.ca

Emails should be responded to within an hour of being received during business hours (9am-5pm).
Outside of normal business hours will be best effort, hopefully before end-of-day.

## Assessment Scoring

The following tables will be provided to you via email after marking of your solution is complete.

### Dockerfile/Docker-compose Component
| Rating                  | Criteria                                                                        |
|-------------------------|---------------------------------------------------------------------------------|
| Pass/Acceptable         | * Utilizes single or multi stage build to produce image                         |
|                         | * Readable, commenting when necessary to explain pattern used to produce image  |
|                         | * Produces image of API without warning or error                                |
|                         | * Minimal documentation provided in order to consume docker-compose             |
| Fail/Unacceptable       | * Any of the requirements of Good/Acceptable are not met                        |

### Pipeline Component
| Rating                  | Criteria                                                                        |
|-------------------------|---------------------------------------------------------------------------------|
| Pass/Acceptable         | * Build, tag, push step that places docker image into repository                |
|                         | * Deploys image into cloud container platform of your choice                    |
|                         | * A stage used to report when API is healthy and ready to be consumed           |
|                         | * Pipeline is documented or accompanied by documentation to explain pattern used|
| Fail/Unacceptable       | * Any of the requirements of Good/Acceptable are not met                        |                                                            |
