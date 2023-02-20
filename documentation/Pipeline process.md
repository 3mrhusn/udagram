# Pipeline Process

This markdown file provides an explanation of the `config.yml` file that outlines the pipeline process for a CircleCI workflow. The workflow consists of two jobs, `build` and `deploy`, which are orchestrated by a workflow named `udagram`.

## Jobs

### Build

The `build` job is responsible for building the frontend and backend applications, installing dependencies, and running tests. The job is defined with a `docker` executor that runs on the `cimg/node:14.15` image. The following steps are executed in the `build` job:

1. Install Node and Checkout Code - This step uses the `node/install` Orb to install Node.js version `14.15` and checks out the code from the repository.

2. Install Front-End Dependencies - This step installs the dependencies required for the frontend application using the `npm` package manager.

3. Install API Dependencies - This step installs the dependencies required for the backend API.

4. Front-End Lint - This step runs the linter on the frontend application to check for any syntax or style errors.

5. Front-End Build - This step builds the frontend application.

6. API Build - This step builds the backend API.

### Deploy

The `deploy` job is responsible for deploying the application to Elastic Beanstalk. The job is defined with a `docker` executor that runs on the `cimg/base:stable` image. The following steps are executed in the `deploy` job:

1. Install Node, Elastic Beanstalk, and AWS CLI - This step installs Node.js version `14.15`, sets up the Elastic Beanstalk environment, and configures the AWS CLI.

2. Checkout Code - This step checks out the code from the repository.

3. Deploy App - This step deploys the application to Elastic Beanstalk.

## Workflows

The `udagram` workflow orchestrates the `build` and `deploy` jobs. It consists of three steps, `build`, `hold`, and `deploy`, that are executed sequentially.

1. Build - The `build` job is executed first to build the application and run tests.

2. Hold - The `hold` job is executed next, but only on the master branch. It requires manual approval before proceeding to the `deploy` job.

3. Deploy - The `deploy` job is executed last to deploy the application to Elastic Beanstalk.

This pipeline process ensures that the application is built and tested before it is deployed to Elastic Beanstalk. Manual approval is required before the deployment process starts to prevent any unintended consequences.

## Pipeline Diagram
