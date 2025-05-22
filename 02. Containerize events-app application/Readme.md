# Steps
- Clone the github repo and created Dockerfile in each folder
- Create Dockerhub repos events-api and events-website
- run docker login form the deployemnt server
- form events-api folder

  - docker build -t davabdallah/events-api:latest .

 - form events-website folder

   - docker push davabdallah/events-api:latest
   
- run docker from docker hub
  
  - docker run -d -p 8082:8082 davabdallah/events-api:latest
  - docker run -d -p 8080:8080 -e SERVER='http://localhost:8082' --network="host" davabdallah/events-website:latest
