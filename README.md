# cdevops-k8sdashboard

k8s dashboard as a hello world.....with dependencies

```
git submodule update --init --recursive
pip install ansible kubernetes
ansible-playbook up.yaml
kubectl get pods
```
Then with the 0th pod, dashboard-kong-68687498db-5jk5m in my case run:

```
kubectl -n default port-forward dashboard-kong-68687498db-5jk5m 8443:8443
```
In vscode you will need to forward the port to localhost.

You will need a bearer token to access the dashboard. Open a 2nd terminal window and run:

```
kubectl -n default create token admin-user
```
To resolve issue for kubectl-config file and API client connection

copy & paste the environment variables from the .devcontainer to the root of the repo 
commit & Sync the changes and delete the exsisting the codespace and create a new codespace
and again re run the same commands as above.

```
git submodule update --init --recursive
pip install ansible kubernetes
ansible-playbook up.yaml
kubectl get pods




