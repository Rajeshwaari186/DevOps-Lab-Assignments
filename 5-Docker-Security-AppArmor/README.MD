Exercise 5: Docker Security with AppArmor

Objective

To run a Flask application inside a Docker container and explore Docker security settings and AppArmor restrictions.

Tasks

1. Build and run the Flask application inside a Docker container.
2. Inspect the container's security configuration.
3. Create an AppArmor profile to restrict access to sensitive files and binaries.
4. Use the Docker SDK for Python to apply the AppArmor profile.
5. Test restricted actions, including access to "/etc/passwd" and execution of "/bin/bash".

Application Output

The Flask application displays the following message:

"Hello, this is a secure Flask application running inside a Docker container!"

Tools Used

- Docker
- Python
- Flask
- Visual Studio Code
- GitHub

Note

AppArmor profile enforcement depends on Linux host support. Docker Desktop on Windows may not support loading a custom AppArmor profile directly.
