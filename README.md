### TODO:
- Read K8s docs (especially concept part) and K8s in action
      - **Read the docs and update the Concept section of this README**
- More about ingress-nginx: https://www.joyfulbikeshedding.com/blog/2018-03-26-studying-the-kubernetes-ingress-system.html.  
- How to deploy and understand K8s uses resource in Production environment: https://docs.aws.amazon.com/eks/latest/userguide/getting-started-console.html

### Working Flow
- Dockerize each service with ```Docker``` and publish them to ```Docker hub``` 
      - Writing ```Dockerfile```
      - Building ```Docker image```
      - Publish the image to Docker hub
- Write a config file to create ```Deployment``` for each service. This will create a controller object that declaratively manage the ```Pod```
      - Here inside the ```Deployment``` config file, we can specify to get the ```Docker image``` we created above from Docker hub to build the ```Container``` 
- Write a config file to create ```Service``` for each service. This will expose the ```Pod``` to the outer world and allow other ```Pod``` to communicate with it 
- A database service would need a ```Persistent Volume``` and ```Persistent Volume Claim (PVC)```, so we would have to write a seperate config file for that and add that configuration to the ```Deployment``` file of the database service
- We also need an ```Ingress``` object to handle outer traffic into our ```Cluster```, in this application, we use ```ingress-nginx```, a specific implementation of an ```Ingress``. In the config file, we can specify all routing rules that we want it to handle

### Concept (Will be regularly updated)
- When we write config file for ```k8s```, it will create ```Object```, and there are many ```Kind``` of ```Object``` and each will handle a totally different purposes.
      - Inside the config file, we have to explicitly specify the ```Kind``` and its associated ```apiVersion```

#### Cluster

#### Node

#### Pod

#### Container

#### Service
- This ```Kind``` of ```Object``` is to set up networking inside a ```k8s``` cluster
- This will link to the ```Pod``` by a ```label``` system, as long as it has same ```label``, it will be linked and controlled


### Architecture:
<img src="misc/K8s local architecture.png" width="700">
