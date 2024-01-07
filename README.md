# ansible
> https://github.com/developer-onizuka/setup-mintLinux#5-run-vagrant-and-gpu-workloads

# 1. Install Ansible on each node
```
sudo apt update
sudo apt install -y software-properties-common
sudo apt-add-repository --yes --update ppa:ansible/ansible
sudo apt install -y ansible
```

# 2. For SetUp of BearMetal Node (Dell Precision at my home) After installing Ubuntu
```
git clone https://github.com/developer-onizuka/ansible
ansible-playbook ansible/vagrant-libvirt.yaml
ansible-playbook ansible/openvswitch.yaml (<-- Need modification of IPs)
```

# 3. For SetUp BearMetal Nodes (Dell Optiplex at my home) After installing Ubuntu
```
git clone https://github.com/developer-onizuka/ansible
ansible-playbook ansible/update-grub.yaml
ansible-playbook ansible/vagrant-libvirt.yaml
ansible-playbook ansible/openvswitch.yaml (<-- Need modification of IPs)
```

# 4. For Only Kubernetes Master Node (Virtual Machine on Precision at my home)
```
vagrant ssh
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

# 4. Completion-bash
> https://qiita.com/superbrothers/items/631508630320aa1dbcbc
