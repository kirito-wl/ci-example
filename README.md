# ci-example

Walkthrough using Google Cloud Marketplace to build a CI environment

Requisites
Google Cloud Account

We will be using Jenkins

Jenkins is an open source automation server that helps you automate the building, testing, and deployment of any project across multiple platforms. Jenkins helps to avoid breaking changes so that you can save time and ensure the delivery of high-quality software. Its web interface provides an easy way to manage and test your applications before taking them to production.

For this you will need to have the following APIs enabled

Compute Engine API
Cloud Deployment Manager V2 API
Cloud Runtime Configuration API



Navigate to Google Cloud Marketplace using the Navigation menu
Find Jenkins packed by Bitnami, read through the documentaiton and pricing and click launch

Verify the vm configuration is accurate and meets your needs. For this example, we have firewall rules allowing HTTP(S) traffic
Click Deploy

If you receivet he following error
{"ResourceType":"compute.v1.instance","ResourceErrorCode":"ZONE_RESOURCE_POOL_EXHAUSTED",
Delete the deployment and try again, selecting a different zone.

Jenkins is an open source automation server that helps you automate the building, testing, and deployment of any project across multiple platforms. Jenkins helps to avoid breaking changes so that you can save time and ensure the delivery of high-quality software. Its web interface provides an easy way to manage and test your applications before taking them to production.

NMake a note of the Adin User and Admin Password, located on the right side of the screen

Visit the site in the site address:
You may need to refresh the page if you get a 503 error
You will see
Please wait while Jenkins is getting ready to work

Login with your username and password

View the menu

You want to check you can administer in the service so ssh into the VM you created using deployment manager in Google Cloud
To verify we are going to shutdown all the services (such as Jenkins) and then restart it by entering the following commands.

This will verify we have admin control over it

Stop script
sudo /opt/bitnami/ctlscript.sh stop
Refresh jenkins page and see if it no longer works
sudo /opt/bitnami/ctlscript.sh restart
Restart the service
Refresh page - dashboard should now be back up

And there you go, able to launch a complete Continuous Integration solution.  demonstrated that you had user access through the Jenkins UI, and  demonstrated administrative control over Jenkins by using SSH to connect to the VM where the service is hosted and by stopping and then restarting the services.



