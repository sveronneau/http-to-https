HTTP to HTTPS
=============

This is a Docker container that forces browser redirection from HTTP to HTTPS for all hosts that hit it.  It also forwards all traffic to a backend service running on port 8080.  Just deploy the container image and make sure your NodePort mapping is port 80 to port 80.  SSL offloading in this case is done at the GCP Global Load Balancer level.

HTTP code 307 could be used to redirect browsers so that the HTTP method does not change (which would happen with old clients using 301/302).
