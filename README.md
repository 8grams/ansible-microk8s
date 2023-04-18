# ansible-microk8s
Simple Ansible Playbook to install MicroK8s

## Usage

1. Make sure you have ansible installed in your machine. Please refers Ansible official website: https://www.ansible.com/ 

2. Create a VM with Public IP Address
3. Update `inventory.yaml`, put your VM's IP Address there
4. Update `install_microk8s.yaml`, replace `egrams` with your username
5. Put VM's SSH Private Key `id_rsa` inside `keys` folder
5. Test ansible connection with health check playbook
```
~$ ansible-playbook health_check
```
6. If it's good, then install MicroK8s
```
~$ ansible-playbook install_microk8s
```

## Additional Setup
Please refers to: https://8grams.tech/blog/how-to-setup-low-cost-zero-ops-full-featured-kubernetes-cluster-in-a-single-vm-using-microk8s/