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

![udagram-api-hosting](https://user-images.githubusercontent.com/103933344/219711088-7e6ee58f-cc5e-45b2-a170-8531b130623b.png)

## Screenshots

### Last Successful CircleCI Build

![udagram](https://user-images.githubusercontent.com/103933344/220101256-6695d0b0-2762-4b1a-a77f-86bbe447c9f1.png)


### AWS RDS for the Database Overview

![udagram](https://user-images.githubusercontent.com/103933344/219710155-b3791345-6502-4b15-8946-de2ee0ee4b9c.png)


### AWS ElasticBeanstalk for the (Backend) API Deployment

![udagram](https://user-images.githubusercontent.com/103933344/219710604-f36352e1-9852-4d65-a04e-e135d03ddd23.png)


### AWS S3 for (Frontend) Web Hosting

![udagram](https://user-images.githubusercontent.com/103933344/219710829-ee05ff25-4979-45ae-b15a-e43ec1abdeae.png)
