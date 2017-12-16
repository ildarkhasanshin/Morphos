# Morphos
A morphological solution for Russian and English language written completely in PHP.

[![Composer package](http://composer.network/badge/wapmorgan/morphos)](https://packagist.org/packages/wapmorgan/morphos)
[![Latest Stable Version](https://poser.pugx.org/wapmorgan/morphos/v/stable)](https://packagist.org/packages/wapmorgan/morphos)
[![License](https://poser.pugx.org/wapmorgan/morphos/license)](https://packagist.org/packages/wapmorgan/morphos)
[![Total Downloads](https://poser.pugx.org/wapmorgan/morphos/downloads)](https://packagist.org/packages/wapmorgan/morphos)
[![Latest Unstable Version](https://poser.pugx.org/wapmorgan/morphos/v/unstable)](https://packagist.org/packages/wapmorgan/morphos)

Tests & Quality: [![Build Status](https://travis-ci.org/wapmorgan/Morphos.svg)](https://travis-ci.org/wapmorgan/Morphos)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/wapmorgan/Morphos/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/wapmorgan/Morphos/?branch=master)

## Features
- [✓] Inflection of Personal names (Фамилия, Имя, Отчество) (Russian)
- [✓] Inflection of Geographical names (Страны/Города) (Russian)
- [✓] Declension/Pluralization of nouns and adjectives (Russian, English)
- [✓] Generation numerals of numbers (количественные и порядковые) (Russian, English)
- [✓] Spelling out amounts of money (Russian)
- [✓] Spelling out time units and intervals (Russian, English)

## Table of contents

1. Installation
2. Quick start
3. Library documentation
4. Contributing

## Installation

* Download library through composer:
```
composer require wapmorgan/morphos
```

- Adapter for Laravel (Blade): [wapmorgan/morphos-blade](https://github.com/wapmorgan/Morphos-Blade)
- Adapter for Symfony (Twig): [wapmorgan/morphos-twig](https://github.com/wapmorgan/Morphos-Twig)
- Adapter for Yii2 (_as part of extension_): [wapmorgan/yii2-inflection](https://github.com/wapmorgan/yii2-inflection)

## Quick Start

#### Russian
```php
// Inflect russian names:
morphos\Russian\inflectName('Иванов Петр', 'родительный') => 'Иванова Петра'

// Inflect geographical names:
morphos\Russian\GeographicalNamesInflection::getCase('Москва', 'родительный') => 'Москвы'

// Pluralize russian nouns:
morphos\Russian\pluralize(10, 'дом') => '10 домов'

// Generate russian cardinal numerals:
morphos\Russian\CardinalNumeralGenerator::getCase(567, 'именительный') => 'пятьсот шестьдесят семь'

// Generate russian ordinal numerals:
morphos\Russian\OrdinalNumeralGenerator::getCase(961, 'именительный') => 'девятьсот шестьдесят первый'

// other functions described in README-ru.md
```

#### English
```php
// Pluralize english nouns:
morphos\English\pluralize(10, 'house') => '10 houses'

// Generate english cardinal numerals:
morphos\English\CardinalNumeralGenerator::generate(567) => 'five hundred sixty-seven'

// Generate english ordinal numerals:
morphos\English\OrdinalNumeralGenerator::generate(961) => 'nine hundred sixty-first'
```

# Library documentation

- [Русская морфология](README-ru.md) в файле README-ru.md
- [English morphology](README-en.md) in file README-en.md

# Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for this.
