# Sample CakePHP App Using Multiple templates path

This is a sample application that uses two folders for templates.
The default one `./templates` and one to override in the
local installation `./templates_local`.

#Use case
The repository has the templates folder and the installation
has the additional folder templates_local to override the
templates for pages http://localhost/ and http://localhost/pages/hello

# Steps

- Added a new item template path at config 'App.paths' in [./config/app.php]
 of the config 'App.paths.templates'
```
    'paths' => [
        'plugins' => [ROOT . DS . 'plugins' . DS],
        'templates' => [
            ROOT . DS . 'templates_local' . DS,
            ROOT . DS . 'templates' . DS
        ],
        'locales' => [RESOURCES . 'locales' . DS],
    ],
```
- Created the template file [templates_local/Pages/home.php](./templates_local/Pages/home.php)
- Created the template file [templates_local/Pages/hello.php](./templates_local/Pages/hello.php)

You could use this approach to use a local path for each
client installation, environment var, or domain.
