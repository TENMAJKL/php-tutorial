# Functions

Function is basicaly reusable code. Best explanation is by example:

```php
<?php

function add($first, $second)
{
    return $first + $second;
}

echo add(1, 2); // 3
```

Function is block of code that we can execute anywhere in our app. It can't use outer variables, so we must `pass them as arguments`. Argument is basicaly variable. We provide its value when calling. So if we call function `add` we provide arguments, in this case 1 and 2. The function is then callen with theese values stored in provided variables. But how do we return values back? For this there is `return` statement, expression of this statement evaluates and its returned from the function. So in this case we simply added 2 numbers and returned its addition.

But here comes problem. Our arguments can be any type. And we need only integers. And in some more complicated functions, we need to specify what type we need. And we can do that.

```php
<?php

function add(int $first, int $second)
{
    return $first + $second;
}

echo add(1, 2); // 3
```

If we use autocompletition we will see what type it expects and if we provide wrong type, we will get meaningful error.

To make things more clear its better to provide return type. You will see it in autocompletition and it will throw error if you will use some unsuported operations.

```php
<?php

function add(int $first, int $second): int
{
    return $first + $second;
}

echo add(1, 2); // 3
```

Let's see some better example:

Imagine we implement range program. It fills array in variable `$array` with numbers from 1 to `$number`:

```php
<?php

$array = [];

for ($curent = 1; $curent <= $number; $curent ++) {
    $array[] = $curent;
}
```

This works, but what if we need this range somewhere in our code? Or what if we need to do it twice? This will lead to completely unreadable code. So the solution is to write function. In this case, it will take number and return the array:

```php
<?php

function my_range(int $number): array
{
    $array = [];

    for ($curent = 1; $curent <= $number; $curent ++) {
        $array[] = $curent;
    }
    return $array;
}
```

Now, if we anywhere in our code call `my_range(number)` we get array from numbers 1 to number.

## Default functions

Php has many default functions which will cover most of your needs.
