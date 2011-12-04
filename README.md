Heroku buildpack: Opa
=========================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpack) for [Opa](http://www.opalang.org) apps.

Usage
-----

Example usage:

    $ ls
    Procfile  package.json  web.js

    $ heroku create --stack cedar --buildpack http://github.com/markpundsack/heroku-buildpack-opa.git

    $ git push heroku master
    ...
    -----> Heroku receiving push
    -----> Fetching custom buildpack
    -----> Opa app detected
    -----> Vendoring opa 1.0.687

The buildpack will detect your app as Opa if it has any `*.opa` files in the root. It will vendor a version of the Opa tools into your slug and compile the .opa files into an executable.
