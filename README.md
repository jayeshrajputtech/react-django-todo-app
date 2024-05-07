This project is meant to demonstrate the usage of continuous integration and continuous delivery (CI/CD) using Jenkins as a tool to automate the delivery of an application.

### Step 1) Install Docker, docker-compose and Jenkins on node/host
You can follow this [link](https://www.jenkins.io/doc/book/installing/linux/) for Jenkins installation.

To Install docker and docker-compose use the commands mentioned below
```
sudo apt-get update
sudo apt-get install docker.io
sudo apt-get install docker-compose
```
#### Once Jenkins is installed configure it using the admin password create a new admin user login to the console and follow the below steps

### 2) As we are using docker as a build tool jenkins service user needs to access the docker service to perform the job for that use these commands to add jenkins user to the docker group
```
sudo usermod -aG docker jenkins
```
Reboot the system to apply the changes
```
sudo reboot
```

### 3) Setup and configure the job by following the instructions
####   Click on the **New Item** button on to create the job
![image](https://github.com/jayeshrajputtech/react-django-todo-app/assets/166933906/5f9eb9e6-8e51-4140-9f63-a293b6337e3b)

####   Name your job whatever you like and select **Freestyle project** then click on **OK** button
   ![image](https://github.com/jayeshrajputtech/react-django-todo-app/assets/166933906/1657836d-1765-4600-9502-3273935f7b34)
#### Provide a description and select the GitHub Project checkbox also provide the GitHub project URL which you directly copy from the browser link.
![image](https://github.com/jayeshrajputtech/react-django-todo-app/assets/166933906/26167990-4ac3-4cb3-817a-8e1cf21f6cde)

#### In source code management (SCM) select Git and provide the repository URL of the project's repo
![image](https://github.com/jayeshrajputtech/react-django-todo-app/assets/166933906/de034300-559e-4e9b-9471-2c60a6588b0f)

#### Mention the name of the branch of the source code that you have to test and build
![image](https://github.com/jayeshrajputtech/react-django-todo-app/assets/166933906/d75a5123-f886-4708-890a-ffbb7cbf61de)

#### In Build Steps select the Execute shell option to provide pre-build, build and post-build shell commands then click on the save button to save the configuration changes. The very first task that Jenkins performs is to clone the GitHub repository in the respective workspace of the job that it created in /var/lib/jenkins/workspace/
![image](https://github.com/jayeshrajputtech/react-django-todo-app/assets/166933906/583fae1b-700f-4efb-8956-e2c134800058)

### 4) Click on the Build Now button to trigger the job to start and once all the commands are executed click on the Build Number button to view the details
![image](https://github.com/jayeshrajputtech/react-django-todo-app/assets/166933906/2c5968fa-a4b3-42d1-bf6d-ccd65107dc62)

### 5) Click on the Console Output button to view the output that the commands generated from the shell
![image](https://github.com/jayeshrajputtech/react-django-todo-app/assets/166933906/9a909bbe-e1ab-4ddd-9ade-868647727d64)

### 6) View the console output a blue tick symbolizes a successful build of the job
![image](https://github.com/jayeshrajputtech/react-django-todo-app/assets/166933906/9cb323b6-d43a-4701-8ab2-efc232ef4ce8)
![image](https://github.com/jayeshrajputtech/react-django-todo-app/assets/166933906/7b151a8d-2675-44f3-bb6e-22cde18f58f5)



#### Jenkins creates a separate workspace for each project or Job that we create on Jenkins in /var/lib/jenkins/workspace/ directory with the job name when we build the job for the first time
### React Django Todo Application
![image](https://github.com/jayeshrajputtech/react-django-todo-app/assets/166933906/4b3ba86b-4941-4fba-8c6e-e89ce0bca981)
