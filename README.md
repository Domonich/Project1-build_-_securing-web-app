# Project1-build_-_securing-web-app
Securing Cloud Applications using Azure

Project 1: Securing Cloud Applications using Azure:{Keyvaults, App Services, Front Dorr, WAF} PHP, HTML, DOCKER, OpenSSL. Developed and designed a cyber-blog web application using Azure cloud services. Created and stored SSL certificates in Azure's web vault and bound them to secure the web app. Protected the web app by utilizing Azure’s security features such as azure front doot, WAF, and Security Center.

I used Microsoft Azure to build and host my own “cyber-blog” web application. I secured it with an SSL certificate and applied Azure’s security features to protect it. 
Our requirements included:

Hosting the web application using Azure’s Cloud Services
Using Azure’s App Service resource to create the web application
Choosing a domain with “Godaddy or Azure” (choose what you selected)
Deploying a Docker container that had a framework for a blog webpage
SSHing  into the container to customize the webpage
Creating a Self-signed certificate with OpenSSL 
Storing the certificate in Azure’s Key vault
Binding the certificate to the website (If you didn't select the free option)
After determining the security issues with a self-signed certificate, creating and bound a managed CA-approved certificate to the web application
Deploying Azure’s Front Door, and configuring a WAF rule to restrict traffic from certain countries
Analyzing Azure’s Security Center recommendations and applying the recommended fix

What were the advantages for choosing Azure’s App Service resource, instead of creating a Virtual Machine From scratch?

Using Azure App Service, we can pass the responsibility of managing features outside of the web application to the cloud service provider
In other words, we are only responsible for deploying and managing their web application and its associated data
Deploying web applications can be done much faster, as users don't have to be concerned about configuring their OS
The user doesn't have to worry about the OS and middleware maintenance, such as installing software updates and patching
Azure App services are cheaper to run than Virtual machines
Azure App services have built-in features for securing and hosting a web application, such as DNS, Web App Firewalls, Domain purchasing, and SSL certification binding.


What were the security issues you encountered when you used a self-signed certificate?

A self-signed certificate is a certificate that has not been signed by a certificate authority. While these certificates are simple to create and have no expense almost all browsers will alert the user visiting the webpage that is signed with a self-signed certificate that the webpage is not trusted by a Certificate Authority in the browser’s root store and to proceed with caution. 


How did you address that security concern?

I created and bound a managed certificate provided by Azure, as this is a trusted certificate that has been approved by a CA which most browsers trust.


What is Azure’s Front Door, and how did you use its WAF feature?

Azure’s Front Door is a  Cloud Resource, it resides in front of my web application to protect it. It works on the Application Layer of the OSI Model (Layer 7). Its primary solution is a load balancer. It can incorporate a Web Application Firewall (WAF) to protect against web vulnerability attacks.  With the WAF, I applied a custom rule to protect against web requests from countries that I wasn't expecting any traffic from.  This could help protect against potential attacks where I knew I wasn't expecting any visitors.


What is Azure’s Security Center, and how did you apply its features?

Azure Security Center is a management system that provides best practices and   recommendations to enhance the security of your cloud resources. When I checked it, it had several security recommendations with various criticalities. One recommendation was to require FTP access into the web application with FTPS, which is the encrypted version of FTP.

Technical Brief: https://docs.google.com/document/d/1toOn15yS86kJ1Y01TaslawXFomYjf41wjY7ubkRmFpM/edit?usp=sharing
