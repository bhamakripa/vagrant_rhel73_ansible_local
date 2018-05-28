# vagrant_rhel73_ansible_local

Commands used were 
------------------
    cd e:

    cd SI/HashiCorp/rhel75/

    vagrant init

Modify Vagrantfile
------------------
    vagrant up

    vagrant ssh

Later to force provision, use below command
------------------------------------
    vagrant reload --provision

Commit github repo:
------------------
    git remote add origin "https://github.com/bhamakripa/vagrant_rhel73_ansible_local.git"
  
    git pull origin master --allow-unrelated-histories
