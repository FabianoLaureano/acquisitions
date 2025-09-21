# Acquisitions API

This is the README for the Acquisitions API.

## Dockerized Setup

This project is fully dockerized for both development and production environments.

### Development

The development environment uses Docker Compose to run the application and a local Neon database instance.

**Prerequisites:**

- Docker
- Docker Compose

**Instructions:**

1.  **Create a `.env.development` file:**

    ```bash
    cp .env.development.example .env.development
    ```

2.  **Start the development environment:**

    ```bash
    docker-compose -f docker-compose.dev.yml up
    ```

    This will start the application and a local Neon database. The application will be available at `http://localhost:3000`.

### Production

The production environment uses Docker Compose to run the application. The database is expected to be a remote Neon database.

**Prerequisites:**

- Docker
- Docker Compose

**Instructions:**

1.  **Create a `.env.production` file:**

    ```bash
    cp .env.production.example .env.production
    ```

2.  **Update the `.env.production` file:**

    Replace the placeholder `DATABASE_URL` with your actual Neon database connection string.

3.  **Start the production environment:**

    ```bash
    docker-compose -f docker-compose.prod.yml up
    ```

    This will start the application. The application will be available at `http://localhost:3000`.
