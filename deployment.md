Step 1: Login to AWS Account 
Step 2: Create VPC
Step 3: Create EC2 machine public subnet
note: Do not assign public IP and allow SSH 22 port and Nginx 80 port(HTTP)
Step 4: Create Elastic IP and assign it to Ec2 machine
step 5:Do the reqired installations:
 apt-get update -y
  apt-get install nginx -y
step 6: clone the repo to ec2 using ssh
step 7: copy the files /var/www/devopsdeepdive 
step 8: Create nginx config file in /etc/nginx/sites-available/devopsdeepdive
step 9 : Create Public DNS hosted zone in the cloud
Step 10 :Create subdomain with A record and add the Elastic Ip public address 
Step 11: Enable the website 
sudo ln -s /etc/nginx/sites-available/devopsdeepdive \
/etc/nginx/sites-enabled/devopsdeepdive
Step 12: Restart the Ngixn
Finally test the Domain from Browser
