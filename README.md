# ansible


```
sudo apt update
sudo apt install software-properties-common
sudo apt-add-repository --yes --update ppa:ansible/ansible
sudo apt install ansible
```
```
git clone https://github.com/developer-onizuka/ansible
ansible-playbook ansible/metalLB.yaml
ansible-playbook ansible/istio.yaml
ansible-playbook ansible/persistentVolume-CSI.yaml
ansible-playbook ansible/gpu-operator4.yaml
ansible-playbook ansible/rabbitMQ_KEDA.yaml
ansible-playbook ansible/AzureFunctionsOnKubernetesWithKEDA.yaml
ansible-playbook ansible/https.yaml
ansible-playbook ansible/google-chrome.yaml
```
