Ansible code snipets for http://isbyr.com/using-goss-and-ansible-templates-for-system-testing/

## Deploy goss to severs
to be done only once per environment, replace `dev` with either `sit` or `prd` as applicable\
`ansible-playbook -i inventory/dev goss_deploy.yml -e "splunk_group=*" -k -K`

## Run Tests per role
Replace `dev` with either `sit` or `prd` as applicable\
Replace 'syslog' with one of the these `uf|hf|ds` (hf and ds tests are not created yet)\
`ansible-playbook -i inventory/dev goss_run_test.yml -e "splunk_group=uf"  -k -K`
