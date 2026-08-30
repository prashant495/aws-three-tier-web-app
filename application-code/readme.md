Dockerizing a 3-Tier Web Application

As part of my practical project, I worked on Dockerizing a 3-tier web application running on an AWS EC2 instance.

 I started by forking a public 3-tier application from GitHub. The application already had the frontend, backend, and database components, but it was not Dockerized.

My goal was to containerize the complete application and make all three layers work together.

🔹 What I worked on:
 
 . Forked a public 3-tier application from GitHub. 

 . Understood the existing frontend, backend, and database architecture. 

 . Created a Dockerfile for the frontend and used a multi-stage build. 

 . Built the React frontend and used Nginx to serve the production build. 

 . Created a Dockerfile for the backend using Node.js. 

 . Containerized MySQL as the database layer. 

 . Created a single docker-compose.yml to run all three services together. 

 . Created a custom Docker network so containers communicate using service names instead of hardcoded IPs. 

 . Used a Docker volume to persist MySQL data even when containers are removed and recreated. 

 . Configured Nginx to forward API requests from the frontend to the backend. 

 . Improved the setup by keeping the database and backend internal, exposing only the frontend to the public. 

 . Tested the complete flow from browser → frontend → backend → database.


<img width="1336" height="701" alt="image" src="https://github.com/user-attachments/assets/4f11ea36-ac6f-4c1d-80e0-065c7cfe3840" />


<img width="756" height="450" alt="image" src="https://github.com/user-attachments/assets/c5084ca2-988f-4f21-998e-9c31c8d36039" />

<img width="870" height="367" alt="image" src="https://github.com/user-attachments/assets/4f4fb4a8-a7b2-4b68-9334-69a89e3fd7ca" />






