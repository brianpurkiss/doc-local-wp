# Mac instructions

## Required to be installed

* [Homebrew](https://brew.sh/)
* [Laravel Valet](https://laravel.com/docs/5.4/valet)
* [WP CLI](http://wp-cli.org/)


### First time setup

[Tutorial on what needs to be installed the first time you begin to work locally.](https://code.tutsplus.com/tutorials/using-laravel-valet-for-wordpress-development--cms-26519)


# WP CLI Installation instructions

Download WordPress and place it in the previously selected valet directory

Rename wp-config-sample.php to wp-config.php. Edit wp-config.php: Choose a unique database name for the site, set the username to "root" and a blank password.

Navigate to the created WordPress directory and run:
`wp db create`

Install WordPress - choose a local domain, title, username, password, and admin email - or use the web interface to set up the WordPress website. 
`wp core install --url="your_domain.test"  --title="Blog Title" --admin_user="theoverlord" --admin_password="enter_your_password" --admin_email="email@email.com"`

Change permalink structure:
`wp rewrite structure '/%postname%'`


## SSL certificate on a local machine

In Terminal, navigate to the WordPress theme folder. Run `valet secure {sitename}` where "{sitename}" is the name of your directory/site URL, not including the chosen TLD. 

[Official documentation](https://laravel.com/docs/5.7/valet#serving-sites)


## Share a local dev site online

It is possible to share a local dev site through the internet using Laravel Valet. This is useful for testing on smartphones and other operating systems. [The official documentation can be found here.](https://laravel.com/docs/5.7/valet#sharing-sites)

In Terminal, navigate to the WordPress theme folder. Run `valet share` to start sharing. A publically accessible URL will be provided and automatically inserted into your clipboard. It will be something along the lines of: http://d2b5c0b9.ngrok.io

However, all of the stylesheets/images/etc will be broken as they are refer to your local dev URL. So open up wp-config.php and change your site URL temporarily using the following: 

`define('WP_HOME', 'http://{temporary-id}.ngrok.io/');
define('WP_SITEURL', 'http://{temporary-id}.ngrok.io/');`

It's a good idea to simply comment out those two lines of code when you're done so you can turn it on and off as needed throughout the development process. When done, simply press ctrl+c in Terminal to stop the process. 


# [Syncing local with a dev environment.](sync-wp-local-dev.md)

--

### Recommended plugins to install on fresh site

* Theme My Login - Provides a better user experience for the customer
	`wp plugin install 'Theme My Login'`
* Brute Force Login Protection - Increase security
	`wp plugin install 'Brute Force Login Protection'`
* The SEO Framework - Useful SEO Improvement
	`wp plugin install 'The SEO Framework'`
* Wordfence - Free security plugin
	`wp plugin install 'wordfence'`


# Useful links

* [WP CLI Commands](https://developer.wordpress.org/cli/commands/)
