# Guzzle Service Description Loader

A stand-alone Service Description loader for Guzzle 5.x.

## Installation

If you are using Composer, and you should, just reference the plugin in your composer.json file:

``` sh
composer require "gimler/guzzle-description-loader"
```

## Supported File Formats

* Yaml
* Php
* Json

## Usage

``` php
$configDirectories = array(FIXTURES_PATH);
$this->locator = new FileLocator($configDirectories);
$this->jsonLoader = new JsonLoader($this->locator);

$description = $this->jsonLoader->load($this->locator->locate('description.json'));
```
