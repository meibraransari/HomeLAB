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

| Service Name | Description |
|--------------|-------------|
| traefik | Reverse proxy/load balancer with Let's Encrypt for TLS Certs|
| tailscale | VPN for remote access to my homelab |
| portainer | Docker/Kubernetes Management Platform/UI |
| pihole | DNS server and ad-blocker |
| passbolt | Self Hosted Password/Secrets Manager |
| db | MariaDB for Passbolt password manager |
| jenkins | Continuous integration and delivery (CI/CD) server |
| prometheus | Monitoring and alerting system (How I scrape metrics) |
| grafana | Data visualization and analytics platform (Dashboards) |
| cloudflare-tunnel | Cloudflare tunnel for secure access to some applications |



# Bring up all services

1. Create a `.env` file based on the `.env_template` file.

```
cp env_template .env
```

2. Modify the values of each environment variable to whats suitable for your environment.

```
vi .env
```

3. Bring up all services with docker-compose up

```
docker-compose up -d
```

Got errors? Troubleshoot based on the error messages! This is a complex setup, likely it is better for you to start from scratch, and copy/paste components of my setup into your own setup.  I suggest bringing up one service at a time, then adding on things like Traefik.
