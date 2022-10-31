**On Network Automation**  
 _a practial approach towards a network engineering CI/CD pipeline, scripting, and parsing_          

**Tenets:**    
* A CI/CD pipeline should be the only way to deploy network equipment to production.  
* The CD of the pipeline in large-scale networks has limiations and risk that should be accounted for with a modified workflow.  
* Vendor and commercial network tools lead to "death by subscription", open-source and scripting should be used to mitigate that.  

The **Network CI (integration)** uses the version control build of main-->branch-->review-->merge.  
* Continuous Integration - automate the integration of configuration changes.  

The **Network CD (delviery and deployment)** has limitations and risk in network engineering.    
* Continuous Delivery - automate the test.    
* Continuous Deployment - automate production deployment.    

**_Continuous Delivery has limiations in network engineering as a "test" production network is non-existent._**    
**_Continuous Deployment has risk as their is no manual gate at a stage before push to the production network._**    

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
**The Repostiories:**
 
* Ansible playbooks:  [playbooks](https://github.com/sdncoder/playbooks)  
* Python examples:  
* Robot Framework:  
* AWK, SED, Perl, TextFSM:  
* NetworkX Modeling:    
* Containerlab Simulation:     










 
