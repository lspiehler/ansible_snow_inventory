# Dependencies

## Install Ansible
Example below is for CentOS 8
```
sudo dnf -y install python3-pip
sudo pip3 install --upgrade pip
pip3 install ansible --user
```

## Clone Repo
```
git clone https://github.com/lspiehler/ansible_snow_inventory.git
cd ansible_snow_inventory
```

## Set environment variables
```
export SN_INSTANCE=<servicenow instance>
export SN_USERNAME=<servicenow username>
export SN_PASSWORD=<servicenow password>
```

## Install dependencies
```
pip3 install netaddr requests
ansible-galaxy collection install -r collections/requirements.yml
```

# Use the inventory
```
ansible-inventory -i cisco.now.yml --list
ansible-inventory -i cisco.now.yml --graph
ansible all -m ping -i cisco.now.yml --list-hosts
```
