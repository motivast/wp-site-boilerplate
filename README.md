# WP Site Boilerplate
WP Site Boilerplate a starter project for sites using WordPress based on modern development tools.

Go to [get started](#user-content-get-started) section to see how work with WP Site Boilerplate.

## Features
- Dependency management using composer
- Clean project structure

## Get started
Clone WP Site Boilerplate from GitHub

```git clone git@github.com:motivast/wp-site-boilerplate.git mysite```

Go into directory

```cd mysite```

Copy dotenv and fill with your properties

```cp .env.example .env```

Install dependencies and download WordPress

```composer install```

Install theme from WordPress theme directory

```composer require wpackagist-theme/twentyseventeen```

Generate config and install WordPress using .env variables with one command. If database do not exist this task will try to create it. Before executing make sure your database user provided in .env file can create database or create database by yourself.

```./vendor/bin/phing wp:init```

Your `wp-config.php` file will be generated in current directory. Open it and add this configuration.

```
define('WP_HOME', 'http://example.com');
define('WP_SITEURL',  WP_HOME . '/wordpress/');
define('WP_CONTENT_DIR', realpath( dirname( __FILE__ ) . '/content' ));
define('WP_CONTENT_URL', WP_HOME . '/content');
```

That's all you can start working with your WordPress!


## Project structure
```
├── content       // Themes, plugins, uploads etc. directory
|   ├── themes
|   ├── plugins
|   └── uploads
├── wordpress     // WordPress directory
├── vendor        // Dependencies directory
├── .env          // Dotenv file with project variables
├── build.xml     // Task manager file
├── composer.json // Dependency management file
├── index.php     // Default WordPress index.php file pointed to wordpress directory
```

## Contribute
I’m really excited that you are interested in contributing to WP Site Boilerplate. Do not hesitate to make pull request.

Thank you to all the people who already contributed to WP Site Boilerplate!

## License
The project is licensed under the [GNU GPLv2 (or later)](https://github.com/motivast/motiforms/blob/master/LICENSE).

Copyright (c) 2017-present, Motivast
