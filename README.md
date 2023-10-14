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
## How to Create a sidecar by editing the yaml file
- vim becky.yaml [vim into the yaml file. In the container section and below the first container name & image, follow the same pattern and insert the name and image of choice, then save what is edited]
- kubectl apply -f becky.yaml [This display the container that was created in yaml file. This container is called the Sidecar]
- kubectl get pod [This will display the number of pod created and running, inclusive of the additional pod - sidecar]
## Deployment of Pod
- kubectl create deployment hayordep --image=nginx [This is to create deployment of the pod]
- kubectle edit deployment hayordep [The deployment can be edited in order to increase the replica to any number of choice]
- Kubectl deleted deployment [This is used to delete deployment]
- kubectl get deployment [This allows the display of created and running deployment]
- kubectl create deployment hayor-deploy --image=nginx  [This can be used to create deployment as well]
- kubectl scale deployment hayor-deploy --replicas=4 [This can also be used to scale the deployment to any number of choice]
- Kubectl get deployment [run this to reconfirm the confirmed number of replica created and running]
- minikube dashboard [This is to view all the deployment on the vmware default browser. Always check the default browser as soon as this is being ran]
- minikube stop [Use this to stop minikube from running]
