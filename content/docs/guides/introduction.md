---
title: "Introduction"
description: "Introduction to the JobLeet api documentation"
summary: ""
date: 2023-09-07T16:04:48+02:00
lastmod: 2023-09-07T16:04:48+02:00
draft: false
weight: 810
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: true # false (default) or true
---

Welcome to Job Leet, a comprehensive and scalable job portal solution powered by our Job Leet Job Portal API. This API is designed to handle all job-related operations, providing an efficient and easy-to-use platform for managing job listings, applications, users, and much more. Built on .NET 8, with support for Docker and MySQL, Job Leet ensures a modern, scalable, and containerized deployment environment.

Job Leet Job Portal API is a backend solution built using .NET and follows the REST architecture. This API provides various job portal functionalities such as job postings, user authentication, and message queuing. With built-in support for RabbitMQ, JWT Authentication, Database Migrations, and more, Job Leet is structured for easy integration into various job-seeking or recruitment platforms.

This documentation will guide you through setting up and running the API locally or in a containerized environment using Docker. We also cover key features and configuration settings to help you get started quickly.

## Getting Started
#### Prerequisites

Before you begin, ensure you have the following tools installed on your machine:

- .NET 8: The latest version of the .NET framework for building and running the API.
- MySQL: Database system required to store job-related data.
- Docker: For running the application in a containerized environment.
- Git: To clone the repository.

### 1. Clone and Build

- Clone the Repository
- Open your terminal and clone the Job Leet API repository by running:


```
git clone https://github.com/Nix-code/Job-Leet-core-api.git

```

### 2. Navigate to the Project Directory
Once cloned, move into the project directory:

```
cd Job-Leet-core-api

```
### Configuration

The Job Leet API uses a MySQL database, and you will need to configure the database connection.

- Update Configuration for Local Environment
- By default, the API uses an appsettings.Development
- json file for development settings. Update the file with your MySQL credentials:

```
{
  "ConnectionStrings": {
    "jobleetconnect": "Server=localhost;Database=<DBName>;User=<Username>;Password=<Password>;Port=3306;AllowPublicKeyRetrieval=True;SslMode=None"
  }
}

```

### Docker setup
To run the API inside a Docker container, follow these steps:

- Create a .env file in the root directory and provide your MySQL database credentials:

```
MYSQL_DATABASE=<DBName>
MYSQL_PASSWORD=<StrongPassword>
```

Make sure the appsettings.Development.json and docker-compose.yml credentials match.

Finally, build and start the Docker containers:

```

  docker-compose build && docker-compose up
```

The API will be accessible at:

`http://localhost:8080/api/v1/<endpoint>`

Or check out the Swagger UI at:

`http://localhost:8080/swagger/index.html`

