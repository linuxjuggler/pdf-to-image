# Convert a pdf to an image

[![Latest Version on Packagist](https://img.shields.io/packagist/v/spatie/pdf-to-image.svg?style=flat-square)](https://packagist.org/packages/spatie/pdf-to-image)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)
[![Build Status](https://img.shields.io/travis/spatie/pdf-to-image/master.svg?style=flat-square)](https://travis-ci.org/spatie/pdf-to-image)
[![SensioLabsInsight](https://img.shields.io/sensiolabs/i/xxxxxxxxx.svg?style=flat-square)](https://insight.sensiolabs.com/projects/xxxxxxxxx)
[![Quality Score](https://img.shields.io/scrutinizer/g/spatie/pdf-to-image.svg?style=flat-square)](https://scrutinizer-ci.com/g/spatie/pdf-to-image)
[![Total Downloads](https://img.shields.io/packagist/dt/spatie/pdf-to-image.svg?style=flat-square)](https://packagist.org/packages/spatie/pdf-to-image)

This package provides an easy to work with class to convert pdf's to images.

## Requirements

You should have Imagick installed. On Ubuntu you can install it by issuing this command
```bash
sudo apt-get install imagemagick php5-imagick
``

## Install

The package can be installed via composer:
``` bash
$ composer require spatie/pdf-to-image
```

## Usage

Converting a pdf to an image is easy!

```php
$pdf = new Spatie\PdfToImage\Pdf($pathToPdf);
$pdf->saveImage($pathToWhereImageShouldBeStored);
```

If the path you pass to `saveImage` has the extensions  `jpg`, `jpeg`, or `png` the image will be saved in that format.
Otherwise the output will be a jpg.

##Other methods
You can get the number of pages in the pdf:
```php
$pdf->getPageCount() //returns an int
```

By default the first page of the pdf will be rendered. If you want to render another page you can do so:
```php
$pdf->setPage(2)
    ->saveImage($pathToWhereImageShouldBeStored) //saves the second page
```

You can override the output format:
```php
$pdf->setOutputFormat('png')
    ->saveImage($pathToWhereImageShouldBeStored) //the output wil be a png, no matter what
```

## Change log

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## Security

If you discover any security related issues, please email freek@spatie.be instead of using the issue tracker.

## Credits

- [Freek Van der Herten](https://github.com/spatie)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
