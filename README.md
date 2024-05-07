This project is meant to demonstrate the usage of continuous integration and continuous delivery (CI/CD) using Jenkins as a tool to automate the delivery of an application.

### Step 1) Install Docker, docker-compose and Jenkins on node/host
You can follow this [link](https://www.jenkins.io/doc/book/installing/linux/) for Jenkins installation.

To Install docker and docker-compose use the commands mentioned below
```
sudo apt-get update
sudo apt-get install docker.io
sudo apt-get install docker-compose
```
#### Once jenkins is installed configure it using admin password and create new admin user login to the console and follow below steps

### 2) Setup and configure the job by following the instructions
####   Click on the **New Item** button on to create the job
![image](https://github.com/jayeshrajputtech/react-django-todo-app/assets/166933906/5f9eb9e6-8e51-4140-9f63-a293b6337e3b)

####   Name your job whatever you like and select **Freestyle project** then click on **OK** button
   ![image](https://github.com/jayeshrajputtech/react-django-todo-app/assets/166933906/1657836d-1765-4600-9502-3273935f7b34)
#### Provide description and select GitHub Project checkbox also provide the GitHub project url which you directly copy from browser link.
![image](https://github.com/jayeshrajputtech/react-django-todo-app/assets/166933906/26167990-4ac3-4cb3-817a-8e1cf21f6cde)

#### In source code management (SCM) select Git and provide the repoitory url of the project's repo
![image](https://github.com/jayeshrajputtech/react-django-todo-app/assets/166933906/de034300-559e-4e9b-9471-2c60a6588b0f)

#### Mention the name of the branch of the source code that you have to test and build
![image](https://github.com/jayeshrajputtech/react-django-todo-app/assets/166933906/d75a5123-f886-4708-890a-ffbb7cbf61de)

#### In Build Steps select the 
### 3)
#### Jenkins create seperate workspace for each project or Job that we create on Jenkins in /var/lib/jenkins/workspace/ directory with the job name when we build the job for first time
### React Django Todo Application
![image](https://github.com/jayeshrajputtech/react-django-todo-app/assets/166933906/4b3ba86b-4941-4fba-8c6e-e89ce0bca981)
