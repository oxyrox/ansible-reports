# ansible-reports #

## Run ###
`ansible-playbook playbook.yml`

## Playbooks ##
* [playbook](playbook.yml): Play the role `role1` with a `print` variable. It's purpose is to test how handlers are dealing with variables, reused in a roles dependency.

## Role ##
* role1: Depends on role2. Will debug the `print` variable and call two handlers, one from *role1* and another from *role2*, both debugging `print`. 
* role2: Contains a handler that debugs the `print` variable as well.
