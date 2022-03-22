# python-app-test-k8s

- Created a Docker image with helloworld python app which is lightweighted since I used Flask. <br />
  Here is the docker image URL:  kpreeti0131/pyapp:latest     <br />
  
- Hello world python application code is mentioned in app directory.  <br />

- I have used python latest version as base image so whenever we built the image, latest python image get pulled.    <br />

- I have created the image which is running by a non-root user     <br />


**Deploy to Kubernetes**

- Assuming, k8s cluster has already nginx-ingress-controller installed for networking  <br />

- Created the deployment with 4 replicas. At the time of deployment update, due to poddisruptionbudget policy, only 1 pod will become unavailable, i.e, at least 3 Pods will always be up and running for the application.  <br />

-
