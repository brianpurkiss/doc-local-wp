
# Create a temporary dev site

Useful for testing on mobile devices instead of emulators, on different operating systems, or getting coworkers to test your local environment.


### Requirements

1. A local WordPress install using Laravel Valet.

## How to:

1. Navigate to the WordPress instance folder in Terminal.
2. Use `valet share`
3. Get the `{temporary-id}.ngrok.io` URL provided.
4. Change the WordPress instance site URL in wp-config.

`define('WP_HOME', 'http://{temporary-id}.ngrok.io/');
define('WP_SITEURL', 'http://{temporary-id}.ngrok.io/');`

Use ctrl+c in terminal to stop sharing. 
