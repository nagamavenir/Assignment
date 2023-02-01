# Assignment on Service <You have deployed an application, that is listening at port 8000. You used a replica-set to deploy it and created a NodePort service to make it accessible. But when you test it, somehow the application is not reachable at the port. Write down your approach and sequentially all the steps that you will take to find out the issue.>
# My approach to find the issue would be as follows:
# Check the status of the pods:
Run 'kubectl get pods' to see if the pods for the application are running correctly and if there are any issues with them.
# Check the logs of the pods: 
If the pods are not running, check their logs using 'kubectl logs [pod_name]' to see if there are any error messages that can help identify the issue.
Verify the service definition:
Run 'kubectl describe service [service_name]' to check if the NodePort and the target port are correctly defined.
Check the NodePort: Use kubectl get services to check the assigned NodePort and then access the application using 
http://[node_ip]:[NodePort].
