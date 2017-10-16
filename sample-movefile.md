# Sample WordMove move file

A sample Movefile for [WordMove](http://welaika.github.io/wordmove/).

`local:
  vhost: "http://boilerplate.dev"
  wordpress_path: "/home/brianpurkiss/Documents/Sites/boilerplate" # use an absolute path here

  database:
    name: "database_name"
    user: "root"
    password: "password"
    host: "127.0.0.1"

production:
  vhost: "http://example.com"
  wordpress_path: "/public_html" # use an absolute path here, don't use a "www" shortcut path

  database:
    name: "database_name"
    user: "user"
    password: "password"
    host: "host"
    # port: "3308" # Use just in case you have exotic server config

  ssh:
    host: "host"
    user: "user"
    password: "password" # password is optional, will use public keys if available.
    port: 22 # Port is optional
    rsync_options: "--verbose" # Additional rsync options, optional
    gateway: # Gateway is optional
      host: "host"
      user: "user"
      password: "password" # password is optional, will use public keys if available.

  exclude:
    - ".git/"
    - ".gitignore"
    - ".sass-cache/"
    - "bin/"
    - "tmp/*"
    - "Gemfile*"
    - "Movefile"
    - "wp-config.php"
    - "wp-content/*.sql"
`
