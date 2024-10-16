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

## Job Leet - Your Smart Recruitment Partner


Welcome to Job Leet, a cutting-edge recruitment agency solution designed to simplify the hiring process and connect top talent with recruiters. As a comprehensive recruitment platform, Job Leet not only helps job seekers find the perfect career opportunities but also provides recruiters with the tools they need to identify and attract the best candidates.

At the core of Job Leet is a smart CRM tailored for recruitment agencies. This intelligent system streamlines the hiring process, enabling recruiters to manage candidate relationships more efficiently and make data-driven decisions. Whether you're a job seeker looking for your next opportunity or a recruiter aiming to discover top talent, Job Leet is your go-to solution.


![JobLeet Agency](../../../assets/images/jobleet.jpg)

**How Job Leet Works**

- **For Job Seekers**: Search for job openings, submit applications, and track your progress. Our platform matches your skills with the right opportunities, providing personalized job recommendations.
- **For Recruiters**: Job Leet empowers recruitment agencies and employers to streamline the hiring process. Our smart CRM helps agents and recruiters manage candidate pools, engage with top talent, and facilitate smooth communication. The platform also includes advanced filtering and search tools to find the right candidates quickly.

**Why Choose Job Leet?**

- **Efficient Talent Acquisition**: Automate and optimize your recruitment process with our smart CRM, reducing the time spent on manual tasks.
- **Personalized Job Matching**: Advanced algorithms match job seekers with relevant roles based on their skills, preferences, and career goals.
- **Enhanced Candidate Experience**: User-friendly interfaces and real-time updates keep job seekers informed and engaged throughout the hiring process.
- **Recruiter Tools and Analytics**: Gain insights into hiring trends, candidate engagement, and recruitment metrics to make better hiring decisions.

Job Leet is your all-in-one recruitment platform that brings candidates and recruiters together, fostering meaningful connections and driving career success. Join Job Leet today and experience a smarter way to hire and get hired!


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

