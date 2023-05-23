# sampledotnetk8scase

just enough to run this command: "sh kubernetesapply.sh" then "http://{{IP}}:{{Port}}/WeatherForecast" path become a accessable.

kubernetes files are inside of "/kubernetes" path and docker image located inside of this link: https://hub.docker.com/r/baybarse/sample-app/tags

this project was made for the purpose of running the contents of the following project:
https://github.com/roofstacks/case-study-pool/tree/main/infrastructure-developer/mini-cluster


## Summary
Imagine that you have a kubernetes cluster. This cluster orchestrates many services behind the load balancer.

## Details
- Clone the GitHub repo on your local which is specified as [sample-app](sample-app/).
- Create a docker file for building a .net core web app within the docker image.
- You need to create a DockerHub account for uploading image.
- Build a docker image and upload this to the DockerHub.
- End to End HTTP communication is Ok for this case study.
- Create a kubernetes definition file for :
     - Create one ingress for handling HTTP requests from outside the cluster 
     - Create one service for load balancing across the pods 
     - Create a deployment with two pods that are hosting our app instances from DockerHub (which is you've uploaded).
- You should be able to test the application with the following URL pattern with HTTP GET request when you complete it :
     - > http://{{IP}}:{{Port}}/WeatherForecast

- You could prepare one-click install script file as bash or shell to install and run the mini-cluster.
