Net-square_ansible_assessment
=========

Ansible script for certificate configuration and python app installation.

Requirements
------------

This playbook is for **RedHat/CentOS** and can be implemented for all OS like Debian, Ubuntu etc... by making the required changes.
All other pre-requisites required for the operation are included in the playbook no need of any mannual operations.

Role Variables
--------------

Three Itesms have been parameterized as asked i.e., 
1. port on which the application will run
2. Deployment location
3. Name of the deployment file(wheel file)

These parameters can be found in [vars/main.yml](https://github.com/nizamgms/Net-square_ansible_assessment/blob/main/vars/main.yml) these cannot be overridden during run time and can be changed in file if required, we can also configure these variables to overwrite during the runtime for that it needs to be configured at a lover level variables.

Example Playbook
----------------

Including an example of how to use this role (for instance, with variables passed in as parameters)
just execute the below given command to start the deployment

Execution file=[converge.yml](https://github.com/nizamgms/Net-square_ansible_assessment/blob/main/molecule/default/converge.yml)

    ansible-playbook converge.yml 
    (or)
    ansible-playbook converge.yml -e "deployment_path=/opt/example wheel_file=Example-1.1.1-py3-none-any.whl port=5050" (if configured low level variables, it can be overridden during runtime like this) 
    ansible-playbook Net-square_ansible_assessment/molecule/default/converge.yml -i inventory --ask-vault-pass (enter Passowrd when promted)
    ansible-playbook Net-square_ansible_assessment/molecule/default/converge.yml -i inventory --ask-vault-pass --skip-tags "prepare" (use this to skip any particular task, and can also be used to run only selected task)

                                                                                                                         


Author Information
------------------

    Nizamuddin M D
    DevOps Engineer
    Email: mdnizam.gms@gmail.com
    
