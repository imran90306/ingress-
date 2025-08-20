# ingress
Step 1: Apply the NGINX Ingress Controller manifest
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.11.3/deploy/static/provider/cloud/deploy.yaml

(This will create the ingress-nginx namespace and all required resources.)

Step 2: Verify installation
kubectl get pods -n ingress-nginx

You should see pods like:

ingress-nginx-controller-xxxxxx   Running

Step 3: Get Service (external IP)
kubectl get svc -n ingress-nginx
