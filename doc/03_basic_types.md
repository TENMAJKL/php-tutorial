# Basic types

Php has 4 basic types.

## Int

Int is just number, the types is called `int` and is defined just by writing number.

```php
<?php

echo 1;

echo -1

echo 37;

```

## Float

Another numeric type is float `float`

```php
<?php

echo 1.1;

echo 3.14159265358979323846;

echo -37.37

```

## Bool

`bool` is type that can have 2 values - true or false. Where true is basialy 1 and false 0.

```php
<?php

echo true;

echo false;

```

## Strings

String is just text. There are 3 ways of creating strings and each has its use.

Mostly recommended is `''` which should be used in most situations.

```php
<?php

echo 'Hello world!';

```

Alternative is `""` which is similar but allows string interpolation, which will be covered in next chapters so for now stick with `''`.

```php
<?php

echo "Hello world";

```

And herodoc, which is used for multiline strings

```php
<?php

echo <<<TEXT
    Hello world!
TEXT;

```

where TEXT can be anything. Some editors support html, so if you use HTML it will be highlighted.
