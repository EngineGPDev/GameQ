# GameQ Version 3
[![CI](https://github.com/EngineGPDev/GameQ/actions/workflows/Tests.yml/badge.svg)](https://github.com/EngineGPDev/GameQ/actions/workflows/Tests.yml)
[![License](https://img.shields.io/badge/license-LGPL-blue.svg?style=flat)](https://packagist.org/packages/enginegp/gameq)

GameQ is a PHP library that allows you to query multiple types of multiplayer game & voice servers at the same time.

## Requirements
* PHP 5.6.40+ - [Tested](https://github.com/EngineGPDev/GameQ/actions/workflows/Tests.yml) in PHP 5.6, 7.0, 7.1, 7.2, 7.3, 7.4, 8.0, 8.1, 8.2, 8.3 & 8.4-dev
* [Bzip2](http://www.php.net/manual/en/book.bzip2.php) - Used for A2S Compressed responses

## Installation
#### [Composer](https://getcomposer.org/)
This method assumes you already have composer [installed](https://getcomposer.org/doc/00-intro.md) and working properly. Add `enginegp/gameq` as a requirement to composer.json by using `composer require enginegp/gameq:~3.1` or by manually adding the following to the *composer.json* file in the **require** section:

```javascript
"enginegp/gameq": "~3.1"
```

Update your packages with `composer update` or install with `composer install`.

#### Standalone Library
Download the [latest version](https://github.com/EngineGPDev/GameQ/releases) of the library and unpack it into your project.  Add the following to your bootstrap file:
```php
require_once('/path/to/src/GameQ/Autoloader.php');
```
The Autoloader.php file provides the same auto loading functionality as the Composer install.

## Example
```php
$GameQ = new \GameQ\GameQ();
$GameQ->addServer([
    'type' => 'css',
    'host' => '127.0.0.1:27015',
]);
$results = $GameQ->process();
```
Need more?  See [Examples](https://github.com/Austinb/GameQ/wiki/Examples-v3).

## Contributing 
 
Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## License
See [LICENSE](LICENSE.lgpl) for more information
