In this project, I utilized Docker to containerize a Node.js application, MongoDB, and Mongo Express, creating a seamless, efficient development environment. The architecture consists of two primary containers: one for MongoDB and another for Mongo Express, alongside the Node.js application serving a login page.

Key Features:
MongoDB Container:

Deployed using a Docker container to host the database, which stores user credentials.
Docker volumes are used to ensure persistent storage of the data, even when the container is deleted or recreated.
Mongo Express Container:

A lightweight web-based administrative interface for MongoDB, deployed using Docker.
Provides a user-friendly UI for managing and interacting with the data stored in MongoDB.
Node.js Application:

A simple login page built using Node.js, featuring email, username, and password input fields.
The login data is sent to MongoDB and securely stored, making use of Docker’s persistent volumes to keep the data intact across container restarts.
Docker Volumes:

Used to store MongoDB data on the host machine, ensuring that user information persists even if the MongoDB container is stopped or removed.
Login Functionality:

The Node.js application processes user login requests, storing the login data (username, email, and password) in the MongoDB database.
Multi-Container Setup:

Managed using Docker Compose to orchestrate the deployment and simplify the setup.
The MongoDB container is connected to the Mongo Express container for real-time data management.
The Node.js container communicates with the MongoDB container to store and retrieve user data.
Benefits:
Data Persistence: Thanks to Docker volumes, the MongoDB container's data persists even after the container is destroyed or recreated.
Easy Deployment: The multi-container setup via Docker Compose allows for quick, easy deployment and scaling.
Simplified Management: Mongo Express provides an intuitive, web-based UI for managing the MongoDB database, reducing the complexity of working with the database.
Technologies Used:
Docker
Node.js (for backend)
MongoDB (for data storage)
Mongo Express (for database management)
Docker Compose (for multi-container orchestration)
This project demonstrates how Docker can be used effectively to deploy multiple interconnected services while ensuring the persistence of critical data across container lifecycles.
