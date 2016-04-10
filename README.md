# magento2_italian_language_pack

## information

This translation pack is basend on [Magento2 Italian translation on Crowdin.com](https://crowdin.com/project/magento-2/it#)

Italian is not a spoken language of mine. Therefore it could take some days to confirm translation pull requests

## installation

### with composer

Go to your magento2 installation ./htdocs

add this repository to your composer.json file:
```
  "repositories": [
    {
      "type": "vcs",
      "url":  "https://github.com/kkrieger85/magento2_italian_language_pack.git"
    },
    {
        ///Other repositories
    }
     ],
```

on your shell:
```
    composer require kkrieger85/magento2-locale-it-it:"dev-master"
    
    php bin/magento setup:static-content:deploy it_IT
``` 


## update with your own translation

On Magento2 you could [extend other language packs](http://devdocs.magento.com/guides/v2.0/config-guide/cli/config-cli-subcommands-i18n.html#config-cli-subcommands-xlate-pack-meta-xml):

[Create your own translation](http://devdocs.magento.com/guides/v2.0/config-guide/cli/config-cli-subcommands-i18n.html#m2devgde-xlate-files) in `app/i18n/[namespace]/[packagename]` with 
- `composer.json`
- `it_IT.csv`
- `language.xml`
- `registration.php`

Put your own translations into it_IT.csv

And use language.xml this way:
```
<?xml version="1.0"?>
<language xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="urn:magento:framework:App/Language/package.xsd">
    <code>it_IT_</code>
    <vendor>[vendorname]</vendor>
    <package>[packagename]</package>
    <sort_order>100</sort_order>
    <use vendor="kkrieger" package="it_it" />
</language>
```

## Help to maintain this language pack

Feel free to create [a issue](https://github.com/kkrieger85/magento2_italian_language_pack/issues) or pull request. 

Please consider, that I will only accept translations wich will be best for a default store translation. 

If a translation just fits to your project, please extend this language pack as described 
above.
