NemAngularJsBundle - AngularJs as a Symfony 2 bundle
====================================================

### Current Version

AngularJs **Ver 1.0.7**

## Installation

### Add bundle to your composer.json file

``` js
// composer.json
{
    "require": {
        // ...
        "nemesarial/angularjs-bundle": "dev-master"
    }
}
```

### Add bundle to your application kernel
``` php
// app/AppKernel.php

public function registerBundles()
{
    $bundles = array(
        // ...
        new Nemesarial\AngularJsBundle\NemAngularJsBundle(),
        // ...
    );
}
```

### Install the bundle using Composer
``` bash
$ php composer.phar update nemesarial/angularjs-bundle
```