Detailed Steps
Environment Setup

Install Docker: Ensured Docker was installed and running on my Windows machine. This involved downloading Docker Desktop and following the installation guide to set it up.
Install Git: Installed Git to manage my source code and version control.
Project Initialization

Create Project Directory: Created a local directory named docker-challenge-template.

Repository Cloning: Cloned the given template repository using git clone https://github.com/eduluz1976/docker-challenge-template.git, which includes essential starter files.
Create Dockerfile and Public Directory

Create Public Directory: Created a public directory inside the challenge1 folder to hold the static assets for the web page.
Create index.html: In the public directory, created an index.html file with the following content:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Static Page</title>
</head>
<body>
    <h1>Hello, this is a static page served by Docker!</h1>
    <p>Name: Harjot Singh Salh</p>
    <p>SAIT ID: 901912</p>
</body>
</html>

Write Dockerfile: Created a Dockerfile in the challenge1 directory with the following instructions:

FROM nginx:alpine
COPY public /usr/share/nginx/html

This file instructs Docker to build an image based on the lightweight nginx:alpine image and copies the contents of the public directory to Nginx's serving directory in the container.

Build the Docker Image
Docker Build Command: Executed docker build -t static-page-server . in the challenge1 directory. This command builds the Docker image named static-page-server from the Dockerfile located in the current directory.


Run the Docker Container
Docker Run Command:To launch the container in detached mode execute the command docker run "-d -p 8080:80 static-page-server". This setup links port 8080 on your computer to port 80 on the container enabling you to access the website at http;//localhost;8080.


Verify the Deployment

Testing the Webpage:I opened a web browser. Went to http;//localhost;8080 to view the HTML page. This was a step to confirm that Nginx was serving the content correctly as anticipated.
Managing. Repositories

Commit Changes: Committed the changes to the local Git repository using git add . followed by git commit -m 'Complete Challenge 1 setup'.
