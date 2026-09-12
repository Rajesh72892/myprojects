 DevOps Deployment Report

1) Project Name: Docker HTML Web Application

2) application Description: This project is a simple HTML web application running inside a Docker container. The application uses Nginx as the web server and displays a basic HTML page.

3) Tools Used: AWS EC2, Git, git hub, docker , nginx, Linux commands

4) GitHub Repository Information

            Repository: 'myprojects'

            git hub: https://github.com/rajesh72892/myprojects

5) Docker Image Information

            Image Name: 'index.html'
            Base Image: 'nginx:alpine'

6) Container Information

            Container Name: 'my-web-app'

            Port Mapping: '8080:80'

        The container was started using: docker run -d --name my-web-app -p 8080:80 my-html-app

7) How the Application Was Started 
   The Docker container was started with:  docker start my-web-app

   The application was tested locally using: curl http://localhost:8080

    The application can also be accessed through the EC2 public IP using: http://54.91.170.15:8080

 8) how logs checked: 
      Application/container logs were checked using: docker logs my-web-app

9) One Problem/Error Scenario

One possible failure scenario is that the application may not be accessible because the Docker container has stopped.

For example, if the container is stopped:  docker stop my-web-app

the application will no longer be available.

Another possible issue is that port 8080 may not be allowed in the AWS EC2 Security Group.

10) How the Problem Could Be Investigated

    1: Check running containers: docker ps -a

    2: Check container logs : docker logs my-web-app

    3: Check the application locally  : curl http://localhost:8080

    4: Check the Docker image : docker images

    5: Check the AWS Security Group Verify that TCP port "8080"is allowed for the EC2 instance.

    6: Restart the container: docker start my-web-app

Then test the application again.

11) What I Learned From the Internship Tasks

During these DevOps internship tasks, I learned how to work with Linux commands, Git and GitHub, Docker, AWS EC2, and GitHub Actions.
I learned how to create and manage files and directories in Linux, use Git branches and Pull Requests, build Docker images, run and manage containers, check container logs, and troubleshoot basic application issues.
I also learned how GitHub Actions can automatically run a workflow whenever code is pushed to a GitHub repository.
These tasks helped me understand the basic DevOps workflow of managing source code, containerizing applications, deploying them on AWS, and automating processes using CI/CD tools.
