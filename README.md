# Dockerized 3-Tier Application
This is a fully functional example of a three-tier multi-container application. It includes React for the frontend, Flask for the backend, and PostgreSQL as the database, all orchestrated by the Nginx reverse proxy.

## How it Works
When a request from an external user hits the Nginx web server on port 80, the request is served based on the URL. The React code routes the request to the Flask backend server through nginx reverse proxy. The Flask Docker container is running and exposes port 5000. These settings are defined in the nginx.conf file, enabling Nginx to be aware of both frontend and backend services. The Flask container communicates with the PostgreSQL database on port 5432 for any requests requiring database operations.

**Note:** Ensure that you have Docker,Docker-compose, Node, and **<a href="https://docs.npmjs.com/downloading-and-installing-node-js-and-npm" target="_blank">**npm**  </a>** installed.

<p align="center">
  <img src="https://github.com/k-mughal/Ansible/assets/18217530/bfaa523b-8e34-42fa-8a55-bfe5712d9cdb">
</p>

## How to use:
- Clone this repo to your workspace
```
git clone https://github.com/k-mughal/dockerized-3-tier-app.git
```
- To execute run the following command
```
-docker-compose up --build
```
- After the application is up and running, open your browser and access it at http://localhost
- To stop the application run the following command
```
docker-compose down
```
