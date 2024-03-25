# ArmagetronAd Server Setup using Docker Compose
Setup multiple armagetron servers easily using the [armagetronad docker image](https://hub.docker.com/r/codefossa/armagetronad) and docker compose

## Basic Setup
- It is recommended to use your preferred distribution of linux
- Follow the instructions for [installing docker](https://docs.docker.com/engine/install/)
- Clone this repo
- Refer to docker-compose.yml.sample for a sample server configuration
- Copy this configuration and adjust the names / mounted folder locations / ports accordingly

## Server Configuration
- Server configuration files live locally on your server
- To create a new server configuration, copy one of the existing server folders and rename it / adjust the settings accordingly
    - Optionally, delete any existing var data
- Adjust server/<server_name>/settings/server_info.cfg and settings_custom.cfg with your server settings
- For scripting, put scripts in the scripts/ folder and SPAWN_SCRIPT in script.cfg

## Running the Servers
- Start all services with docker compose up (add -d to only log to /var/consolelog.txt)
- Restart / manage individual containers as needed with docker compose commands