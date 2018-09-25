HTTP to HTTPS
=============

This is a Docker container that forces browser redirection from HTTP to HTTPS for all hosts that hit it.
HTTP code 307 is used to redirect browsers so that the HTTP method does not change (which would happen with old clients using 301/302).

This repo is designed to be used with GCP Build triggers and used as an image template in a managed instance group fronted by a GLB.

Inspired by: https://blog.realkinetic.com/http-to-https-using-google-cloud-load-balancer-dda57ac97c
