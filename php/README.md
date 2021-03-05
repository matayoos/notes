## Wednesday, March 3, 2021, 6:55:29PM -03 <1614808529>

### PHP My Admin

- sudo ln -s /etc/phpmyadmin/apache.conf /etc/apache2/conf-available/phpmyadmin.conf
- sudo a2enconf phpmyadmin.conf
- sudo service apache2 reload

## Old notes

### How to solve the "sudo" problem on /var/www/ patch:
  - sudo chown -R $USER:$USER /var/www

### How to print a beautiful JSON on screen:

```php
<?php

$api_url = 'https://randomuser.me/api/?results=0';
$json_ugly_data = file_get_contents( $api_url );
$json_pretty_data = json_encode(json_decode( $json_ugly_data ), JSON_PRETTY_PRINT );
// pre tag save the day.
echo '<pre>';
echo $json_pretty_data;
echo '</pre>';

?>

```

If wasn't clear the *pre* tag save the day.

### How to read inside the square brackets in a JSON

Square brackets in JSON works like an array, you must use index number to
acess.

```php
$cart = json_decode( $jsonString, true );
echo $cart["shopperEmail"] . "<br>";
echo $cart["contents"][1]["productName"] . "<br>";
```

or

```php
$cart = json_decode( $jsonString );
echo $cart->shopperEmail . "<br>";
echo $cart->contents[1]->productName . "<br>";
```
### How to concatenate options in a url

Use **&** instead '/';
- php $api_url = 'https: //randomuser.me/api/ ?results=3 **&** inc=gender,name,picture';

*Obs: I put some spaces just to not anchor the link.*

## Web Scraping

> how to run a PHP file in the terminal = php file_name.php

1. Composer (must learn).
1. Symphony (PHP framework)
  - HttpClient (Symphony library)
    - BrowserKit: to fill the forms, click on links and so on.
    - DomCrawler: colect data and elements (also data)
