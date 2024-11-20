# Storefront build configuration for Shopware

This plugin allows building Shopware storefronts without accessing the database,
e.g. during container image builds.

## How it works

This plugin ensures that plugins and theme configuration are loaded from disk,
as outlined in [Shopware Developer Documentation](https://developer.shopware.com/docs/guides/hosting/installation-updates/deployments/build-w-o-db.html).

Additionally, it changes the default location of theme config files from
`files/` to `var/`. The reason for that is that `files/` holds deployment-specific
assets so often an external volume is mounted to this path. This makes its
contents unavailable during builds.

## Installation

`composer require kiwee/shopware-storefront-build-config`

## Contributing

Contributions (issues, pull-requests) are welcome!

Please refer to [CONTRIBUTING](CONTRIBUTING.md) to get started.
