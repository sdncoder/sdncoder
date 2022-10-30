**the network automation framework**  
_practical approaches towards a network engineering CI/CD_  

 ```mermaid
   stateDiagram
   direction LR
    [*] --> main
    main --> branch : 1
    state branch {
    direction LR
    change --> review : 2
    review --> merge : 3
    }
    merge --> main : 4
    main --> ansible : 5 git pull
    state network {
    ansible --> router : 6 playbook
    }
 ```
 


* [network CI/CD](https://github.com/sdncoder/network-ci-cd)  
* [ansible playbooks](https://github.com/sdncoder/playbooks)  
* [robot testing](https://github.com/sdncoder/robot)  
* [diagrams as code](https://github.com/sdncoder/diagrams)
* [network analysis with python](https://github.com/sdncoder/sr-te-networkx)  
* [parsing network data](https://github.com/sdncoder/text-parsing)  










 
