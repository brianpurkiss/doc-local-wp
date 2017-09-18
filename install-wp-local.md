# Mac instructions

## Required to be installed

* [Homebrew](https://brew.sh/)
* [Laravel Valet](https://laravel.com/docs/5.4/valet)
* [WP CLI](http://wp-cli.org/)


# First time setup

**todo: first time setup instructions**
(start valet in desired directory)


# Mac Installation instructions

Download WordPress and place it in the previously selected valet directory

Rename wp-config-sample.php to wp-config.php. Edit wp-config.php: Choose a unique database name for the site, set the username to "root" and a blank password.

Navigate to the created WordPress directory and run:
`wp db create`

Install WordPress - choose a local domain, title, username, password, and admin email
`wp core install --url="your_domain.dev"  --title="Blog Title" --admin_user="theoverlord" --admin_password="enter_your_password" --admin_email="email@email.com"`

Change permalink structure:
`wp rewrite structure '/%postname%'`


# Plugins to install on fresh site

* Theme My Login - Provides a better user experience for the customer
	`wp plugin install 'Theme My Login'`
* Brute Force Login Protection - Increase security
	`wp plugin install 'Brute Force Login Protection'`
* Yoast SEO - Useful SEO Improvement
	`wp plugin install 'Wordpress SEO'`
* WP Sync DB - for syncing local and dev
	`wp plugin install 'https://github.com/wp-sync-db/wp-sync-db/archive/master.zip'`




# Relevent links

https://developer.wordpress.org/cli/commands/
