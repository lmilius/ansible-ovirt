# ansible-ovirt
Ansible Ovirt installation

## OVirt Installation Instructions
   - Clone repo and setup hosts file
```
git clone https://github.com/lmilius/ansible-ovirt.git
cd ansible-ovirt
sed -i 's/ovirt-01/yourOvirtHostName/' hosts
```
   - Optionally edit any variables here:
```
vi install/group_vars/all.yml
```
   - Run the playbook
```
ansible-playbook -i hosts install/ovirt.yml
```

**File Hierarchy**
```
├── hosts
└── install
    ├── ovirt.yml
    ├── group_vars
    │   └── all.yml
    └── roles
        └── ovirt
            ├── files
            │   ├── 7days.service
            │   └── startserver.sh
            ├── tasks
            │   └── main.yml
            └── templates
                └── serverconfig.xml.j2
```
