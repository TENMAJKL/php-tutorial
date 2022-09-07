# Operators

## Numeric

You have regular math operators:

```php

echo 1 + 1; // 2

echo 2 - 1; // 1

echo 2 * 3; // 6

echo 4 / 2; // 2

echo 3 % 2; // 1
```

Where `%` is modulo operator. It basicaly returns rest from whole number division

Standart is to put spaces between them.

If we provide integer/float on each side it works fine. If we use string it will try to convert it into int/float, so

```php
<?php

echo '1' + 1;

// or

echo '1' + '1';

```

will work the same as with integers. If you provide string that is not numeric it will throw warning.

```php
<?php

echo 'foo ' + ' bar';
```

You can also change priority using braces:

```php
<?php

echo (1 + 1) * 3;
```
## String

But what if I want to actualy connect two strings? For that there is `.` operator.

```php
<?php

echo 'foo '.'bar';

```

unlike numeric operators, this one does not use spaces.

If we add other type it will convert them to string.

```php
<?php

echo 'foo '.(1)
```

We had to use () because `.1` is valid float.
