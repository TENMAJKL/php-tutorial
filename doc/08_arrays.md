# Arrays

Array is basicaly list that contains some data. To create use this syntax:

```php
<?php

$numbers = [1, 2, 3, 4];

```

Each element has its sytnax, by default its position starting from 0. To get value we have to `index it`:

```php
<?php

$numbers = [1, 2, 3, 4];

echo $numbers[0]; // 1;

$numbers[3] = 5;

print_r($numbers);

```

Arrays can't be printed using `echo`. To actually print them we have to use function `print_r` which is debugging function. Its not recommended to use it for actualy printing data in real apps.

We can also push to the array using empty brackets:

```php

<?php

$numbers = [];

$numbers[] = 1;
$numbers[] = 2;

print_r($numbers);

```

We can also use our own index to create asociative arrays:

```php
<?php

$editors = [
    'Majkel' => 'neovim',
    'CoolFido' => 'vscode',
    'yamiteru' => 'webstorm',
];

print_r($editors);

```

And index it using given key:

```php

$editors = [
    'Majkel' => 'neovim',
    'CoolFido' => 'vscode',
    'yamiteru' => 'webstorm',
];

echo $editors['yamiteru']; // webstorm

$editors['yamiteru'] = 'neovim'

print_r($editors);

```

Arrays can contain multiple types.
