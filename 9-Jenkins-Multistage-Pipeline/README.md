Exercise 9: Jenkins Multi-Stage Pipeline – Deploying a Python Application

Objective

Create and execute a Jenkins Declarative Pipeline that performs multiple stages to build, test, and deploy a sample Python application. This exercise demonstrates how to automate application delivery using Jenkins.

Introduction

Jenkins is an open-source automation server that supports Continuous Integration and Continuous Delivery (CI/CD). A multi-stage pipeline divides the software delivery process into stages, making it easier to automate builds, testing, and deployment.

In this exercise, Jenkins is used to execute a pipeline for a sample Python application.

Tools and Technologies

- Jenkins
- Python
- Git
- GitHub
- Jenkinsfile
- CI/CD Pipeline

Pipeline Stages

1. Checkout: Retrieve the application source code from GitHub.
2. Build: Prepare the application and install required dependencies.
3. Test: Run tests to verify the application.
4. Deploy: Execute the deployment steps for the sample application.

Implementation Steps

Step 1: Create the Application

Create a sample Python application named "app.py".

Example:

def main():
    print("Hello from the Python application!")

if __name__ == "__main__":
    main()

Step 2: Create a Jenkinsfile

Create a file named "Jenkinsfile" in the root of the GitHub repository.

Example Declarative Pipeline:

pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building Python application'
                sh 'python --version'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Python application'
                sh 'python -m py_compile app.py'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Python application'
                sh 'python app.py'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the console output.'
        }
    }
}

Note: This example uses Unix-style shell commands and assumes Python is installed on the Jenkins agent. On Windows agents, use the appropriate "bat" commands.

Step 3: Upload Files to GitHub

Commit the following files to the repository:

- "app.py"
- "Jenkinsfile"

Step 4: Create a Jenkins Pipeline Job

1. Open the Jenkins dashboard.
2. Click New Item.
3. Enter a job name.
4. Select Pipeline and click OK.
5. In the Pipeline section, select Pipeline script from SCM.
6. Select Git and enter the GitHub repository URL.
7. Specify the branch, such as "*/main".
8. Set the script path to "Jenkinsfile".
9. Save the configuration.

Step 5: Execute the Pipeline

1. Open the created Jenkins pipeline job.
2. Click Build Now.
3. Open the latest build.
4. Select Console Output to inspect the results.
5. Verify that the Checkout, Build, Test, and Deploy stages complete successfully.

Expected Output

Checking out source code
Building Python application
Testing Python application
Deploying Python application
Hello from the Python application!
Pipeline completed successfully!

The exact output depends on the pipeline configuration. A successful run should show all configured stages completed without errors.

Screenshots

Add screenshots of the following:

1. GitHub repository containing "app.py" and "Jenkinsfile".
2. Jenkins pipeline configuration.
3. Pipeline stage view showing the completed stages.
4. Console Output showing the execution results and successful build status.

Expected Outcome

- Understand Jenkins Declarative Pipelines.
- Create a multi-stage CI/CD workflow.
- Automate source code checkout and application validation.
- Execute a Python application through Jenkins.
- Verify pipeline execution using the stage view and console logs.

Conclusion

This exercise demonstrates how Jenkins multi-stage pipelines automate the software delivery process. By dividing the workflow into checkout, build, test, and deploy stages, the pipeline improves visibility, consistency, and efficiency in application delivery.

References

- Jenkins: https://www.jenkins.io/
- Jenkins Pipeline Documentation: https://www.jenkins.io/doc/book/pipeline/
- Python: https://www.python.org/
- GitHub: https://github.com/

Technologies Used

Jenkins | Python | Git | GitHub | CI/CD
