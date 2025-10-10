This Ansible playbook is for the Solution Pattern found in https://www.solutionpatterns.io/soln-pattern-connectivity-link/solution-pattern/index.html


## **Step 1**
```
git clone https://github.com/rh-soln-pattern-connectivity-link/connectivity-link-ansible
```

## **Step 2**

Update the `inventory.template` file

## **Step 3: Ansible scripts for the deployment of connectivity link (Operators etc)**
```
cd operator-setup
ansible-playbook playbooks/ocp4_workload_connectivity_link.yml  -e ACTION=create -i inventories/inventory.template
```
## **Step 4: Demo setup**
```
cd ../demo-setup
ansible-playbook playbooks/globex.yml -e ACTION=create -e "ocp4_workload_cloud_architecture_workshop_mobile_gateway_url=https://globex-mobile.globex.sandbox2145.opentlc.com"
```
