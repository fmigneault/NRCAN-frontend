# NRCAN-frontend

## Features

## Requirements 

**(TODO: add/remove real dependencies...)**
* node `^4.2.0` but developped with Node v5.11.1
* npm `^3.0.0` but developped with Node v3.8.6

## Getting Started 

**(TODO: validate + other steps?)**
After confirming that your development environment meets the specified [requirements](#requirements), you can follow these steps to get the project up and running:

**(TODO: change links as required + add steps to fix encountered errors)**
```bash
$ git clone https://github.com/fmigneault/NRCAN-frontend.git
$ cd NRCAN-frontend
$ npm install                   # Install project dependencies
$ npm start                     # Compile and launch
```

If everything works, you should see the following:

<img src="http://i.imgur.com/zR7VRG6.png?2" />

## Docker
**(TODO: fix links / commands - now invalid)**
Install Docker, I followed CentOS guide: https://docs.docker.com/engine/installation/linux/centos/

Build & Run on Linux
```bash
$ git clone https://github.com/Ouranosinc/PAVICS-frontend.git
$ cd PAVICS-frontend
$ docker build -t pavics/geoweb .
#To Run
$ docker run -p 3000:3000 -it pavics/geoweb #Then browse application at localhost:3000
#OR
$ docker run -p 3000:3000 -e PAVICS_FRONTEND_IP=<host_ip> -t pavics/geoweb #Then browse application at host_ip:3000
```

Build & Run on Windows:
```bash
$ git clone https://github.com/Ouranosinc/PAVICS-frontend.git
$ cd PAVICS-frontend
$ docker-machine ip default #If on Windows uses VM IP (note that ip for next step)
$ vi config/index.js
# Change line 37 with previous vm ip
# server_host : '<docker-machine ip>', // use string 'localhost' to prevent exposure on local network
# Save & Quit
$ docker build -t "pavics/geoweb" .
$ docker run -p 3000:3000 -it "pavics/geoweb" #Browse application at address <docker-machine ip>:3000
```

Pull from CRIM private registry (some config is needed for http insecure-registries):
```bash
$ docker pull crim-registry1:5000/pavics/geoweb
$ docker run -p 3000:3000 -it crim-registry1:5000/pavics/geoweb #Browse application at localhost:3000
```
