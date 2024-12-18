Voting App
A simple distributed application running across multiple Docker containers.

Getting Started
Download Docker Desktop for Mac or Windows. Docker Compose will be automatically installed. On Linux, make sure you have the latest version of Compose.

This solution uses Python, Node.js, .NET, with Redis for messaging and Postgres for storage.

Run this command in the project directory to build and run the app:

shell
docker compose up
The vote app will be running at http://localhost:8080, and the results app will be at http://localhost:8081.


A front-end web app in Python which lets you vote between two options.

A Redis instance which collects new votes.

A .NET worker which processes votes and stores them in...

A Postgres database backed by a Docker volume.

A Node.js web app which shows the results of the voting in real time.

Notes
The voting application accepts only one vote per client browser. It does not register additional votes if a vote has already been submitted from a client.