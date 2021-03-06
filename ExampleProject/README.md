# Simple NodeJS HTTP Server version 0.1.0
A simple NodeJS Express application for standing up an HTTP server.  The goal of this project is to easily run a local server for developing static content, while allowing for integration with NPM libraries for security and convenience.

## Hardware requirements
### Computational Resource Requirements
CPU Cores: 1

CPU Clock Speed: 1.3 GHz

RAM requirements: 2 GiB
### Minimal Physical Storage
Drive Space: 2GB (Plus storage for hosted files)

*HHD or SSD agnostic*

### Additional Hardware required
Network Interface Card

## Operating System Requirements
### Drivers and other software
Required Kernel and Drivers: 
- Ubuntu Kernel  4.15.0-45-generic #48~16.04.1-Ubuntu SMP
- xt_nat v4.15.0-43-generic
- zstd_compress 4.15.0-43-generic
- xor 4.15.0-43-generic
- raid6_pq 4.15.0-43-generic
- nfnetlink 4.15.0-43-generic
- xfrm_user 4.15.0-43-generic
- iptable_nat 4.15.0-43-generic
- nf_conntrack_ipv4 4.15.0-43-generic
- xt_addrtype 4.15.0-43-generic
- iptable_filter 4.15.0-43-generic
- xt_conntrack 4.15.0-43-generic
- aufs 4.15.0-43-generic
- snd_intel8x0 4.15.0-43-generic

Required Libraries:
- libapt-pkg5.0 v1.2.29ubuntu0.1
- libc6 v2.23-0ubuntu11
- libgcc1 v6.0.1-0ubuntu1
- libstdc++6 v5.4.0-6ubuntu1~16.04.11
- init-system-helpers v1.29ubuntu4
- ubuntu-keyring v2012.05.19
- gpgv v1.4.20-1ubuntu3.3
- gnupg v1.4.20-1ubuntu3.3
- gnupg2 v2.1.11-6ubuntu2.1
- adduser v3.113+nmu3ubuntu4

### System Setup
Required Operating System: Ubuntu 16.04.6 LTS

Required user permissions: One user with root access

Required credentials: N\A
### Additional Requirements
Third party libraries
- [axios](https://www.npmjs.com/package/axios) v0.18.0
- [cors](https://www.npmjs.com/package/cors) v2.8.5
- [ejs](https://www.npmjs.com/padduserackage/ejs) v2.6.1
- [express](https://www.npmjs.com/package/express) v4.16.4

Third Party applications:
- Git v2.7.4
- Curl v7.47.0-1ubuntu2.12
- Node.js v4.2.6~dfsg-1ubuntu4.2
- Node Package Manager (NPM) v3.5.2
- Docker v1.5.1 OR Docker-Compose v1.8.0-2~16.04.1r

URL and download instructions for above libraries and applications:

All libraries and third party software can be installed by running the install-reqs shell file

- `sudo apt update`
- `sudo apt upgrade`
- `sudo bash ./install-reqs.sh`

If running locally, you will need to **[install NodeJS](https://nodejs.org/en/download/)**.

Licensing information for above libraries and applications
- Node.js: Licenses/NodeJsLicense
- Docker: Licenses/Apache2License
- Docker-Compose: Licenses/Apache2License
- axios: Licenses/MITLicense
- cors: Licenses/MITLicense
- ejs: Licenses/Apache2License
- express: Licenses/MITLicense

## Application Documentation
### Deployment Description
#### Default network topology
Default IP addresses: 127.0.0.1

Default Port usage: Port 80

Additional Software or Hardware requirements: None
### Deployment Instructions
Each of the below will begin with opening your favorite shell.  **The instructions for Docker have not been tested on Windows.**
#### Node
If you are looking to start this on Windows, then this is the preferred method. **These instructions will not work on ubuntu 16.04**
- `git clone https://github.com/vbhayden/simple-node-http`
- `cd simple-node-http`
- `node app.js`
#### Docker
If you enjoy typing out long Docker commands, then this is the method for you.
- `git clone https://github.com/vbhayden/simple-node-http`
- `cd simple-node-http`
- `sudo ./install-reqs.sh`
- `sudo docker build -t simple-http-image .`
- `sudo docker run -d -it -p 80:80 -e PORT=80 --name=simple-http simple-http-image`

#### Docker-Compose
If you enjoy Docker but are also civilized, this is the preferred method for you.
- `git clone https://github.com/vbhayden/simple-node-http`
- `cd simple-node-http`
- `sudo ./install-reqs.sh`
- `sudo docker-compose up -d --build`

### Installation Testing Instructions
When the server starts, the console will print the following:
```
[Server] listening on port 3000 ...
```
If you used one of the Docker configurations, then you can access the server's console output with:
```
sudo docker logs -f simple-http
```

To view the service, browse to `localhost:3000` (or `localhost` for Docker) for the default landing page:
![alt text](https://i.imgur.com/2P3mAl9.png "Default landing page")

Navigating to something not found in your `/files` folder will produce the following:
![alt text](https://i.imgur.com/GvPEwDa.png "404")

### Troubleshooting Tips
This project isn't intended to be a robust HTTP server out of the box, opting instead to be either a simple static hosting service or an extensible baseline for a more elegant HTTP solution.  With that said, there are still a few potential issues.

#### Non-Relative `href` and `src` attributes
When a resource is requested on a page, it will be processed as one of 3 types.  Suppose we have a folder with a page accessed at `/mypage/`:
- **absolute**: specifies the protocol and full path (`https://www.google.com/images/...`)
- **domain-relative**: a path from the hosting service itself (`/my-page/public/css/...`)
- **page-relative**: a path on the server relative to that page itself (`public/css`)

If you notice that some of your static files aren't being found, check that your path declaration is navigable.  Depending on your situation, you may need to change them.

#### HTTPS / SSL
By default, this project doesn't include an HTTPS configuration.  This can be achieved either through the `https` NPM module or perhaps more easily through an Nginx proxy (straightforward with the Docker configuration).

More information on using SSL with Node **[can be found here](https://www.sitepoint.com/how-to-use-ssltls-with-node-js/)**.

## Licensing Information
The Licensing information must include transfer to the ADL (Dr Schatz) and a copy of or location of all licenses for all software used in vendor’s software delivery.
Software developed under this contract must have a statement of release of data rights as defined in the contract.
Any software developed under a Gnu Public License (GPL) that has been modified must be disclosed as defined in the license agreement by the vendor.

