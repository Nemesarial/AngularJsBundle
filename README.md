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

### Add Resource to Assetic Configuration

``` yaml
assetic:
    # ...
    assets:
        # ...
        angular_js:
            inputs:
                - %kernel.root_dir%/../vendor/nemesarial/angularjs-bundle/Nemesarial/AngularJSBundle/Resources/public/js/angular.min.js
            output: js/angular.js
        # ...
```

### Add Javascript Reference to the layout
``` twig
{% block javascripts %}
  {% javascripts '@angular_js' combine=true %}
     <script src="{{ asset_url }}"></script>
  {% endjavascripts %}
{% endblock %}
```