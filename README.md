# Azure-CICD-Devops-Project-Excercise


### Project Overview

This project demonstrates an end-to-end Continuous Integration and Continuous Delivery/Deployment (CI/CD) workflow for Azure Data Factory using Azure DevOps. It automates the validation, version control, and deployment of data pipeline changes across Development, Testing/QA, and Production environments.

### Business Problem

Managing Azure Data Factory pipelines manually across multiple environments can lead to deployment errors, inconsistent configurations, limited version control, and delays in releasing updates.

This project addresses these challenges by implementing an automated CI/CD process that improves deployment consistency, traceability, collaboration, and release management.

### Project Objectives

- Automate data pipeline deployments across Development, QA, and Production.

- Implement Git-based version control and branch management.

- Use pull requests to support code reviews and controlled integration.

- Automate deployment using Azure DevOps pipelines.

- Promote reusable Azure Resource Manager (ARM) templates and environment-specific parameters.

- Reduce manual intervention and deployment errors.

Architecture Overview



The architecture illustrates how data Engineer and  developers manage Azure Data Factory changes through Git branches and promote approved changes through Azure DevOps into the target environments.


### Key Components

| Component                    | Purpose|
|------------------------------|--------|
|Azure Resource Group          | Organizes and manages Azure resources.|
|Azure Data Factory            | Develops and executes data integration pipelines|.
|Git Repository                | Stores source code and tracks changes.|
|Feature Branches              | Isolates development work before integration|
|Pull Requests                 | Enables review and approval of changes.|
|Azure DevOps                  | Orchestrates CI/CD builds and deployment workflows.|
|ARM Templates                 | Define Azure Data Factory resources for deployment.|
|ARM Template Parameters       | Support environment-specific configuration.|
|Deployment Agent              |Executes deployment tasks and communicates with Azure services.|
|QA and Production Environments|Support validation and controlled release of pipeline changes.|



### CI/CD Workflow

#### 1. Development and Version Control

- Developers create or update pipelines in the Development Azure Data Factory environment.

- Changes are committed to the Git repository.

- Feature branches are used to develop and test individual changes independently.

#### 2. Code Integration and Review

- Developers push changes to the relevant feature branches.

- A pull request is created to merge approved changes into the target collaboration branch.

- Reviews and validation checks help ensure that changes meet project require

#### 3. Build and Publish

- Approved changes are integrated into the collaboration branch.

- Azure Data Factory publishing generates deployment artifacts, including ARM templates and parameter files.

- These artifacts are used to deploy the factory configuration to other environments.

#### 4. Continuous Integration and Deployment

- Azure DevOps pipelines automate the deployment workflow.

- The deployment agent executes the required tasks.

- ARM templates and parameter files are used to deploy the Azure Data Factory resources.

- Environment-specific parameters are supplied for the target environment.

#### 5. QA and Production Deployment

- Changes are deployed to the QA environment for validation.

- After the required checks and approvals, the release is promoted to Production.

- Production configuration is managed separately from Development and QA configuration.

#### 6. Validation and Monitoring

- Verify that deployments complete successfully.

- Confirm that deployed pipelines, linked services, datasets, and triggers have the expected configurations.

- Review deployment logs and pipeline execution results.

- Resolve failures before promoting changes to the next environment.

### Technologies Used

- Microsoft Azure

- Azure Data Factory

- Azure DevOps Pipelines

- Git and Azure Repos

- ARM Templates

- JSON parameter files

- CI/CD automation

- Development, QA, and Production environments

### Expected Business Benefits

- Deployment automation: Reduces repetitive manual deployment activities.

- Improved reliability: Promotes consistent deployments across environments.

- Version control: Maintains a history of code changes.

- Better collaboration: Supports branch-based development and pull request reviews.

- Environment separation: Helps prevent unvalidated changes from reaching Production.

- Traceability: Improves visibility into changes and deployment outcomes.

- Scalability: Establishes a repeatable deployment approach for additional data engineering projects.

### Conclusion

This project demonstrates how Azure DevOps CI/CD can streamline the lifecycle of Azure Data Factory solutions. By combining Git version control, pull request reviews, ARM template-based deployments, and environment-specific configuration, the architecture supports reliable, controlled, and repeatable releases from Development through QA to Production.

The approach provides a foundation for implementing DevOps best practices in modern Azure data engineering environments.

