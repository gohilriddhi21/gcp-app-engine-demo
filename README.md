# Simple Python Application Deployment on GCP App Engine 

This project demos how to deploy your Python application to GCP App Engine

## Steps:
1. Create a Basic Python Application
2. Write YAML for configuring the app engine service
3. Enable the App Engine API on the GCP console.
4. Grant Storage Object Viewer permission to your service account attached to the enabled service. 
5. Hit the ```gcloud app deploy``` command
6. All Done!


## Sample commands:
- ```gcloud app browse --version <version ID>```
- ```gcloud app services list``` : To list all the services in the configured GCP project.  
- ```gcloud app versions list``` : To list all the services with their versions.
- ```gcloud app instaces list``` : To list all the instance in that App engine Application.
- ```gcloud app deploy --version=<vid> --no-promote``` : To **NOT** migrate the traffic to the newly deployed version.
- ```gcloud app services set-traffic --splits=<v1_id>=.5,<v2_id>=.5 --split-by=random``` : To split traffic by 50% each to specified versions of services.
  
