1. Install NGINX Ingress Controller using `kubectl apply` according to the
   latest instructions: https://kubernetes.github.io/ingress-nginx/deploy/#quick-start.
   As of this writing: `kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.3.1/deploy/static/provider/cloud/deploy.yaml`
1. `kubectl edit service ingress-nginx-controller -n ingress-nginx`
1. Add `spec.loadBalancerIP` with the value of the load balancer public IP,
   save and exit.
1. `kubectl describe ingress-nginx-controller -n ingress-nginx` - verify
   that it seems to find the load balancer, then move on to the next step.
