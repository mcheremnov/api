# Go Project 🚀

## Prerequisites
Ensure you have the following installed:
- **Go**: [Download Go](https://go.dev/dl/)
- **Docker**: [Get Docker](https://docs.docker.com/get-docker/)

## Setup Instructions

### 1️⃣ Clone the Repository
```sh
git clone https://github.com/mcheremnov/api.git
cd api
```

### 2️⃣ Configure Environment Variables

```sh
cp .example.env .env
```

### 3️⃣ Create and Start PostgreSQL & Redis Containers

```sh
docker run --name postgres \
  -e POSTGRES_USER=youruser \
  -e POSTGRES_PASSWORD=yourpassword \
  -p 5432:5432 -d postgres

docker run --name redis \
  -p 6379:6379 -d redis

```
⚠️WARNING⚠️ Do not forget to change variables in .env file with your variables above!!!

### 4️⃣ Start All Containers

To start all stopped containers, run:
```sh
docker start $(docker ps -aq)
```

### 5️⃣ Run the Go Project
```sh
go run main.go 
```
