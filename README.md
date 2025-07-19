# MULTI-CLOUD-ARCHITECTURE

*COMPANY* : CODTECH IT SOLUTION

*NAME* : SANTHOSH GOVINDAN

*INTERN ID* : CT06DG1559

*DOMAIN* : CLOUD COMPUTING

*DURATION* : 6 WEEKS

*MENTOR* : NEELA SANTOSH

This project exemplifies a robust multi-cloud architecture, seamlessly integrating a frontend hosted on Amazon Web Services (AWS) Simple Storage Service (S3) with a backend powered by an Azure Function. This approach highlights the flexibility and interoperability achievable when leveraging distinct cloud providers for different components of an application.

## Architecture Overview

The core of this multi-cloud solution revolves around two primary components:

* **Frontend (AWS S3)**: The user interface, a simple HTML page named `index.html`, is securely stored and served from an AWS S3 bucket. AWS S3 is chosen for its excellent capabilities in static website hosting, providing high availability, scalability, and cost-effectiveness for delivering web content.
* **Backend (Azure Function)**: The business logic and data processing are handled by an Azure Function. Azure Functions provide a serverless compute service, allowing developers to run code without provisioning or managing infrastructure. This is ideal for event-driven architectures and provides scalability on demand.

## Functional Breakdown

The `index.html` file, deployed on AWS S3, presents a user-friendly interface with a button. Upon a user clicking this button, a JavaScript function embedded within `index.html` initiates an asynchronous network request. This request is directed to the backend Azure Function's specific API endpoint. The Azure Function then processes the request, performs any necessary operations, and returns a response. This response is subsequently received by the frontend and dynamically displayed on the webpage, providing immediate feedback to the user.

## Deployment Specifics

### AWS S3 (Frontend)

The `index.html` file, which forms the frontend of this application, is hosted within an AWS S3 bucket named `multi-cloud-demo-frontend`. This bucket is provisioned in the Europe (Stockholm) eu-north-1 region, ensuring data residency and potentially lower latency for users in that geographical area. The `index.html` file, with a size of 373 B, was last modified on July 2, 2025, at 00:23:52 UTC+05:30. The publicly accessible URL for the frontend is `https://multi-cloud-demo-frontend.s3.eu-north-1.amazonaws.com/index.html`.

### Azure Function (Backend)

The backend component is an Azure Function App, uniquely identified as `awsbackendfunction`. This function is strategically deployed in the Canada Central region, which is its designated location for execution. Operating on a Flex Consumption plan, the Azure Function is designed to scale dynamically based on demand, optimizing cost by only charging for the compute resources consumed during execution. It is allocated 2048 MB of instance memory to support its operations. The default domain name for this Azure Function is `awsbackendfunction-ederbff2eycwhybq.canadacentral-01.azurewebsites.net`, providing a stable endpoint for frontend communication. The precise API endpoint invoked by the frontend is `https://awsbackendfunction-ederbff2eycwhybq.canadacentral-01.azurewebsites.net/api/awsResponder?code=xeYLzbnFNGkm9OOtH-EDEJoMMTGHSA2DQiSCIpqSJOKyAzFuIx3L7w==`.

## Implementation and Execution

To replicate or run this multi-cloud application, the following steps are essential:

1.  **Frontend Deployment**: The `index.html` file must be uploaded to an AWS S3 bucket that is correctly configured for static website hosting. This involves enabling static website hosting for the bucket and setting the index document to `index.html`.
2.  **Azure Function Deployment**: The backend code for the Azure Function needs to be deployed to an Azure Function App. This includes ensuring all necessary dependencies and configurations are in place for the function to execute correctly.
3.  **Endpoint Verification**: Crucially, the `fetch` URL within the `index.html` file's JavaScript code must be updated to accurately point to the specific API endpoint of your deployed Azure Function. Any mismatch here will result in communication failures between the frontend and backend.

This demonstration effectively illustrates the power and flexibility of a multi-cloud strategy, enabling developers to select the best-of-breed services from different providers to build robust and scalable applications.

## OUTPUT
