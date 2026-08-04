# Pods with YAML

Kubernete uses YAML files as inputs for the creation objects such as pods, replicas, deployments, services, etc. <br>
They all follow the same structure. 

A kubernetes defintion file always containers four top level fields.
- API Version, Kind, Metadata, Spec

They are located in the root level and are required fields. They must be in the configuration file. 

**API Version** - This is the version of Kubernetes API we are using to create the object. 
- Depending on what we're trying to create, we must use the right API version. 

**Kind** - Refers to the type of object we are trying to create, for example a Pod or other possible values could be replica set, deployment, or service. 

Metadata - Data about the object such as name and labels. This is in the form of a dictionary. 
- The name is a string value so you can name your Pod.
- The labels is a dictionary so you can have as many key value pairs needed.

```
apiVersion: v1
kind: Pod
metadata: 
  name: myapp-pod
  labels:
    app: myapp
    type: front-end
spec:
  containers:
    - name: nginx-container
      image: nginx
```

Once the file is created `kubectl create -f pod-definition.yaml` - Deploys the Pod <br>
`kubectl get pods` - To see the pods ran <br>
`kubtcel describe pod <my-app>` Shows a detailed information

The `cat` (concatenate) command is used to view, create, and combine file contents directly from the terminal.
- It allows users to quickly work with the file content without opening a text editor.
- Primarily used to display the contents of files on the terminal.

`kubectl apply` <br>
`kubectl create` <br>
If you're creating a new object you can use either:
- `kubectl apply -f <pod.yaml>`
- `kubectl create -f <pod.yaml>`
