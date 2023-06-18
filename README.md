# MULTI-CLOUD PROJECT

## INTRODUCTION
Migrated existing Covid-19 test data storage application for a luxory hotel chain from on premise storage to multi-cloud solution
The following cloud technologies and Devops tools were used-
  * Google Cloud Platform
  * Amazon Web Services Cloud
  * Kubernetes
  * Terraform
  * Docker

## PROBLEM STATEMENT
A hotel chain has a rule of taking COVID-19 test information(test pdf) of guests checking in and storing this information using a database for guest information and pdf metadata. They are having scalability issues with their architecture
Below is the existing architecture - 
![Old architecture](/images/old_achitecture.png)

The hotel chain has decided to migrate this application to a public cloud and have decided to use a multicloud setup to get a cost efficient solution. 
The solutions architect has designed the following solution - 
![New architecture](/images/new_architecture.png)

## WORKING
 * 2 AWS IAM user created for terraform and for the application.
 * terraform is initialized on GCP to spawn the following resources
    1. Google Kubernetes Engine 
    2. Google Cloud SQL instance
    3. Amazon S3 Instance
 * Docker Image of the existing application is created and connected to the kubernetes cluster. 
 * SQL instance is linked to the application
 * Data migrated from existing solution to cloud architecture, pdf files stored in s3 bucket.

## RESULT
The final application running on the new architecture is shown in the following pictures. 
Website Home Page
![Website Landing Page](/images/landing_page.png)

The Existing Guest List
![View Guest List](/images/guest_list.png)

Adding new Guest Information
![Adding new Guest information](/images/adding_new_guest.png)

Opening the pdf file through the link for a guest
![Testing pdf File link](/images/testing_pdf_file.png)
