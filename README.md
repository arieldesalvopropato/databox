<img src="https://github.com/arieldesalvopropato/databox/blob/main/Databox-logos_black.png" width="200" height="200">

Scripts to implement a home server using Docker.

## Introduction

The goal of this project is to make more easy the deployment and installation of a home server, without the need to perform the installation of the services to use and provide a more practical solution when it comes to having our own server.

## Operating Systems

The requirements of this script for use are not determined on a single particular operating system. It was developed using Ubuntu Server, so you could use operating systems like Ubuntu or Debian out of the box. In case you choose another distribution like Arch or Fedora you will have to make modifications and I cannot guarantee it will work.

## Containers

* [Ngnix](https://www.nginx.com/)
* [Dashy](https://dashy.to/)
* [Portainer](https://www.portainer.io/)
* [Pi-Hole](https://pi-hole.net/)
* [Uptime-Kuma](https://github.com/louislam/uptime-kuma)
* [Watchtower](https://containrrr.dev/watchtower/)
* [NextCloud](https://nextcloud.com/es/)
* [MySQL](https://www.mysql.com/)
* [FileBrowser](https://filebrowser.org/)
* [Jellyfin](https://jellyfin.org/)
* [Sonarr](https://sonarr.tv/)
* [Jackett](https://github.com/Jackett/Jackett)
* [Transmission](https://transmissionbt.com/)
* [Duplicati](https://www.duplicati.com/)
* [Syncthing](https://syncthing.net/)
* [Resilio-Sync](https://www.resilio.com/individuals/)
* [Kasm](https://www.kasmweb.com/)
* [Wireguard](https://www.wireguard.com/)
* EKF ([Elasticsearch](https://www.elastic.co/) - [Kibana](https://www.elastic.co/kibana/) - [Filebeat](https://www.elastic.co/beats/filebeat))
* No-IP
* Samba

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
* cd databox
* Change the "setupvariables.yml" file in the config folder with your own preferences.
* ansible-playbook playbook.yaml -i inventory/hosts.ini

## Authors

* **Ariel De Salvo Propato** - [GitHub](https://github.com/arieldesalvopropato)

## License

This project is licensed under the GNU GPL v3.0 - see the [LICENSE](LICENSE) file for details