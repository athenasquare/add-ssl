# add-ssl

To add SSL to your website with the given docker-compose.yaml and Nginx configuration, you can follow these steps. This assumes you are adding SSL for the domain.

## Step 1: Prerequisites

Before you start, ensure that you have Docker and Docker Compose installed on your server. Also, make sure that your DNS records for <domain> point to your server's IP address.

## Step 2: Configure Nginx for SSL

In your data/nginx/default.conf file, there is a configuration of SSL. Replace existing domain_name with your current domain_name in server_name as well as in in the SSL certificate paths.

## Step 3: Update your domain in init-letsencrypt file

Update init-letsencrypt.sh file with your domain instead of getdash.live


## Step 4: run init-letsencrypt.sh, this will create certificate for your domain.

## Step 5: redeploy docker-compose containers. 

It may take some time to reflect SSL changes. 
