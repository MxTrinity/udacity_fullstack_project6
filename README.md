# udacity_fullstack_project6

## **PROJECT**
Setting up a Linux server on amazon webservices server to run web application code.
the webapp is a flask based web app that utilizes a sqllite3 database and google oauth

## **DEPENDENCIES**
* an internet connection
* a modern/updated web browser (sorry IE fans you don't count)

## **SETUP/INSTALLATION & USAGE**
* Setup: List of modifications to server

-update packages
-modify firewall to deny all traffic except on ports for ntp ssh & http
-change ssh port to 2200
-modify amazon firewall to match ubuntu

-create user grader
-add grader to suoers

-install apache, mod_wsgi, postgres
-create mod_wsgi file for the application, spefifying path to app and adding the application to the python path
-create virtual host that links to wsgi script
-add redirect to virtual host in hostfile
-enable site and mod-wgsi

-install python-pip
-pip install flask

-install sqlalchemy,passlib,oauth2client,flask_httpauth
-create database
-make database & contining directory writable with chmod
-move secret key to beingning of app so that it doesn't screw
-restart apache

to use 
navigate to
http://ec2-18-191-88-47.us-east-2.compute.amazonaws.com/

to ssh
http://ec2-18-191-88-47.us-east-2.compute.amazonaws.com/
on port 2200
login as "grader"
key in instructor's notes (sorry random folks)

### **NOTES/KNOWN BUGS**

### **ATTRIBUTION INFO**
* big shouts to the documentation teams for Flask & Apache
* followed this tutorial: https://www.jakowicz.com/flask-apache-wsgi/
* STACK.OVER.FLOW. 4Lyfe