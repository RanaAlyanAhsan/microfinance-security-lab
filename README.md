
# Microfinance Security Lab

## Project Overview
This project is a simulated web application security assessment for Ezitech. DVWA is used as an intentionally vulnerable application for learning and security testing.

## Lab Environment
- Ubuntu 22.04 LTS (VirtualBox)
- Docker Engine 29.10.1
- Docker Compose 5.8.0
- Damn Vulnerable Web Application (DVWA)
- MariaDB Database

## Repository Files
- scope.md: Assessment scope and authorization.
- compose.yaml: Docker container configuration.
- verification.txt: Lab verification results.
- README.md: Project documentation and setup instructions.

## How to Start the Lab

1. Install Docker and Docker Compose.
2. Download or clone this repository.
3. Open the repository directory in the terminal.
4. Validate the configuration:

   sudo docker compose config -q

5. Start the containers:

   sudo docker compose up -d

6. Check container status:

   sudo docker compose ps

7. Open the following URL inside Ubuntu:

   http://127.0.0.1:4280

8. Open setup.php and click Create / Reset Database.
9. Log in using the default DVWA lab credentials.

## Verification Results
- DVWA container is running.
- MariaDB container is running.
- HTTP response returned 302 Found.
- Application redirects to the login page.
- Application is bound to 127.0.0.1:4280.
- UFW firewall remains active.
- Existing SSH hardening settings remain enabled.
- Database initialization completed successfully.

## Security and Authorization
All testing is performed locally inside the authorized lab environment. No real microfinance systems, external websites or real borrower data are involved.

The vulnerable application is restricted to localhost and must not be exposed publicly.

## Stop the Lab

Run the following command:

    sudo docker compose down

## Task 1 Outcome
The assessment scope has been defined and the local Docker-based vulnerable web application has been successfully configured and verified.
