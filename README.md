# 2 apps to deploy in aks

### First guestbook

Its app from kubernetes guide [Link](https://kubernetes.io/docs/tutorials/stateless-application/guestbook/) 

In this tutorial the service Frontend is configurated in Cluster Ip, that's a problem to get in from a external browser
#### We update the the service to LoadBalancer Type with this command 
``
kubectl patch svc frontend -p '{"spec": {"ports": [{"port": 443,"targetPort": 443,"name": "https"},{"port": 80,"targetPort": 80,"name": "http"}],"type": "LoadBalancer"}}'
``

### React-Node App

It's a fork of [Link](https://github.com/bbachi/react-nodejs-example), for the deploy we build the image and Save it in the Azure Container register in the manifest.yml we can see a deployment with the container of ACR also we can see a service using LoadBalancer type


## Group  

Juan Camilo Guzman
Juan Camilo Espinoza
