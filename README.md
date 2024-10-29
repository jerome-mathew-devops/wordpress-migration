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

  ## Login to WordPress
* While still connected to the instance, run "sudo cat /home/bitnami/bitnami_credentials" to get the credentials for the wordpress
  
* Visit WordPress login page and use the username and password from the step above
  
## Assign a Static IP
	By Default, Our Wordpress instance is assigned an ephemeral IP, meaing the WP IP address is change when ever the Instance stops or restarts.
Import the WordPress Website

	We use the All-in-one WP Migration Unlimited Plugin to quickly and easily import nd export the existing WordPress Website to it's new location on AWS.
 
* Downlaod the WP Migration Plugin: From our  WordPress website, head over to "Add Plugins" and download the All-in-One WP Migration plugin
  
* Activate the All-in-One WP Migration plugin, and access it by clicking the link in your WordPress sidebar column. From the All-in-One WP Migration dashboard, enter your existing website URL in the Find field, and your new website URL in the Replace with field. Finally, export your website by selecting Export To > File.
  
* Import Website File: From your new WordPress Website installation, download the All-in-One WP Migration plugin and go to Import From > File. Choose the export file that you downloaded in the previous step.
  
* Change Permalink Structure: After you've successfully imported your WordPress website,will need to reset your permalink structure. From your WordPress dashboard go to Settings > Permalinks, and select the permalink structure that you prefer (I recommend Post name).
