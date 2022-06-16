# ansible

# 0. Install Ansible on each node
```
sudo apt update
sudo apt install software-properties-common
sudo apt-add-repository --yes --update ppa:ansible/ansible
sudo apt install -y ansible
```

# 1. For SetUp of Master and Worker Node After installing Ubuntu
```
git clone https://github.com/developer-onizuka/ansible
ansible-playbook ansible/update-grub.yaml
ansible-playbook ansible/vagrant-libvirt.yaml
ansible-playbook ansible/openvswitch.yaml
```

# 2. For Kubernetes Master Node
```
git clone https://github.com/developer-onizuka/ansible
ansible-playbook ansible/kubernetes-master.yaml
ansible-playbook ansible/metalLB.yaml
ansible-playbook ansible/istio.yaml
ansible-playbook ansible/persistentVolume-CSI.yaml
ansible-playbook ansible/gpu-operator4.yaml
ansible-playbook ansible/rabbitMQ_KEDA.yaml
ansible-playbook ansible/AzureFunctionsOnKubernetesWithKEDA.yaml
ansible-playbook ansible/https.yaml
ansible-playbook ansible/google-chrome.yaml
```
