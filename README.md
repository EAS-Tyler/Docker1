# My First View at Docker

Here I:
- Created a Dockerfile
    - Must be named "Dockerfile" with no extension 
    - Contains commands such as FROM, COPY, EXPOSE and CMD
    - A blueprint that tells docker how to build an image
- Created a basic index.html to test my docker application
    - Copied from my machine into my container using COPY command in Dockerfile
- Created a docker-compose.yml to automate the launching and configuring of my container - This was however very basic (one container), so I have decided to start another project using a multi-container docker application with use of docker-compose
- Made notes on the aspects of Docker and some of its commands (Can be found in Academy-journal repo)