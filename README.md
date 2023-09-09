# PHP SSL  
This folder is for running php with ssl on your local machine  

## Install  
1. Clone this repository `git clone https://github.com/benjaminchocron/php-ssl.git php`  
  
2. Copy **.env.example** to **.env** `cp .env.example .env`  
  
3. Modify **.env** with your values `vi .env`

4. In `server/conf` folder create folder `certs` with your ssl certificates  
***Note: You can use mkcert, openssl or any other way to create your certificates***  

## Run the application  
1. In the root folder  
run `docker-compose build --no-cache`  
then `docker-compose up -d`

2. Open your browser to your localhost `https://localhost`

3. Create your php app in the `app` folder.

4. That's all