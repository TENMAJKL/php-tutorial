# Conditions

We may want to do different actions depending on some conditions (eg. comparing result). For that there is control structure `if` This structure takes expression, evaluates it and executes block underneeth if its true:

```php
if (true) {
    // this will be executed everytime
}

$a = 10;

if ($a < 20) {
    // the $a < 20 expression in this case evaluates to true, so this block will execute
    echo 'number is smaller than 20.';
}

```

If we want to do something in case the expression is false, we can se else:

```php

$a = 37;

if ($a < 20) {
    // this wont execute since the expression is false
    echo 'number is smaller than 20.';
} else {
    // so this will evaluate instead
    echo 'number is bigger than 20!';
}

```

If the block contains only single line, the brackets are actually redundant, but its better to use them, not only because its standart but because if you e.g. add new statement and you forget to add the brackets it may lead to security vulnerabilities.

### Ternary operator

Let's say we have variable `$a` which contains some number. If the number is smaller than 20, we want to set variable `$b` to `'foo'`, otherwise we want `'bar'`. The basic aproach is something like

```php

if ($a < 20) {
    $b = 'foo';
} else {
    $b = 'bar';
}

```

 However this produces boilerplate code. This is basicaly repetetive code. Better solution is to use ternary operator. That is basicaly single-line if. It is single expression that has 3 inner expressions. The first evaluates, if its true, it evaluates the second, otherwise the third. So return value of evaluated expression is return value of this operator. This sounds way too abstract, so lets rewrite the above example.

```php
$b = $a < 20 ? 'foo' : 'bar';
```

And because it takes expressions, something like this is not possible:

```php
$b = $a < 20 ? echo 'foo' : 'bar';
```

### Multiple arms

Ifs can also have multiple arms. This means that we can have multiple conditions.

```php

if ($a < 20) {
    echo 'foo';
} else if ($a > 20) {
    echo 'bar';
} else {
    echo 'baz';
}

```

## Switch

Let's say we have variable `$name` with name. We want to print something depending on the name. First aproach is obviously if:

```php

if ($name === 'Majkel') {
    echo 'neovim';
} else if ($name === 'CoolFido') {
    echo 'vscode';
} else if ($name === 'yamiteru') {
    echo 'webstorm';
} else {
    echo 'unknown user';
}
```

As you can see there is lot of boilerplate and adding new names is painful. Lets fix it with switch. Swith is similar to if, however it by default compares.

```php

switch ($name) {
    case 'Majkel':
        echo 'neovim';
        break;
    case 'CoolFido':
        echo 'vscode';
        break;
    case 'yamiteru':
        echo 'webstorm';
        break;
    default:
        echo 'unknown user';
}
```

However this still produces some boilerplate - we repeat the same patern all the time. So lets introduce match

## Match

Match is similar to ternary operator but for switch, the above example will look like this:

```php

echo match ($name) {
    'Majkel' => 'neovim',
    'CoolFido' => 'vscode',
    'yamiteru' => 'webstorm',
    default => 'unknown user'
};

```
