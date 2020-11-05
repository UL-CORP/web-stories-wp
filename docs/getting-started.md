# Getting Started

## Requirements

To contribute to this plugin, you need the following tools installed on your computer:

- [PHP](https://www.php.net/) - version 7.2 or higher, preferably installed via [Homebrew](https://brew.sh/)
- [Composer](https://getcomposer.org/) (PHP package manager) - to install PHP dependencies, the minimum version is 1.10.x (warning: 2.x version may raise issues in package installation).
- [Node.js](https://nodejs.org/en/) (current LTS) - to install JavaScript dependencies.
- [WordPress](https://wordpress.org/download/) - to run the actual plugin.
- [Docker Desktop](https://www.docker.com/products/docker-desktop) and [Docker Compose](https://docs.docker.com/compose/install/) - for using the local environment

You should be running a Node version matching the [current active LTS release](https://github.com/nodejs/Release#release-schedule) or newer for this plugin to work correctly. You can check your Node.js version by typing node -v in the Terminal prompt.

If you have an incompatible version of Node in your development environment, you can use [nvm](https://github.com/creationix/nvm) to change node versions on the command line:

```bash
nvm install
```

## Local Environment

Check out the [Local Environment](./local-environment.md) document.

## Development

First of all, you need to make sure that all PHP and JavaScript dependencies are installed:

Install Composer, please use the following command or see [here](https://getcomposer.org/download/), to set Composer to a specific version (i.e. 1.10.16), run:

```bash
composer require composer/composer:~1.10.16
composer self-update 1.10.16
```

Install all the required composer packages, run:

```bash
composer install
```

Install all the required npm packages, run:

```bash
npm install
```

Whether you use the pre-existing local environment or a custom one, any PHP code changes will be directly visible during development.

However, for JavaScript this involves a build process. To watch for any JavaScript file changes and re-build it when needed, you can run the following command:

```bash
npm run dev
```

This way you will get a development build of the JavaScript, which makes debugging easier.

To get a production build, run:

```bash
npm run build:js
```

In order bring the entire project up, we will also need to start the php server, run:

```bash
npm run env:start
```
