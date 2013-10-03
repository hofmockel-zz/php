php
===

This module when installed at sites/all/php will prevent the user from changing the state of the php filter module.
This may be the smallest and most useful module ever!

Installation
-------------

Disable the php filter module in one of the following ways:
* Drupal interface - http://DRUPAL_ROOT/admin/modules
* drush dis php

cd DRUPAL_ROOT/sites/all/modules
git clone https://github.com/hofmockel/php.git
!you do not need to enable the module!

How it works
-------------

First, it takes over the name space of the core php filter module.
Second, there are no function conflicts because the module has no functions.
Third, it leverages the "required = TRUE" stanza in the php.info that disables the ability to change the state of the module.

Warning
-------

If the core php filter module is on when you place this module in your code base it can not be turned off through the interface.
This module does not disable the module but locks its current enabled state.

The core PHP Filter module can be enabled or disabled with Drush.
