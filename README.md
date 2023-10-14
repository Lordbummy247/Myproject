# KUBERNETES
## How To create Pods on Kubernetes (Guides)
- mkdir lordbummy [Create a directory; in this case, lordbummy is the directory]
- cd lordbummy [Access the directory]
- minikube start --driver=docker [Start the minikube]
- kubectl run hayorpod --image=nginx [create a pod. hayorpod is the pod name and Nginx is the image]
- kubectl get pod [To confirm the creation and running of the pod]
- kubectl get pod hayorpod -o yaml [To see the Pod in yaml format. It displays the config of the POD]
- kubectl run hayorpoddy --image=nginx --dry-run=client -o yaml > becky.yaml [Creation of a pod in yaml file. This allows for easy edition of the pod]
- cat becky.yaml [This allows to read data from the pod]
