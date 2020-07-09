# What is Leafcutter?

Leafcutter is a flat-file based CMS, written in PHP, and designed to run online rather than be used to generate static sites like, for example, Jekyll. This means your workflow for updating content on your site will be editing raw Markdown files in a content directory, which Leafcutter will transform on the fly into a fully functional website.

# Getting started

The easiest way to get started with Leafcutter is by [downloading](https://github.com/leafcutter-cms/site-template/archive/main.zip) or [using](https://github.com/leafcutter-cms/site-template/generate) the [site template](https://github.com/leafcutter-cms/site-template). This will establish a good starting point from which you can have a basic but functioning site.

The template is designed to keep everything out of the web root, so when planning to deploy it, keep in mind that it is expecting `web/` to be the web root.

Once you have your site template directory on your computer (either by unzipping the download or cloning a copy you made using Github's template repository feature), you will need to run composer update to install all the dependencies of the project, and do a little basic configuration.

## Composer update

First, run `composer update` from the root of the project. This will install appropriate versions of the actual Leafcutter code and all its dependencies. This is also how you will update your copy of Leafcutter in the future.

## Configuration

All of the site's configuration files are kept in the `config/` directory. Everything here is read (in alphabetical order, on most systems) and merged into the system config. One special file is `config/env.yaml`. This file is ignored by Git and can be used to set environment-specific settings, such as using a different URL or disabling caching in a development copy.

## Permissions

For Leafcutter to function you also need to make sure that the web server can write to the following directories:

* `cache/`
* `logs/`
* `web/assets/`
