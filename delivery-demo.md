# Delivery Demo

## Initial one time set up (per project)

* Log into the [Delivery Server](https://10.194.9.71/e/emea_enterprise/#/login)
* Click on the Organisation named [dbaas](https://10.194.9.71/e/emea_enterprise/#/organizations/dbaas).  
* Click on the Project name [sitedbaas](https://10.194.9.71/e/emea_enterprise/#/organizations/dbaas/projects/sitedbaas).
* In the top of the page click the 'Clone Project' button.  Select and copy the clone command. 
  * `delivery clone sitedbaas --ent=emea_enterprise --org=dbaas --user=<YOUR USERNAME> --server=10.194.9.71`
* In a command prompt enter the delivery clone command to clone the project onto your local workspace, then change directory into the project within your workspace. 

       
        cd <MY_LOCAL_WORKSPACE>
        delivery clone sitedbaas --ent=emea_enterprise --org=dbaas --user=<YOUR USERNAME> --server=10.194.9.71
        cd sitedbaas
        

## Submit a change

  1. Create feature branch.

        
        git checkout -b my_feature_branch
        

  2. Make a changes to the cookbook.

        
        vi attributes/default.rb  # Edit the default['sitedbaas']['company-name'] value
        vi metadata.rb            # Bump the version of the cookbook
        
 
  3. Add the changes.

        
        git add .
        

  4. Commit the changes.

        
        git commit -m "My awesome new feature"
        

  4. Deliver the change

        
        delivery review
        
