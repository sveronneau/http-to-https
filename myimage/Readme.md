For GCP
=======

Step 1: Create a source repo

Step 2: Clone this repo and sync it with GCp Source Repositories

Step 3: Create a 'build trigger' in Cloud Build

--------- Name: http-to-https

--------- Docker directory: myimage

--------- Dockerfile name: Dockerfile

--------- Create

Step 4: Create instance template from it.

--------- Name: http-to-https

--------- Machine Type: micro

--------- Check the CONTAINER box

--------- Container image: value from container registry (i.e.: eu.gcr.io/project_name/repo_name:SHA VALUE )

--------- Firewall: HTTP

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

Step 6: Update Managed Instace Group

--------- Go inside your newly creaed MiG and click EDIT

--------- Click on Specify port name mapping + Add Item

---------------- Port name: http

---------------- Port numbers: 80

--------- Save

Step 7: On an existing GCLB - Create a backend service

--------- Name: http-to-https

--------- Protocol: http

--------- Named port: http

--------- Instance group: http-to-https

--------- Port numbers: 80

--------- Done

--------- Health Check: http-to-https

--------- Create
