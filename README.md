# Mautic Mailketing Plugin

[![license](https://img.shields.io/circleci/project/github/KonstantinCodes/mautic-recaptcha.svg)](https://circleci.com/gh/KonstantinCodes/mautic-recaptcha/tree/master) [![license](https://img.shields.io/packagist/v/koco/mautic-recaptcha-bundle.svg)](https://packagist.org/packages/koco/mautic-recaptcha-bundle)
[![Packagist](https://img.shields.io/packagist/l/koco/mautic-recaptcha-bundle.svg)](LICENSE) [![mautic](https://img.shields.io/badge/mautic-%3E%3D%202.15.2-blue.svg)](https://www.mautic.org/mixin/recaptcha/)

This Plugin brings Mailketing integration to Mautic 2.15.2 and newer.

Licensed under GNU General Public License v3.0.

## Installation via composer
1. Execute `composer require pekanbarugamer/mautic-mailketing` in the main directory of the Mautic installation.
2. Clear the cache via console command `php app/console cache:clear --env=prod` (might take a while) *OR* manually delete the `app/cache/prod` directory.

## Configuration
Navigate to the Plugins page and click "Install/Upgrade Plugins". You should now see a "Mailketing integration" plugin.

### Emails
Navigate to the Configuration page and open Email Settings section. Set "Mailketing - API" service to send email through and enter your Mailketing API key.

### Webhooks
1. Navigate to your Mailketing Page > Integration > Webhhok.
2. Input Webhook:
    1. URL: https://YOURMAUTICSITE/mailer/mailketing_api/callback
    2. Supported events:
        * Error
        * Soft Bounce
        * Hard Bounce
        * Invalid email
        * Complaint
        * Unsubscribed
        * Blocked
        
