Tested on GCP with GLB with SSL and GKE Deployment
==================================================

Step 1: Create a source repo

Step 2: Clone this repo and sync it with GCP Source Repositories

Step 3: Create a 'build trigger' in Cloud Build

--- Name: http-to-https

--- Docker directory: myimage

--- Dockerfile name: Dockerfile

--- Create

Step 4: Insert the container creation code in your YAML file for your GKE Deployment.

```
      containers:
      - image: GCR.IO Image Pull link.  i.e. (eu.gcr.io/hd-dish-dev/http-https-redirect:abc123xyz)
        imagePullPolicy: Always
        name: nginx-http-https
        ports:
        - containerPort: 80
          name: http
          protocol: TCP
```

Step 5: Expose a Service where port is 80 and target port is 80.

Step 6: Create an Ingress Loadbalancer with an Frontend SSL Policy containing your site certificates.

Step 7: Test it out.
