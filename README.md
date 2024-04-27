# Motivation
A simple k8s demo show casing basic concepts of kubernetes

# How to run this?

* Install minikube 
https://kubernetes.io/docs/tasks/tools/install-minikube/

* Start the minikube
``` minikube start ```

* Apply config map

``` kubectl apply -f mongo-config.yml ```

* Apply secret

``` kubectl apply -f mongo-secret.yml ```

* Apply mongo db config

``` kubectl apply -f mongo.yml ```

* Apply web app config

``` kubectl apply -f mongo-config.yml ```

* Verify everything is up and running

``` minikube dashboard ```

* Try accessing the web app via web browser

    * Get the external IP of minikube 

        ```  kubectl get node -o wide ```

    * Type the following url

        ``` {EXTERNAL-IP}:30100 ```

    NOTE: If this doesn't work , try exposing the port using port forwarding
        ``` kubectl port-forward svc/webapp-service 30100:3000 ```

    * Type the following url

        ``` http://localhost:30100/ ```



   
