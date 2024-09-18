# PHP Application with CI/CD, Docker, AWS Deployment, and Database Integration

This project demonstrates a simple PHP web application with MySQL database integration, modern development practices, and a complete CI/CD pipeline using Docker and GitHub Actions. The application includes automated testing, code quality checks, Slack notifications, and deployment to AWS Elastic Beanstalk for both staging and production environments. Database migrations are automated to handle schema changes across environments.

## Features

1. **Basic PHP Website with MySQL Integration**
   - A PHP webpage that displays user data from a MySQL database.
   - Data is fetched dynamically from the `users` table.

2. **Dockerized Development Environment**
   - PHP application and MySQL database run in separate Docker containers.
   - Consistent and isolated local development environment using Docker Compose.

3. **Database Migration Support**
   - Schema migrations can be added to the `migrations/` folder.
   - Automatically applied migrations in staging and production during deployment.

4. **Unit Testing with PHPUnit**
   - Unit tests are provided for database connection and core functionalities.
   - Tests are executed within a Docker container.

5. **GitHub Actions CI/CD Pipeline**
   - Automatic testing, code quality checks, and deployment upon pushing changes to the repository.
   - Staging deployment is automated, while production deployment requires manual approval.

6. **Code Quality Checks with PHP CodeSniffer**
   - Code is checked against PSR-12 coding standards using PHP CodeSniffer.
   - Integrated into the CI pipeline via GitHub Actions.

7. **Slack Notifications**
   - Real-time build, test, and deployment status updates sent to Slack via webhooks.

8. **AWS Elastic Beanstalk Deployment**
   - **Staging Deployment**: Automatically triggered on successful build and testing.
   - **Production Deployment**: Requires manual approval after staging environment validation.

## Project Structure

```bash
project-root/
├── public/
│   └── index.php        # Main PHP file that shows data from the database
├── src/
│   └── Calculator.php   # Example PHP class for unit testing
├── migrations/          # Database migration files
│   └── migration_001_create_users_table.php
├── db.php               # Database connection file using PDO
├── composer.json        # Composer dependencies and autoload configuration
├── Dockerfile           # Dockerfile to set up PHP and Apache
├── docker-compose.yml   # Docker Compose configuration to run app and MySQL
├── tests/
│   └── DatabaseTest.php # PHPUnit tests for the database
└── .github/
    └── workflows/
        └── php.yml     # GitHub Actions CI/CD pipeline configuration
```

# Getting Started

## Prerequisites

- Docker & Docker Compose installed
- Composer installed for managing PHP dependencies
- AWS Elastic Beanstalk CLI installed for deployment
- A Slack webhook URL for notifications (optional)

## Local Development

Clone the repository:

```bash
git clone https://github.com/your-username/php-cicd-project.git
cd php-cicd-project
```

