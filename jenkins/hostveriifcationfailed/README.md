Problem statement :
Jenkins build is failing while checkout the code from bitbucket cloud

Host key verification failed.
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

SOlution :

To fix this, disabled CheckHostIP by adding the below config in your ~/.ssh/config file

Host bitbucket.org
       CheckHostIP no

RCA : Everytime bitbucket.org is going to  change the IP address and it may cause the failure of git clone       
