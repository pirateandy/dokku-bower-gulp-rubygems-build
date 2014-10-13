dokku-bower-gulp-rubygems-build
===============================

Based on [ezynda3/dokku-bower-gulp-build](https://github.com/ezynda3/dokku-bower-gulp-build).
With some added logic for dependency checks and the ability to require rubygems (eg: Sass) before performing the `gulp build`.

This plugin will:

1. Check for `Gemfile`
  - *if found:* install [Bundler](http://bundler.io/), then run `bundle install`.
2. Check for `bower.json`
  - *if found:* ensure that bower is installed, then run `bower install --allow-root`.
3. Check for `gulpfile.js`
  - *if found:* ensure that gulp is installed, then run `gulp build`.


## Install

On your dokku server run:
```sh
cd /var/lib/dokku/plugins
git clone https://github.com/knksmith57/dokku-bower-gulp-rubygems-build bower-gulp-rubygems-build
```
