*** Docker
https://stackoverflow.com/questions/31251356/how-to-get-a-list-of-images-on-docker-registry-v2


*** Bugs and fix:
https://stackoverflow.com/questions/56220392/kubectl-unable-to-connect-to-the-server-dial-tcp-192-168-214-1366443-conne

https://kubernetes.io/docs/tasks/configure-pod-container/pull-image-private-registry/
https://kubernetes.io/docs/tasks/configure-pod-container/pull-image-private-registry/
https://skryvets.com/blog/2021/03/15/kubernetes-pull-image-from-private-ecr-registry/
https://komodor.com/learn/how-to-fix-createcontainerconfigerror-and-createcontainer-errors/#:~:text=If%20the%20error%20is%20waiting,object%20required%20by%20the%20container.
*** Templates + Tutorials:
https://kubernetes.io/docs/tutorials/
https://opensource.com/article/20/5/helm-charts
https://linuxhint.com/how-to-set-up-a-kubernetes-cluster-on-an-aws-ec2-instance/      list private zone: aws route53 list-hosted-zones-by-name (The name zone has '.' at the end)

*** Note:
Get NODEPORT and NODE_IP then can do: wget http://$NODE_IP:$NODE_PORT 
```sh
  export NODE_PORT=$(kubectl get --namespace default -o jsonpath="{.spec.ports[0].nodePort}" services cherry-chart)
  export NODE_IP=$(kubectl get nodes --namespace default -o jsonpath="{.items[0].status.addresses[0].address}")
  echo http://$NODE_IP:$NODE_PORT
```
**** Commands:
1. kubectl port-forward $POD_NAME <port of using localhost>:<port of Pod>
   ex. kubectl port-forward $POD_NAME 3000:80 
2. 
kubectl get - list resources
kubectl describe - show detailed information about a resource
kubectl logs - print the logs from a container in a pod
kubectl exec - execute a command on a container in a pod
