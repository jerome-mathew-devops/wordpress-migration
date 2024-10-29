# ﻿Migrating WP Website to AWS Cloud Services
Procedure (Theoritically):

Access: Cloud readiness of the company

Mobilize: Build foundation capability of company on AWS

Migrate: Migrate system and database to the cloud

## Steps
Install WordPress

Transfer domian

Migrate Database

## Installing WordPress
### Steps:
* Create an EC2 install
  
* Choose an Amazon Machine Image in AWS Marketplace
  
* Select, Configure (Add Storage,  Add Tags, Security group), Launch Instance
  
### Configure Domain
* From the Launch Status screen, click on the link to your instance.
  
* From your Instances dashboard, copy your instance's Public IPv4 address.
  
* From your web browser, navigate to your domain name provider (we recommend Namecheap. Navigate to the settings page for your domain, and select Namecheap BasicDNS from the NAMESERVERS row.
  
* Next, click on the Advanced DNS tab at the top-right of your domain name dashboard. Then, under the HOST RECORDS row, create a new A record as shown in the image, however, remember to replace the IP address in the image with the IPv4 address of your instance (which you copied in a previous step). Next, create a CNAME record record as shown in the image.
  
* Return to your Instances dashboard and click on your Instance ID
  
* Click the Connect button at the top of your Instance summary page.
  
* From the Connect to instance screen, click on the SSH client tab, then copy the  command.
  
* Open your terminal and navigate to your Downloads directory (or whichever default directory you use for storing downloads)
  
* Now that you've navigated to your Downloads directory, execute the chmod command to change the permissions of your key pair file
  
* Or you can connect too your instance using AWS  connect
  
* Once you've connected to the instance, run the command "sudo /opt/bitnami/bncert-tool"
  
* You will be prompted to answer the a set of questions and it is advised to answer all questions correctly
