## Ready Docker Warden environment for a Symfony with Postgres
<p align="center">
    <img alt="PHP 8" src="https://img.shields.io/badge/PHP-8.x-8892BF?style=for-the-badge&logo=php">
    <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-16.x-336791?style=for-the-badge&logo=postgresql&logoColor=white">
    <img alt="Redis" src="https://img.shields.io/badge/Redis-6.x-a51f17?style=for-the-badge&logo=redis&logoColor=white">
</p>

### Installation
- Docker Desktop 4.26.1+: https://docs.docker.com/docker-for-windows/install/
- Docker Compose 2.23.3+: https://docs.docker.com/compose/install/
- Ubuntu 22.04: https://docs.microsoft.com/en-us/windows/wsl/install-win10
- Install Warden: https://docs.warden.dev/
- Run `git clone https://github.com/perkhailo/symfony-warden` to clone the environment files to a separate folder and `cd` to the `app` folder.
- Check and update the `.env` file if needed. Additionally, can specify version of the services if need, e.g. `PHP_VERSION` or other.
- Run `warden env up` to get the environment up and run.
- Run `warden sign-certificate TRAEFIK_DOMAIN` use `TRAEFIK_DOMAIN` from `.env` file.
- Import the certificate file  `~/.warden/ssl/rootca/certs/ca.cert.pem` to trusted SSL's in the browser. 
- Add domain to `hosts`, i.e: `127.0.0.1 TRAEFIK_DOMAIN` use `TRAEFIK_DOMAIN` from `.env` file.
