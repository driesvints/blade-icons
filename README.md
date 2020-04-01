# Blade Icons

<a href="https://github.com/driesvints/blade-icons/actions"><img src="https://github.com/driesvints/blade-icons/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/driesvints/blade-icons"><img src="https://poser.pugx.org/driesvints/blade-icons/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/driesvints/blade-icons"><img src="https://poser.pugx.org/driesvints/blade-icons/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/driesvints/blade-icons"><img src="https://poser.pugx.org/driesvints/blade-icons/license.svg" alt="License"></a>

A package to easily make use of icons in your Laravel Blade views. 

Heroicons and Zondicons originally made by [Steve Schoger](https://twitter.com/steveschoger) and [Adam Wathan](https://twitter.com/adamwathan).

## List of icons

- [Heroicons](resources/images/heroicons)
- [Zondicons](resources/images/zondicons)

## Requirements

- PHP 7.4 or higher
- Laravel 7.0 or higher

## Installation

```bash
composer require driesvints/blade-icons
```

## Updating

General steps for every update:

- Run `php artisan view:clear`
- If you published the raw icons run `php artisan vendor:publish --tag=blade-icons --force`

When upgrading to a new major version of the library, remember to read [`the upgrade guide`](UPGRADE.md).

## Usage

Icons can be used a self-closing Blade components which will be compiled to SVG icons:

```blade
<x:heroicon-o-adjustments/>
```

You can also pass classes to your icon components:

```blade
<x:heroicon-o-adjustments class="w-6 h-6 text-gray-500"/>
```

And even use inline styles:

```blade
<x:heroicon-o-adjustments style="color: #555"/>
```

The solid icons can be referenced like this:

```blade
<x:heroicon-s-adjustments/>
```

Zondicon icons can be referenced like:

```blade
<x:zondicon-add-outline/>
```

### Raw SVG Icons

If you want to use the raw SVG icons as assets, you can publish them using:

```bash
php artisan vendor:publish --tag=blade-icons --force
```

Then use them in your views like:

```blade
<img src="{{ asset('vendor/blade-icons/heroicons/heroicon-o-adjustments.svg') }}" width="10" height="10"/>
```

And use zondicons like: 

```blade
<img src="{{ asset('vendor/blade-icons/zondicons/zondicon-add-outline.svg') }}" width="10" height="10"/>
```

## Changelog

Check out the [CHANGELOG](CHANGELOG.md) in this repository for all the recent changes.

## License

Blade Heroicons is open-sourced software licensed under [the MIT license](LICENSE.md).
