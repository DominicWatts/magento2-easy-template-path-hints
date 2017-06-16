# Magento 2 Easy Template Path Hints

Overview
-------------

This is an ported version of [Easy Template Path Hints - Magento 1](https://github.com/MagePsycho/MagePsycho_Easypathhints) for Magento 2

It is used to enable the template path hints on the fly just by using query strings.

Functionality
-------------
- Turn on template path hints on the fly for frontend
- Turn on template path hints on the fly for backend
- Option to require access code
- Option to save settings in cookie


<h2>Install:</h2>
First add repository to composer configuration:
```bash
composer config repositories.magepsychotemplatehints git git@github.com:MagePsycho/magento2-easy-template-path-hints
```
Require new package with composer:
```bash
composer require magepsycho/magento2-easy-template-path-hints:dev-master
```
Enable module
```bash
php bin/magento module:enable MagePsycho_Easypathhints --clear-static-content
```

Flush everything:
```bash
php bin/magento setup:upgrade
```

How to use?
-------------
Some Examples
1. Enable template path hints without access code:
    * http://magento-store-url.com/any-page?tp=1

2. Enable template path hints with access code:
    * http://magento-store-url.com/any-page?tp=1&code=access-code

3. Enable template path hints with cookie
    * http://magento-store-url.com/any-page?tp=1&code=your-access-code&cookie=1

Screenshot
-----------
![Backend Settings](https://raw.github.com/MagePsycho/magento2-easy-template-path-hints/master/docs/backend-settings.png "Backend Settings")

Changelog
-------------
**Version 1.1.0 (2017-06-16)**
* Refactored the code (Logger, Cookie etc.)
* Fixed template path hints not working for Magento versions 2.1.3+

**Version 1.0.1 (2016-04-03)**
* Formatted code as per Code Sniffer
* Acl implementation, removal of relative xsd path etc.

**Version 1.0.0 (2015-10-30)**
* Initial Release

Support
-------------
If you encounter any problems or bugs, please create an issue on [GitHub](https://github.com/MagePsycho/magento2-easy-template-path-hints/issues).

Contribution
-------------
Any contribution to the development of Easy Template Path Hints is highly welcome. The best possibility to provide any code is to open a [pull request on GitHub](https://github.com/MagePsycho/magento2-easy-template-path-hints/pulls).

Licence
-------
[Open Software License (OSL 3.0)](http://opensource.org/licenses/osl-3.0.php)

Copyright
---------
(c) 2015 Raj KB
