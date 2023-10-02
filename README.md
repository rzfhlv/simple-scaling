# Simple Scaling APP

Simple horizontal scaling nodejs app with nginx as load balancer

## Requirements
- nodejs v16^
- nignx v1.23^
- pm2

## Installation
1. Clone this repo.
2. Go to apps directory in root.
3. Run using pm2 with spesific port one by one (3000, 3001, 3002, 3003) ex: ```PORT=3000 pm2 start app.js --name "app-1"``` (make sure each port using different name).
4. Copy config/simple-scaling.conf to sites-available directory on your nginx config.
5. Create symlink for simple-scaling.conf with command: ```ln -s <path-to-nginx-config>/nginx/sites-available/simple-scaling.conf <path-to-nginx-config>/nginx/sites-enabled/```
6. Reload nginx and this app ready to test, it can accessible from browser with url ```http://localhost:8000```
7. The response can give repsonses like port app and pid.