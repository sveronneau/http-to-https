For GCP
=======

Step 1: Create a source repo

Step 2: Clone this repo and sync it with GCp Source Repositories

Step 3: Create a 'build trigger' in Cloud Build

--------- Name: http-to-https

--------- Docker directory: myimage

--------- Dockerfile name: Dockerfile

Step 4: Create instance template from it.

--------- Name: http-to-https

--------- Machine Type: micro

--------- Check the CONTAINER box

--------- Container image: value from container registry (i.e.: eu.gcr.io/project_name/http-https-redirect:latest )

--------- Firewall: HTTP/HTTPS

Step 5: Create an instance group

--------- 
