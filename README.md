# CDAAS Candidate Assignment

This assignment has two parts designed to assess your skills in CI/CD pipeline setup and GitLab Runner configuration. You can do both parts independently.

## Tools & Technologies:

- **GitLab** (CI/CD tool)
- **Docker**
- **GitLab Runner**

---

## Before You Start:
- You will receive a zip file with the assignment code in your email. 
- This is a simple java application. The contents of the application do not really matter. You only need some basic knowlegde of java and maven to build and run it.

Next to this, you will need a:

### GitLab Account:
1. If you don’t have one, [create a GitLab account](https://gitlab.com) (free, no credit card required).
2. Once signed up, create a new group in GitLab to organize your project.

---

## Part 1: Set Up a CI/CD Pipeline for a Dockerized Application

### Instructions:

### 1. Create a Project in your gitlab group and push the application code to the project:
- Push the application code provided to you into your GitLab project.

### 2. Dockerize the Application:
- Create a `Dockerfile` to containerize the application.
- Ensure that the Docker container can run the application without issues.

### 3. Set Up a GitLab CI/CD Pipeline:
- Create a `.gitlab-ci.yml` file to define your CI/CD pipeline.

### The pipeline should include the following stages:
- **Build**: Build the application from the source code.
- **Test**: Run unit tests against the built application.
- **Publish**: 
  - Build a Docker image for the application.
  - Push the Docker image to a Docker registry (e.g., Docker Hub, AWS ECR, etc.).
  - **Note**: Do not push the image to GitLab’s container registry.

### Notes:
- You can use GitLab’s shared runners, or if you already have the private runner from part 2 set up, feel free to use that.
- Ensure that each stage is properly defined and that the pipeline runs successfully.
- Make sure your code is readable, and documentation is available if needed

---

## Part 2: Set Up a Private GitLab Runner

### Instructions:

### 1. Set Up GitLab Runner:
- Set up a GitLab Runner on a self-hosted machine (this could be a VM or your local machine).
- Follow GitLab's official documentation for setting up the runner.

### 2. Runner Configuration:
- Register the runner to your GitLab account.
- Ensure that the runner uses the Docker executor for running jobs.

### 3. Test the Runner:
- Verify that your runner is working by triggering the pipeline from Part 1.
- Ensure that the runner executes the pipeline stages successfully (i.e., builds the app, runs tests, and publishes the Docker image).

### 4. Automate runner setup
- to explain/reproduce your runner setup, use a tool to automate this part. You can use any tool you like (for example, ansible).
---

## Additional Notes:

### Documentation:
- You can refer to the following GitLab official documentation for assistance:
  - [GitLab CI/CD Documentation](https://docs.gitlab.com/ee/ci/)
  - [GitLab Runner Documentation](https://docs.gitlab.com/runner/)
  - [GitLab CI/CD Syntax Reference](https://docs.gitlab.com/ee/ci/yaml/)

### Docker Registry:
- You can use Docker Hub, GitHub Packages, or any other public/private Docker registry to store your Docker image.

### Security:
- Ensure that no sensitive information (e.g., Docker registry credentials) is exposed in your GitLab CI configuration. 
- You can use GitLab CI/CD variables to manage secrets securely.

---

## Deliverables:

- Mail us a link to your GitLab repository for us to review, or alternatively send us a zip of your code.
