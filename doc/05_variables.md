# Variables

In php variables use `$` prefix, this is probably relic from perl. But it has some advantages.

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

Variables can be removed using `unset()`:

```php
<?php

$foo = 'bar';

unset($foo);

echo $foo; // error
```
