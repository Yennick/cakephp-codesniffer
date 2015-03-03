# Oefenweb Code Sniffer for CakePHP

This code works with [phpcs](https://github.com/squizlabs/PHP_CodeSniffer) and checks code against the coding standards used at Oefenweb.

## Installation

It's generally recommended to install these code sniffs with `composer`:

```sh
composer global require --dev 'cakephp/cakephp-codesniffer=1.*';
~/.composer/vendor/bin/phpcs --config-set installed_paths ~/.composer/vendor/cakephp/cakephp-codesniffer;
```

```json
"require-dev": {
	"oefenweb/cakephp-codesniffer": "*"
},
"repositories": [
	{
		"type": "vcs",
		"url": "https://github.com/Oefenweb/cakephp-codesniffer"
	}
]
```

```sh
composer global update oefenweb/cakephp-codesniffer;
~/.composer/vendor/bin/phpcs --config-set installed_paths ~/.composer/vendor/oefenweb/cakephp-codesniffer;
```

The second command lets `phpcs` know where to find your new sniffs. Ensure that
you do not overwrite any existing `installed_paths` value.

## Usage

When these sniffs are installed with `composer`, ensure that you have
configured the CodeSniffer `installed_paths` setting.

Once `installed_paths` is configured, you can run phpcs using:

```sh
vendor/bin/phpcs --standard=Oefenweb;
```