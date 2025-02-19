# Nginx Public Files Server

This project sets up a public Nginx server exposed through a Traefik proxy.

## Prerequisites

- Docker
- Docker Compose

## Setup

1. Clone the repository:

   ```sh
   git clone https://github.com/Emilien-Foissotte/nginx-public-files-open.git
   cd nginx-public-files-open
   ```

2. Start the services using Docker Compose:
   ```sh
   docker-compose up -d
   ```

## Configuration

- **Nginx Configuration**: Modify `nginx.conf` to change the Nginx server settings (OPTIONAL).
- **Docker Compose**: Modify `docker-compose.yml` to change the Docker services configuration (OPTIONAL).

## Access

Once the services are up and running, you can access the Nginx server through the Traefik proxy at `http://<your-domain>/public/sharefolder`.

Add some files under /opt/publicfolder under your server to expose them.

_N.B:Google bots shouldn't list your files due to the `X-Robots-Tag=no-index`. If it does appear, make sure a `robots.txt` at root domain doesn't block metadata reading._

## Live demo

A live demo of this implementation can be seen at `https://emilienfoissotte.fr/public/`

## License

This project is licensed under the MIT License.
