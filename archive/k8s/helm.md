## How to reproduce a Helm "Chart" for Prometheus and Grafana
helm repo add stable https://charts.helm.sh/stable
helm repo update
helm install prometheus stable/prometheus-operator
kubectl logs prometheus-grafana-76cbbd744f-6hkhh -c grafana
kubectl port-forward deployment/prometheus-grafana 3000
