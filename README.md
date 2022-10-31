<img src="https://github.com/arieldesalvopropato/databox/blob/main/Databox-logos_black.png" width="200" height="200">

Scripts to implement a home server using Docker.

## Introduction

The goal of this project is to make more easy the deployment and installation of a home server, without the need to perform the installation of the services to use and provide a more practical solution when it comes to having our own server.

## Operating Systems

The requirements of this script for use are not determined on a single particular operating system. It was developed using Ubuntu Server, so you could use operating systems like Ubuntu or Debian out of the box. In case you choose another distribution like Arch or Fedora you will have to make modifications and I cannot guarantee it will work.

## Containers

* Duplicati
* Dashy
* Jellyfin
* MySQL
* NextCloud
* Ngnix
* Pi-Hole
* Portainer
* Transmission
* Sonarr
* Jackett
* Uptime-Kuma
* Watchtower
* Kasm
* Wireguard
* Samba
* FileBrowser
* Elasticsearch
* Kibana
* Filebeat

### Optional
* No-IP

## Usage
Install a base operating system. For the development of the Scripts and Playbooks I used [Ubuntu Server](https://ubuntu.com/download/server). In case of using an operating system with a package manager different to apt, define it in the playbook yaml file.

If you choose to use some NAS system like for example OpenMediaVault as your base system, please consider the following modifications to your server:
* Change the default port of the http service 80 to 88, this port will be used by the Nginx service.
* Install [OMV-Extras](https://wiki.omv-extras.org/) to have more functionality on your server, including Docker.
* Install Docker from OMV-Extras options in OpenMediaVault webgui.

To deploy the server perform the following steps:
* Install git
* Install ansible
* git clone https://github.com/arieldesalvopropato/databox.git
* cd databox-main
* Change the "setupvariables.yml" file in the config folder with your own preferences.
* sudo ansible-playbook playbook.yaml

## Authors

* **Ariel De Salvo Propato** - [GitHub](https://github.com/arieldesalvopropato)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
