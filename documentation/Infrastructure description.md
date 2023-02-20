## Infrastructure Description

This project requires the following AWS services to run:

- Amazon RDS: This is used to store a Postgres database that holds two tables - `users` and `feeds`.
- Elastic Beanstalk: This is used to deploy and run the Node.js backend server.
- Amazon S3: This is used to store and statically host the Angular front-end project.
- CircleCI: This is used for the pipeline infrastructure.

## CircleCI

This project uses CircleCI for continuous integration and deployment. The configuration file for CircleCI is located at `.circleci/config.yml`. The pipeline includes the following steps:

- Build and test the application code.
- Deploy the application to Elastic Beanstalk.

## Architecture Diagram

![Architecture Diagram](/path/to/architecture-diagram.png)

## Screenshots

### Screenshot 1

![Screenshot 1](/path/to/screenshot1.png)

### Screenshot 2

![Screenshot 2](/path/to/screenshot2.png)
