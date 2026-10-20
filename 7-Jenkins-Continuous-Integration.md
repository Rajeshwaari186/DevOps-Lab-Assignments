Exercise 7: Introduction to Continuous Integration (CI) and Jenkins Installation

Objective

Understand the concept of Continuous Integration (CI), install and configure Jenkins, and learn how Jenkins automates software development and testing workflows.

Introduction to Continuous Integration (CI)

Continuous Integration is a software development practice in which developers frequently integrate code changes into a shared repository. Each integration can trigger automated builds and tests to identify errors early, improve software quality, and accelerate development.

Key Features of CI

- Frequent code integration.
- Automated building and testing.
- Early detection of errors.
- Improved software quality.
- Faster development and feedback.
- Reduced integration issues.

What is Jenkins?

Jenkins is an open-source automation server used to automate software building, testing, and deployment. It supports Continuous Integration and Continuous Delivery (CI/CD) through pipelines and plugins.

Tools and Technologies

- Jenkins
- Java (JDK)
- Git
- GitHub
- Web browser
- Operating System: Windows

Jenkins Installation and Configuration

Step 1: Install Java

Install a Java Development Kit (JDK) compatible with the Jenkins version being used. Verify the installation using:

java -version

Step 2: Install Jenkins

Download and install Jenkins using the official website:

https://www.jenkins.io/download/

Follow the installation instructions for the operating system.

Step 3: Start Jenkins

Start the Jenkins service and open the Jenkins web interface in a browser:

http://localhost:8080

Step 4: Unlock Jenkins

Retrieve the initial administrator password from the location specified by the Jenkins installer. Enter the password in the setup screen.

Step 5: Configure Jenkins

Install the suggested plugins and create an administrator account. Complete the initial setup wizard.

Step 6: Verify Installation

Open the Jenkins dashboard and verify that Jenkins is running and ready to create jobs.

Continuous Integration Workflow

1. A developer commits code to GitHub.
2. Jenkins detects or receives notification of the code change.
3. Jenkins checks out the source code.
4. Jenkins builds the application.
5. Automated tests are executed.
6. Jenkins reports the build result.

Screenshots

Add screenshots of the following steps to demonstrate your work:

1. Java installation verification using "java -version".
2. Jenkins installation or service status.
3. Jenkins initial setup or unlock screen.
4. Jenkins dashboard after successful configuration.

Expected Outcome

- Understand the fundamentals of Continuous Integration.
- Learn the purpose and features of Jenkins.
- Install and configure Jenkins successfully.
- Access the Jenkins dashboard.
- Understand how Jenkins supports automated build and test workflows.

Conclusion

This exercise introduces Continuous Integration and Jenkins as an automation tool. It demonstrates the basic installation and configuration process and explains how Jenkins helps automate software development workflows, improve code quality, and detect errors early.

References

- Jenkins Official Website: https://www.jenkins.io/
- Jenkins Documentation: https://www.jenkins.io/doc/
- GitHub: https://github.com/

Technologies Used

Jenkins | Java | Git | GitHub | CI/CD
