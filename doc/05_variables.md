# Variables

In php variables use `$` prefix, this is probably relic from perl. But it has some advantages.

Variables should have meaningful names that describe their contant.

To create variable simply use `=`. Don't read this as `equal` but as `assign`:

```php
<?php

$name = 'Majkel';

```

PHP Is weakly typed so no type declaration is required.

To work with variable simply use its name:

```php
<?php

$name = 'Majkel';

echo 'Hello '.$name;

```

## More assign operators

If we have variable with number and want to add 1 we can do it like this:

```php
<?php

$number = 0;

$number = $number + 1;
```

We basicaly take curent value, add 1 and assign this.

Note that 

```php
<?php

$number = 0;

$number + 1;
```

won't work, because this will only return 1, but not assign it.

To make it simpler there is `+=` which simplifies the process:

```php
<?php

$number = 0;

$number += 1;
```

Which works with other operators (`+-*/%.`).

And if we add only 1, we can use `++` instead:

```php
<?php

$number = 0;

$number++;
```

Which also works with `--`.

Note that we don't use spaces.

## String interpolation

And here comes the advantage of dollar. In `""` we can use variables directly and clean the notation a bit:

```php
<?php

$name = 'Majkel';

echo "Hello $name";

```

However better is 

```php
<?php

$name = 'Majkel';

echo "Hello {$name}";

```

because you can call functions etc.

## Removing

Variables can be removed using `unset()`:

```php
<?php

$foo = 'bar';

unset($foo);

echo $foo; // error
```
