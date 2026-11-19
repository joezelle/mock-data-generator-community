# Database Containers

The extension can start a database in Docker for you to fill with mock data, so you don't need a database server installed. It needs Docker Desktop (or the Docker Engine) installed and running.

## Commands

| Command | What it does |
| --- | --- |
| Check Docker Availability | Tells you whether Docker is running, and its version |
| Create Database Container | Creates a MongoDB, MySQL, PostgreSQL or SQL Server container and waits until it accepts connections |
| Manage Database Containers | Start, stop, view the logs of, or remove a container the extension created |
| Generate Docker Compose File | Writes a Compose file for the databases you pick (Docker doesn't need to be running) |

The **Database Containers** section of the Mock Data Generator view lists the containers; click one to start, stop, view logs or remove it.

## Using a container when you populate a database

When you generate data with **Database** as the output and choose **Individual Parameters**, the extension offers to create a container (if Docker is running). You choose a port and a password, and the extension:

1. downloads the image the first time (this can take a few minutes),
2. creates and starts the container, or starts the existing one,
3. waits until the database accepts connections,
4. creates the database (`mock_data`) if the container doesn't have it,
5. fills in the host, port, database, username and password for you.

A container that already exists is reused as it is: it keeps the port and password it was created with, and the extension reads them from the container. Remove it with **Manage Database Containers** to start over with new settings.

## Images and defaults

| Database | Image | Port | Username | Default password |
| --- | --- | --- | --- | --- |
| MongoDB | `mongo:7` | 27017 | `root` (or yours) | `example` |
| MySQL | `mysql:8.4` | 3306 | `root` | `example` |
| PostgreSQL | `postgres:16` | 5432 | `postgres` (or yours) | `example` |
| SQL Server | `mcr.microsoft.com/mssql/server:2022-latest` | 1433 | `sa` | `MockData_Passw0rd!` |

SQL Server refuses weak passwords: it needs at least 8 characters with 3 of uppercase, lowercase, digits and symbols. The extension checks this before creating the container.

Containers are named `mock-data-<database>` by default and carry the label `mock-data-generator`, so the extension finds them whatever you name them.

## Troubleshooting

- **"Port … is already in use"**: another database or container is using that port. Pick another port, or stop it.
- **"stopped while starting"**: the message includes the container's last log lines. For SQL Server this is usually the password policy or too little memory (it needs 2 GB).
- **"did not accept connections within … seconds"**: view the container's logs with **Manage Database Containers**.
- **The image could not be downloaded**: check your internet connection and Docker's proxy settings.

## Security

These containers are for development and testing. Passwords are passed to Docker directly, not through a shell, and aren't written to the extension's log. The default passwords are public; use your own for anything shared.
