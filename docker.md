# 🐳 Docker Command Reference

A handy cheat sheet for commonly used Docker commands, complete with examples.

---

## 🔹 Run a Basic Container
`docker run`:  This command is used to create and start a Docker container from a specified image. It's like saying "start this application" in the Docker world. For example,
```bash
docker run mongo
```
starts a MongoDB container using the official MongoDB image from Docker Hub.

## 🔹 Run with Port Mapping
Maps MongoDB's default port so your host can connect to it.
```bash
docker run -p 27017:27017 mongo
```

## 🔹 Run in Detached Mode(Background)
Starts MongoDB in the background, freeing up your terminal.
```bash
docker run -d -p 27017:27017 mongo
```

## 🔹 List Running Containers
Shows currently running containers with details.
```bash
docker ps
```

## 🔹 Stop a Running Container
```bash
docker kill <container_id>
```

## 🔹 Pull an Image from Docker Hub
```bash
docker pull mongo
```

## 🔹 Inspect Container Details
```bash
docker inspect <container_id>
```

## 🔹 Restart a Container
```bash
docker restart <container_id>
```

---

## 🗂 Example Use Case: PostgreSQL

Run a PostgreSQL container with environment variables, port mapping, and volume persistence:

```bash
docker run -d --name postgresdb -e POSTGRES_PASSWORD=mysecretpassword -e POSTGRES_DB=mydatabase -p 5432:5432 postgres
```

## Connection String
`postgresql://<username>:<password>@<host>:<port>/<database>`
```bash
postgresql://postgres:mysecretpassword@localhost:5432/postgres
```
