Glass module for Drupal
================================
The Glass module for Drupal allows you to push nodes from a Drupal site to Google Glass using the Mirror API. The module will push all nodes from a selected nodequeue to Glass and update those items using the Mirror API when the nodes are updated on your Drupal site.

Items are pushed as an HTML timeline card if there are images present or as a text card if there isn't an image attached. Because access to the Mirror API is currently limited, you'll need to be in the Glass Explorer program to use this module.

This module is currently only for Drupal 6. It's based heavily on [googleglass/mirror-quickstart-php](https://github.com/googleglass/mirror-quickstart-php).

Requirements
-------------------------
* Drupal 6.x
* [Imagecache](https://drupal.org/project/imagecache) module 6.x-2.x
* [Imagefield](https://drupal.org/project/imagefield) module 6.x-3.x
* [Nodequeue](https://drupal.org/project/nodequeue) module 6.x-2.x
* [Libraries](https://drupal.org/project/libraries) module 6.x-2.x
* [Google APIs Client Library for PHP](https://code.google.com/p/google-api-php-client/)

Installation
-------------------------
1. Download the module to your `sites/*/modules` folder
2. Download the [Google APIs Client Library for PHP](https://code.google.com/p/google-api-php-client/) and place it in your `sites/*/libraries` folder. Make sure the folder is named google-api-php-client.
3. Follow the directions on the Google Developers [PHP Quick Start](https://developers.google.com/glass/quickstart/php) page to setup an API project. Under *Authorized Redirect URIs* use yoursite.com/glass/install and be sure to add your site under *Javascript origins*. You'll need the *API Client ID*, *API Client Secret* and *API Simple Key* during the module setup process.
4. Enable the module and finish the setup at yoursite.com/admin/settings/glass.