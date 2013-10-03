php
===

This module when installed at sites/all/php will prevent the user from changing the state of the php filter module through the Drupal interface.
This may be the smallest and most useful module ever!

Installation
-------------

Disable the php filter module in one of the following ways:
* Drupal interface - http://DRUPAL_ROOT/admin/modules
* drush dis php

Install the code base:
* cd DRUPAL_ROOT/sites/all/modules
* git clone https://github.com/hofmockel/php.git

You don't need to enable this module that is counter to it's goal, right?

How it works
-------------

1. It takes over the name space of the core php filter module.
2. There are no php function conflicts during bootstrap because the module has no functions.
3. It leverages the "required = TRUE" stanza in the php.info that disables the ability to change the state of the module.
4. It levarages the "hidden = TRUE" to remove the module listing entirely from the module listing page.
5. It does not hack core!

I don't see why this will not work with other core modules as well.

Warning
-------

If the core php filter module is on when you place this module in your code base it can not be turned off through the interface.
This module does not disable the module but locks its current enabled state.

The core PHP Filter module can be enabled or disabled with Drush.
