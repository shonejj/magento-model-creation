# magento-model-creation
setup the basic environment 

Name of the module is defined as “VendorName_ModuleName”. First part is name of the vendor and last part is name of the module:
  app/code/VendorName/ModuleName

create registeration.php

create controller/ index/test.php 

Create app/code/VendorName/ModuleName/etc/module.xml 

create app/code/VendorName/ModuleName/etc/frontend/routes.xml 


go to the command line and enable the created module : 

check the status of the modules and enable the created model by using the command line prompt : 

  php bin/magento module:status
  php bin/magento module:enable VendorName_ModuleName
  
then use this command line prompt to clean the cache , upgrade , deploy the code , enable the module , give permission for accessing the files .

sudo php bin/magento setup:upgrade  && sudo php bin/magento setup:static-content:deploy -f && sudo php bin/magento setup:di:compile   && sudo php bin/magento cache:c && sudo php bin/magento cache:flush &&  sudo chmod -R 777 var/* pub/* generated/*
  
  now go to the browser and your url must be of the form : 
  
   http://<yourhost.com>/helloworld/index/test
   
