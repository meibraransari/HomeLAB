# About my Homelab Setup

<img src="Home-Lab.png" alt="Home-Lab.png" width="800"/>

# Hardware Details

🔄🏡 Small Homelab for 2023! 💻🔧
Hey folks! 👋 I am excited to give you a sneak peek into my Homelab setup! 🤓 
🚀 As a DevOps engeener we neeed a lab where we can deploy & test our microservices/application. Here is my homelab. Nothing special but mine.

```
Server:
        -> Dell Precision T5810:
                Xeon E-2673 v3 12Core/24Thread CPU
                64GB DDR3-1600 Ram
                500 SSD Boot Drive
                STORAGE 2 TB HDD
                Nvidia Quadro K-2200 4GB Graphics 
                Operating Systems: Proxmox 
Personal System
        -> Desktop PC has below config:
                AMD Ryzen 7 5800X 3.8 GHz
                ASUS B550 Prime B550M-A WiFi II
                Corsair 8x4 32GB DDR4 Ram
                1TB SSD
                1 TB HDD
                Operating Systems: Windows 10
                Monitor: Dell 
                Keyboard: TVS Gold
                Mouse: Logitech M235
                Alexa Echo Dot (3rd Gen)
Laptop:
        -> Dell Latitide 5490 (i7 CPU, 16GB Memory, 500GB SSD)

Routers: 
        -> TPLink is for Fiber Connectivity & Netgear for LAN
```

# Services I use in my Lab:

Services that I bring up using Docker Compose

```
-> Proxmox
        Proxmox Virtual Environment is a hyper-converged infrastructure open-source software. It is a hosted hypervisor that can run operating systems including Linux and Windows on x64 hardware.
        https://www.proxmox.com/en/
-> OPNsense
        OPNsense is an open source, FreeBSD-based firewall and routing software developed by Deciso, a company in the Netherlands that makes hardware and sells support packages for OPNsense. It is a fork of pfSense, which in turn was forked from m0n0wall built on FreeBSD.
-> Linux OS        
        Ubuntu, CentOS, Debian, Alpine
-> Nginx & Nginx proxy manager
        We are using it to access our microservices
        https://docs.nginx.com/nginx/admin-guide/web-server/reverse-proxy/
        https://nginxproxymanager.com/
-> Kubernetes
        Kubernetes is an open-source container orchestration system for automating software deployment, scaling, and management. Originally designed by Google, the project is now maintained by the Cloud Native Computing Foundation. 
        https://kubernetes.io/
        kubectl cluster-info
        kubectl get nodes -o wide | awk -v OFS='\t' '{print $1, $6}'
-> Rancher
        Rancher, the open-source multi-cluster orchestration platform, lets operations teams deploy, manage and secure enterprise Kubernetes. 
        https://www.rancher.com/ 
-> TrueNAS
        TrueNAS is the branding for a range of free and open-source network-attached storage operating systems produced by iXsystems, and based on FreeBSD and Linux, using the OpenZFS file system.
-> MINIO SERVER
        MinIO® is an object storage server, compatible with Amazon S3 cloud storage service, mainly used for storing unstructured data (such as photos, videos, log files, etc.).
        https://min.io
        https://hub.docker.com/r/bitnami/minio/
-> Docker
        Docker is a set of platform as a service products that use OS-level virtualization to deliver software in packages called containers. The service has both free and premium tiers. The software that hosts the containers is called Docker Engine.
        https://www.docker.com/
-> Database Host
        Database(MySQL, Postgres, MongoDB) hosted for some personal tasks and testing purpose
-> Portainer
        Portainer is your container management software to deploy, troubleshoot, and secure applications across cloud, datacenter, and Industrial IoT use cases.
-> Zabbix
        Zabbix is an open-source software tool to monitor IT infrastructure such as networks, servers, virtual machines, and cloud services. Zabbix collects and displays basic metrics.
        https://www.zabbix.com/
-> Uptime Kuma
        Uptime Kuma. Uptime Kuma is an easy-to-use self-hosted monitoring tool. 
        https://uptime.kuma.pet/
        https://demo.uptime.kuma.pet:27000/
-> Traefik
        Reverse proxy/load balancer with Lets Encrypt for TLS Certs
        Traefik is the leading open-source reverse proxy and load balancer for HTTP and TCP-based applications that is easy, dynamic and full-featured
        https://traefik.io/traefik/
-> excalidraw
        Excalidraw is a virtual collaborative whiteboard tool that lets you easily sketch diagrams that have a hand-drawn feel to them
        https://excalidraw.com/
-> pihole
        Pi-hole is a Linux network-level advertisement and Internet tracker blocking application which acts as a DNS sinkhole and optionally a DHCP server, intended for use on a private network.
        https://pi-hole.net/
-> Gitlab
        GitLab Community Edition docker image based on the Omnibus package.
        https://docs.gitlab.com/ee/install/docker.html
```
