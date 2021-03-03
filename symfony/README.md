## Wednesday, March 3, 2021, 2:50:41PM -03 <1614793841>

- This doesn't work for me

```bash
$ composer require server
```

- But this does work

```bash
$ composer require symfony/web-server-bundle --dev ^4.4.2
```

*"Using the WebserverBundle is deprecated since Symfony 4.4."* Oh my...

![Symfony server](https://symfony.com/doc/4.4/setup/symfony_server.html) new
way.

## Wednesday, March 3, 2021, 9:34:21AM -03 <1614774861>

![Symfony taugh me how do I execute(?) a script](imgs/symfonyCLIScript.png)

## Wednesday, March 3, 2021, 8:15:48AM -03 <1614770148>

### Free Code Camp

This doesn't work for me:

```php
    public function index(): Response
    {
        return new Response(content: '<h1>Welcome, Matayoos!</h1>');
    }
```
This could be a PHP Storm feature.

But this does:

```php
    public function index(): Response
    {
        $response = new Response(
            '<h1>Welcome, Matayoos!</h1>',
            Response::HTTP_OK,
            ['content-type' => 'text/html']
        );
        return $response;
    }
```
