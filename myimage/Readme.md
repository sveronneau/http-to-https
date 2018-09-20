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

--------- Container image: value from container registry (i.e.: eu.gcr.io/project_name/repo_name:latest )

--------- Firewall: HTTP/HTTPS

--------- Create

Step 5: Create an instance group

--------- Name: http-to-https

--------- Multi-zone / Choose Zone and Region

--------- Instance template: http-to-https

--------- Target CPU usage: 70

--------- Minimum number of instances: 1

--------- Maximum number of instances: 3

--------- Health check: Create another health check

---------------- Name: http-to-https 

---------------- Protocol: TCP

---------------- Port: 80

---------------- Check interval: 10

---------------- Timeout: 10

---------------- Healthy threshold: 3

---------------- Unhealthy threshold: 3

--------- Create

Step 6:
