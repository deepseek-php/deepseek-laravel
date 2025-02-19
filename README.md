# Deepseek Laravel

Laravel wrapper for **[Deepseek PHP client](https://github.com/deepseek-php/deepseek-php-client)** to seamless [deepseek AI](https://www.deepseek.com) API integration with Laravel applications.

## Table of Contents

- [Installation](#installation)
  - [Publishing Configuration File](#publishing-configuration-file)
- [Usage](#usage)
  - [Basic Usage](#basic-usage)
  - [Advanced Usage](#advanced-usage)
- [Testing](#testing)
- [Contributors](#contributors-)
- [Changelog](#changelog)
- [Security](#security)
- [License](#license)

## Installation

> **Requires [PHP 8.1+](https://php.net/releases/)**

You can install the package via composer:

```bash
composer require deepseek-php/deepseek-laravel
```

### Publishing Configuration File

```bash
php artisan vendor:publish --tag=deepseek
```
then add token to `.env` file
```php
DEEPSEEK_API_KEY="your_api_key"
```

## Usage

### Basic Usage

```php
use DeepSeekClient;

$deepseek = app(DeepSeekClient::class);
$response = $deepseek->query('Hello deepseek, I am Laravel Framework , how are you Today ^_^ ?')->run();
print_r("deepseek API response : " . $response);
```

**Note**: In easy mode, it will take defaults for all configs [Check Default Values](https://github.com/deepseek-php/deepseek-php-client/blob/master/src/Enums/Configs/DefaultConfigs.php)

### Advanced Usage

```php
use DeepSeekClient;

$deepseek = app(DeepSeekClient::class);

// Another way, with customization
$response = $deepseek
    ->query('Hello deepseek, how are you ?', 'system')
    ->query('Hello deepseek, my name is PHP ', 'user')
    ->withModel("deepseek-chat")
    ->setTemperature(1.5)
    ->run();

print_r("deepseek API response : " . $response);
```

## Testing

Tests will come soon

## Contributors ✨

Thanks to these wonderful people for contributing to this project! 💖

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/omaralalwi">
        <img src="https://avatars.githubusercontent.com/u/25439498?v=4" width="70px;" alt="Omar AlAlwi"/>
        <br />
        <sub><b>Omar AlAlwi</b></sub>
      </a>
      <br />
      🏆 Creator
    </td>
      <td align="center">
      <a href="https://github.com/A909M">
        <img src="https://avatars.githubusercontent.com/u/119125167?v=4" width="70px;" alt="Asim Al-Wasai"/>
        <br />
        <sub><b> Assem Alwaseai </b></sub>
      </a>
      <br />
      💻 Contributor
    </td>
    <!-- Contributors -->
    </td>
      <td align="center">
      <a href="https://github.com/200-0K">
        <img src="https://avatars.githubusercontent.com/u/38166228?v=4" width="70px;" alt="Faisal"/>
        <br />
        <sub><b> Faisal </b></sub>
      </a>
      <br />
      💻 Contributor
    </td>
    <!-- Contributors -->
  </tr>
</table>

Want to contribute? Check out the [contributing guidelines](./CONTRIBUTING.md) and submit a pull request! 🚀

### Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

---
<div>

# 🐘✨ **DeepSeek PHP Community** ✨🐘

Click the button bellow or [join here](https://t.me/deepseek_php_community) to be part of our growing community!

[![Join Telegram](https://img.shields.io/badge/Join-Telegram-blue?style=for-the-badge&logo=telegram)](https://t.me/deepseek_php_community)


### **Channel Structure** 🏗️
- 🗨️ **General** - Daily chatter
- 💡 **Ideas & Suggestions** - Shape the community's future
- 📢 **Announcements & News** - Official updates & news
- 🚀 **Releases & Updates** - Version tracking & migration support
- 🐞 **Issues & Bug Reports** - Collective problem-solving
- 🤝 **Pull Requests** - Code collaboration & reviews

</div>

---
### Security

If you discover any security-related issues, please email [omaralwi2010@gmail.com](mailto:omaralwi2010@gmail.com) instead of using the issue tracker.

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
