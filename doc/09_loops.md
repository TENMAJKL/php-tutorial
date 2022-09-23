# Loops

Simpelest loop we can use is while loop. This loop basicaly loops while expresion is true.

```php

while (expression) {
    // something
}
```

The expression will evaluate, if its true, it will execute its block and to it again. If the expression is false, it will stop.

```php

<?php

while (true) {
    echo 'Hello! ';
}
```

So this is basicaly infinite loop - the expression allways returns true.

Let's print numbers from 1 to 100:

```php

<?php

$counter = 1;

while ($counter <= 100) {
    echo $counter."\n";
    $counter++;
}

```

Each time it t checks the counter, if its false it ends, otherwise prints and adds.

## For loop

For loop was intended for looping in arrays. It has 3 commands. The first executes only once (we use it for initialization of counter). The second is condition and third is statement that executes after the codeblock (mostly incrementing).

```php
<?php

$array = ['foo', 'bar', 'baz'];
$size = 3;

for ($i = 0; $i < $size; $i++) {
    echo $array[$i].' ';
}
```

## Foreach

However foreach is much better option for iterating in array:

```php

$array = ['foo', 'bar', 'baz'];


foreach ($array as $item) {
    echo $item.' ';
}
```

It can also destruct the array, which means we can get key and value:

```php

$array = ['foo', 'bar', 'baz'];


foreach ($array as $key => $item) {
    echo $key.': '$item.', ';
}
```

We just use the same notation as for declaring arrays.
