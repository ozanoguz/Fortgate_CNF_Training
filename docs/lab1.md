# LAB 1: Deploy a fortigatecnf playground for intra-subnet / single vpc

## Deploy the environment
Inside the cloned repo:
```
cd ./terraform-single-vpc
```
```
terraform init
terraform apply
```
Extract the private SSH key
```
terraform output -raw private_key >key.pem
chmod 400 key.pem
```
Access your Jumpbox
```
ssh -i ./key.pem ubuntu@<jumpbox>
```


## Deploy fortigatecnf
### Install / verify cross account setup
xxxx
### Deploy fortigatecnf
xxxx
### Add a LB ??
xxxx
### Test connectivity
xxxx

## Create a policy set
- ex. allow traffic to port 8080 and blcok 8090
- create a dynamic address group
- checkout the routing

## Cleanup for next lab
### Remove the CNF instance
Remove CNF instance in the Fortigate CNF UI

### Remove AWS account from Fortigate CNF

### Remove the CFT

### Destroy playground
```
terraform destroy
```

