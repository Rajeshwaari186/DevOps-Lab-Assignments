Exercise 8: Creating a Hello World Jenkins Job

Objective

Create and configure a Jenkins job to execute a simple Hello World shell script stored in a GitHub repository and understand the basics of Jenkins job automation.

Introduction

Jenkins is an open-source automation server used for Continuous Integration and Continuous Delivery (CI/CD). It allows developers to automate tasks such as building, testing, and executing scripts.

In this exercise, a shell script named "hello-world.sh" is stored in GitHub and executed through a Jenkins job.

Tools and Technologies

- Jenkins
- Git and GitHub
- Shell scripting
- Web browser
- Java (JDK)

Implementation Steps

Step 1: Create a GitHub Repository

1. Log in to GitHub.
2. Create a new repository named "devops-sample-code".
3. Add a file named "hello-world.sh".

Step 2: Create the Shell Script

Add the following content to "hello-world.sh":

#!/bin/bash
echo "Hello World"
echo "Jenkins job executed successfully!"

Save and commit the file to the repository.

Step 3: Configure Jenkins

1. Open the Jenkins dashboard at "http://localhost:8080".
2. Click New Item.
3. Enter the job name "Hello-World-Job".
4. Select Freestyle project and click OK.

Step 4: Configure Source Code Management

1. Open the job configuration page.
2. Under Source Code Management, select Git.
3. Enter the URL of your GitHub repository.
4. Configure the branch to build, such as "*/main".
5. Save the configuration.

Step 5: Configure the Build

1. Under Build Steps, select Execute shell if available on your Jenkins agent.
2. Enter the following command:

bash hello-world.sh

If the script is located in the checked-out repository root, Jenkins will execute it from the workspace.

Step 6: Execute the Job

1. Click Save.
2. Select Build Now.
3. Open Build History.
4. Click the build number.
5. Select Console Output to view the execution results.

Expected Output

Hello World
Jenkins job executed successfully!
Finished: SUCCESS

The output above is expected when the script runs successfully.

Screenshots

Add screenshots of the following:

1. GitHub repository containing "hello-world.sh".
2. Jenkins job configuration.
3. Jenkins build history showing the completed build.
4. Console Output displaying the Hello World message and successful build status.

Expected Outcome

- Create a shell script and store it in GitHub.
- Configure a Jenkins Freestyle project.
- Retrieve source code from a GitHub repository.
- Execute a shell script through Jenkins.
- Verify the build result using Console Output.

Conclusion

This exercise demonstrates how to create and execute a basic Jenkins job using a shell script stored in GitHub. It introduces source code management, build configuration, job execution, and output verification in a CI workflow.

References

- Jenkins: https://www.jenkins.io/
- Jenkins Documentation: https://www.jenkins.io/doc/
- GitHub: https://github.com/

Technologies Used

Jenkins | Git | GitHub | Bash | CI/CD
