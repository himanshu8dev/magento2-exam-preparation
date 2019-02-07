### Magento Areas
  - adminhtml
  - frontend
  - base
  - cron
  - webapi_rest
  - webapi_soap
  
### Necessary file to create module
  - registration.php
  - etc/module.xml
  - composer.json
  
### Module Event Observer SortOrder
  - they don't have any orders
  
### If two diffrent module called same url then what happend ?
  


### create new layout for custom page_layout / which two file are important ?
     view/frontend/layout.xml && view/frontend/page_layout/custom.xml
     
### manually specify the product order on fronend using backend 
    - admin can change "default product listing sort order" by editing particular category.
    - sort order add from product grid

### how install data worked ?
    - whenever setup:upgrade command fire 
    - it will check `setup_module` table values
    - if not available it will insert row & run InstallSchema.php file.
    - if module row existed in table then it will check version from `schema_version` if they find greater version of the existing record it will run UpgradeSchema.php.
    - so very first time on module install InstallSchema.php file run else other it won't get exceuted in any scenario.
    
    
### how plugin works
   - We did practical creating three module
   - Module A, Module B, Module C
   - We register Module A first after Module B & C.
   - Call plugin in three module with same function without giving any sequence in module.xml.
   - Call plugin it will return result of first registered module.
   - then we go and give sequence of module.
   - it will worked on sequence depending.
   - after we applied sort order.
   - It will worked as sort order.
   - now we are try to replicate after,before,around function how they are calling.
   
### observer functionality
  - need to test
   
