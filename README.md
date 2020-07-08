# FIN4 System

## Structure

The project contains three services:

- ganache-cli: runs local private ethereum blockchain
- FIN4Contracts
- FIN4Xplorer: React frontend 

## Setup

1. Install Docker Desktop: [https://docs.docker.com/desktop/](https://docs.docker.com/desktop/)
2. Add MetaMask to your browser: [https://metamask.io/](https://metamask.io/)
3. `git clone --recurse-submodules https://github.com/moritz-schindelmann-tum/ETH-FIN4.git`
4. `cd ETH-FIN4`

## Build the images / services

Run `docker-compose build`
Depending on your system and docker version, you could see some warnings in the console. You can ignore these warnings as long as the build finishes successfully.

## Start the system

1. Run `docker-compose up -d` to start the services in the detached mode.
2. (Optional) Run `docker ps -a` to see all services.
Run `docker logs -f fin4xplorer` to follow the progress of the frontend startup. 
3. Go to your browser and import the ganache ethereum accounts to your MetaMask with the following seed phrase: 
`season prevent fault almost then hungry lazy typical pipe exist recipe milk` 
Make sure to do this before you try to access the frontend in your browser. 
Choose localhost:8545 as the network that MetaMask connects to. If the import does not work at the first try. Switch to another network like ropsten, switch back and then import again.
5. When the frontend server has started (which you will see in the console), you can access the frontend at [http://localhost:3000/](http://localhost:3000/).
