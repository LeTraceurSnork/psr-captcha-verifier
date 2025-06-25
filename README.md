# PSR Captcha
This repository contains all the interfaces related to proposed PSR CaptchaVerifierInterface

## Discussion
* [PHP-FIG repo PR](https://github.com/php-fig/fig-standards/pull/1330)

## Intendend usage

```php
class SpecificCaptchaVerifier implements \LeTraceurSnork\Captcha\CaptchaVerifierInterface
{
    // some implementation here
}

$captcha_verifier = new SpecificCaptchaVerifier('CAPTCHA_SECRET_KEY');
$captcha_response = $captcha_verifier->verify('user_token');
if ($captcha_response->isSuccess()) {
    // ... Captcha successfully passed
}
```
