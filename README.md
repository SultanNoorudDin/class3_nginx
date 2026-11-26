# Static Portfolio Website Deployment on AWS EC2 with Nginx & HTTPS (TLS)

A responsive one-page portfolio website built with HTML, CSS, and JavaScript, deployed on an AWS EC2 Ubuntu instance using Nginx, and secured with a free TLS/SSL certificate via Let's Encrypt and Certbot.

## Architecture & Traffic Flow

```text
Visitor Browser (HTTPS / Port 443)
        │
        ▼
AWS EC2 Security Group (Ports 22, 80, 443)
        │
        ▼
Nginx Reverse Proxy & Web Server (HTTP 301 Redirect → HTTPS)
        │
        ▼
Static Web Root (/var/www/mysite)
