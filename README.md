# nginx-setup
Setup NGINX Server as API Gateway on Ubuntu 

Install Nginx on Ubuntu Linux 18.04 LTS
---------------------------------------

$ sudo apt update

$ sudo apt upgrade

$ sudo apt install nginx

Commands to start/stop/restart Nginx server on Ubuntu
-----------------------------------------------------

__Enable Nginx server at boot time using the systemctl command:__

$ sudo systemctl enable nginx

__Start Nginx server using the systemctl command:__

$ sudo systemctl start nginx

__Restart Nginx server using the systemctl command:__

$ sudo systemctl restart nginx

__Stop Nginx server using the systemctl command:__

$ sudo systemctl stop nginx

__Reload Nginx server using the systemctl command:__

$ sudo systemctl reload nginx

__Get status of Nginx server using the systemctl command:__

$ sudo systemctl status nginx


Use __$ sudo systemctl status nginx__ to check status of nginx server that its status is active or not. 
By default NGINX server runs on port 80 but if you already installed apache or any other server then you need to 
configure the port of nginx server.

To Change NGINX Server Port Settings:
-------------------------------------

$ sudo nano /etc/nginx/sites-enabled/default

Now find these lines:

listen 80 default_server;

listen [::]:80 default_server;

__Here change 80 with another port number for example I am changing it to 8088 port number__

listen 8088 default_server;

listen [::]:8088 default_server;

__Now save the file and restart the nginx server:__

$ sudo systemctl restart nginx

__Now check status of nginx server, it will be active now__

$ sudo systemctl status nginx

__Now go to your browser and hit base url of your server__ 

for example if you are working on local

http://localhost:8088

Or if you are on live server having a live domain or IP address, then use that

http or https://yourdomain.com:8088

You will see the NGINX Server Welcome page with heading __"Welcome to nginx !"__

__Now your NGINX Server is installed successfully !!!__


Setting Up NGINX as API Gateway
--------------------------------


