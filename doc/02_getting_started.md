# Getting started

As said before, php was designed as template engine. If you are not familiar with this concept, you can basicaly embed code in some text (typicaly html).

So this is technicaly hello world in php:

```php
Hello world
```

Every text we write outside of php will be just printed.

To actualy start writing php, we use `<?php ?>`

```php
Anytext 
<?php

// some php code

?>
Any text
```

This can be quite useful, however we wont use it in this tutorial, we will have files with only php. So our patern will look like this:

```php
<?php

// some php code

```

Its quite unusual to have to say "Now I'm using this programming language" however text editors are able to generate it and you get into it.

So let's write actual hello world.

```php
<?php

echo 'Hello world!';

```

Echo basicaly just outputs given value - in this case its string.

## Comments

There are three types of comments in php.

Normal is `//` it ends with new line.


```php
<?php

// this is single line comment
```

Multiline comments can be created using `/**/` and they will be more important later.

```php
<?php

/*
    multi
    line
    

            comment


*/
```

There are also `#` comments which work the same as normal ones.

```php
<?php

# this is also comment

```

However this type is not used mostly because it can be confusing while working with attributes.

