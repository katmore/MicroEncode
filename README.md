# MicroEncode
micro package for php containing encoding utility libraries
 * [Installation](#)
 * [Encoding data to XML](#)
 * [Encoding data to HTML](#)

## Installation
use composer to add **MicroEncode** to your PHP project:
```
composer require katmore/micro-encode
```

## Usage - XmlEncoder
Example encoding an object to XML:
```php
<?php
use MicroEncode\XmlEncoder;
require __DIR__.'/vendor/autoload.php';

$myData = [
   'my'=>'data'
];

echo (new XmlEncoder($myData));
```
The above code should output the following XML:
```html
<?xml version="1.0" encoding="UTF-8"?>
<fx:data fx:created="2018-05-30T15:32:18-07:00" fx:md5="37a6259cc0c1dae299a7866489dff0bd" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xs="http://www.w3.org/2001/XMLSchema" xmlns:extxs="https://github.com/katmore/flat/wiki/xmlns-extxs" fx:flat-xml-ver="0.2" xmlns:fx="https://github.com/katmore/flat/wiki/xmlns" xmlns="https://github.com/katmore/flat/wiki/xmlns-object" xsi:type="extxs:Hashmap">
   <my xsi:type="xs:string">data</my>
</fx:data>
```

## Usage - HtmlEncoder
Example encoding an object to HTML:
```php
<?php
use MicroEncode\HtmlEncoder;
require __DIR__.'/vendor/autoload.php';

$myData = [
   'my'=>'data'
];

echo (new HtmlEncoder($myData));
```
The above code should output the following HTML:
```html
<ul data-type="array">
   <li data-index="0" data-key="my" data-role="item"><span data-role="item-key">my</span>:&nbsp;<span data-role="item-value" data-type="string">data</span></li><!--/data-item: (my)-->
</ul>
```

## Legal
### Copyright
MicroEncode - https://github.com/katmore/micro-encode

Copyright (c) 2012-2018 Doug Bird. All Rights Reserved.

### License
MicroEncode is copyrighted free software.
You may redistribute and modify it under either the terms and conditions of the
"The MIT License (MIT)"; or the terms and conditions of the "GPL v3 License".
See [LICENSE](https://github.com/katmore/micro-encode/blob/master/LICENSE) and [GPLv3](https://github.com/katmore/micro-encode/blob/master/GPLv3).
