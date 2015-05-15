# Delivery Demo

## Initial one time set up (per project)

* Setup Workstation [ChefDK, Git, Delivery CLI](setup-workstation.md) 
* Log into the [Delivery Server](https://10.194.9.71/e/emea_enterprise/#/login)
* Click on the Organisation named [dbaas](https://10.194.9.71/e/emea_enterprise/#/organizations/dbaas).  
* Click on the Project name [sitedbaas](https://10.194.9.71/e/emea_enterprise/#/organizations/dbaas/projects/sitedbaas).
* In the top of the page click the 'Clone Project' button.  Select and copy the clone command. 
       
       delivery clone sitedbaas --ent=emea_enterprise --org=dbaas --user=<YOUR USERNAME> --server=10.194.9.71
       
* In a command prompt enter the delivery clone command to clone the project onto your local workspace, then change directory into the project within your workspace. 

        
        cd <MY_LOCAL_WORKSPACE>
        delivery clone sitedbaas --ent=emea_enterprise --org=dbaas --user=<YOUR USERNAME> --server=10.194.9.71
        cd sitedbaas
        

## Submit a change

  1. Change into the project directory.

        
        cd <MY_LOCAL_WORKSPACE>/sitedbaas
        

  2. Create feature branch.

        
        git checkout -b my_feature_branch
        

  3. Make a changes to the cookbook.

        
        vi attributes/default.rb  # Edit the default['sitedbaas']['company-name'] value
        vi metadata.rb            # Bump the version of the cookbook
        
 
  4. Add the changes.

        
        git add .
        

  5. Commit the changes.

        
        git commit -m "My awesome new feature"
        

  6. Deliver the change

        
        delivery review
        

  7. Watch the change in the delivery server.  When the job is ready for review enter a comment and approve the change.

        
        http://replygif.net/i/716.gif
        

  8. When the change is deployed to in the Acceptance stage then check the change in a browser
   * Acceptance: [http://10.194.8.123/](http://10.194.8.123/)

  9. When you are happy with acceptance, then click the deliver button.  Check each environment as they are deployed.
   * Union: [http://10.194.15.106/](http://10.194.15.106/)
   * Rehearsal: [http://10.194.11.252/](http://10.194.11.252/)
   * Delivered: [http://10.194.8.147/](http://10.194.8.147/)

[Back Home](README.md)
