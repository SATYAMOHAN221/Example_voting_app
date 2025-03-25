EXAMPLE VOTING APP:
A simple distributed application running across multiple Docker containers.


Download Docker Desktop for Mac or Windows. Docker Compose will be automatically installed. On Linux, make sure you have the latest version of Compose.

This solution uses Python, Node.js, .NET, with Redis for messaging and Postgres for storage.

Run in this directory to build and run the app:

>>docker compose up
The vote app will be running at http://localhost:8080, and the results will be at http://localhost:8081.

Alternately, if you want to run it on a Docker Swarm, first make sure you have a swarm. If you don't, run:

>>docker swarm init
Once you have your swarm, in this directory run:

>>docker stack deploy --compose-file docker-stack.yml vote
