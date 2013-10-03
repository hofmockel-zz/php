php
===

This module when installed in sites/all will prevent the user from changing the state of the php filter module.

Installation
-------------

disable the php filter module in one of the following ways:
* Drupal interface - DRUPAL_ROOT/admin/modules
* 
cd DRUPAL_ROOT/sites/all/modules
git clone https://github.com/ISUITC/php.git
* you do not need to 


How it works
-------------

First, it takes over the name space of the core php filter module.
Second, there are no function conflicts because the module has no functions.
Third, it leverages the "required = TRUE" stanza in the php.info that disables the ability to change the state of the module.

If the core php filter module is on when you place this module in your code base it can not be turned off as well.
This module does not disable the module but locks its current enabled state.
