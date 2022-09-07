# Comparing

In php we can compare 2 values, they can be anything from variables to values. There are several operators and everyone returns bool.

```php
<?php

$foo = 10;

echo $foo < 20;
echo $foo > 20;
echo $foo <= 10;
echo $foo >= 5;

echo $foo == 5; // false
echo $foo == '10'; // true
echo $foo == 10; // true
echo $foo === '10'; // false
echo $foo === 10; // true

```

`==` checks if values are same, so if we have 10 and '10' it returns true. But `===` matches values and types, so if we use it on 10 and '10' it returns false as they have different type.

## Negation

There are not-equal operators:

```php
<?php

$foo = 10;

echo $foo != 5; // true
echo $foo !== '10'; // true

```

They work the same except they return oposite boolean value (true => false, false => true)

We can also negate bool value using `!`:

```php
<?php

echo !(false); // true
```

and the value can be expression which will evaluate:

```php
<?php

echo !(1 == 1); // false;

```
