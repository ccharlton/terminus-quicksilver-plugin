# Terminus Quicksilver Plugin

A plugin for Terminus-CLI that allows for installation of Quicksilver webhooks from the Quicksilver examples, or a personal collection.

### Installation
```
mkdir -p ~/terminus/plugins
cd ~/terminus/plugins
composer require pantheon-systems/terminus-quicksilver-plugin
```

### Configuration
This plugin will allow the user to quickly install Quicksilver webhooks pulled from either the Pantheon Quicksilver examples project, or from a personal collection of commonly-used webhooks.

To provide your own repository containing example webhooks that can be installed with the `terminus quicksilver install` command, set up a configuration file in your home directory, as shown below:
```
mkdir ~/.quicksilver
cp example-user-config.yml ~/.quicksilver/quicksilver.yml
```
See contents of this file for customization instructions.

### Init pantheon.yml File
```
cd /path/to/local/pantheon/site
terminus quicksilver init
```
Writes a simple pantheon.yml file to get you started with Quicksilver.

### Install a Quicksilver Webhook
```
cd /path/to/local/pantheon/site
terminus quicksilver install debug
```
Installs one of the example projects from quicksilver-examples, and updates the site's pantheon.yml file.  Searches for a project whose name contains the provided string; in the example above, the debugging_example will be installed.

Once the sample has been installed, read its README file and customize the pantheon.yml file as needed.

### Install a Predefined Set of Quicksilver Webhooks
```
cd /path/to/local/pantheon/site
terminus quicksilver profile development
```
