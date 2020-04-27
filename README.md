Scrypt
---
**Pure PHP-implementation without any extensions**

#### Install:
```php
composer require cast/scrypt
```

#### Usage:
```php
<?php

use function Cast\Crypto\Scrypt\scrypt;

$expected = "77d6576238657b203b19ca42c18a0497f16b4844e3074ae8dfdffa3fede21442fcd0069ded0948f8326a753a0fc81f17e8d3e0fb2e0d3628cf35e20c38d18906";
// strlen($expected) == 128
$actual = bin2hex(scrypt("", "", 16, 1, 1, 64));
// strlen($actual) == 128
```

Based on https://github.com/cmpscabral/cryptobits/tree/master/php/scrypt.