# README

IRIS Systems Task 1

Pack [the rails application](https://github.com/VithikShah/Shopping-App-IRIS) in a docker container image.

To run the container

 1. docker build -t task_2:v1 .
 2. docker compose up
 3. Go to localhost:8080 to see the app
 
 References
 1. https://github.com/VithikShah/Shopping-App-IRIS
 2. https://youtu.be/a-jcTib9ZPA

 Steps to make the dockerised application
  1. First, I made a Dockerfile in the application directory.
  2. Then, I took a ruby base image.
  3. Then, I installed all the requires packages.
  4. Then, all the dependecies were installed.
  5. Then, I made an entrypoint.sh file which removes any potentially pre-existing server.pid for rails.
  6. In the Dockerfile, this is compiled and run in the bash.
  7. I created a docker-compose.yml file which starts 2 containers, one for application and the other for database. 
  8. I am setting the environment variables in docker-compose.yml file which are used by the database.yml to connect to the database container.
  9. The database and the application are communicating through docker internal network named task_2_default.
  10. I also created a volume for the app.

 
