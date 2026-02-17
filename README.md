# 4640-lab-wk7

### 1. cmds to create new SSH
```
mkdir -p ~/.ssh
chmod 700 ~/.ssh
ssh-keygen -t ed25519 -f ~/.ssh/aws -C "acit4640-ansible-lab" 
chmod 600 ~/.ssh/aws
chmod 644 ~/.ssh/aws.pub
```
### 2. cmds to import and delete aws key pair
```
# make script executable:
chmod +x scripts/import_lab_key scripts/delete_lab_key
# import key to asws:
./scripts/import_lab_key ~/.ssh/aws.pub
#delete key from aws:
./scripts/delete_lab_key
```

### 3. terraform cmds used:
```
# move into directory:
cd terraform
# initialize:
terraform init
# format config files:
terraform fmt
# validate config:
terraform validate
# preview:
terraform plan
# create:
terraform apply
# destroy:
terraform destroy
```

### 4. ansible cmds used 
```
# first copy ec2 public dns into ansible/inventory/hosts.yml
# check syntax:
ansible-playbook --syntax-check playbook.yml
# run playbook:
ansible-playbook playbook.yml
```

### 5. visit web browser
![ss](/lab7.png)