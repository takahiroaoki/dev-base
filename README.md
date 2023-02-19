# dev-base

## Requirement
- Windows 11
- Docker Desktop for Windows 4.2.0

## Initial setup
1. Execute the following command at project root.
```
$ docker-compose up -d
```
2. Get Access to http://localhost:8080
3. Login with initial password(see "/var/jenkins_home/secrets/initialAdminPassword").
4. Select "Select plugins to install" and select no plugins(we would install plugins later).
5. Make admin user and set the url of jenkins(if you deploy the jenkins server on some location other than localhost).
6. Execute the following command.
```
# At the project root
$ docker-compose exec jenkins /bin/bash

# Install the plugins written in plugins.txt
$ jenkins-plugin-cli --plugin-file /var/jenkins_home/plugins.txt

# Check whether the plugins would be installed.
$ jenkins-plugin-cli --list
```