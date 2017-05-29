Nette Mail: Sending E-mails
===========================

[![Downloads this Month](https://img.shields.io/packagist/dm/nette/mail.svg)](https://packagist.org/packages/nette/mail)
[![Build Status](https://travis-ci.org/nette/mail.svg?branch=master)](https://travis-ci.org/nette/mail)
[![Coverage Status](https://coveralls.io/repos/github/nette/mail/badge.svg?branch=master)](https://coveralls.io/github/nette/mail?branch=master)
[![Latest Stable Version](https://poser.pugx.org/nette/mail/v/stable)](https://github.com/nette/mail/releases)
[![License](https://img.shields.io/badge/license-New%20BSD-blue.svg)](https://github.com/nette/mail/blob/master/license.md)

Almost every web application needs to send e-mails, whether newsletters or order confirmations. That's why Nette Framework provides necessary tools.

Example of creating an e-mail using `Nette\Mail\Message` class:

```php
use Nette\Mail\Message;

$mail = new Message;
$mail->setFrom('John <john@example.com>')
	->addTo('peter@example.com')
	->addTo('jack@example.com')
	->setSubject('Order Confirmation')
	->setBody("Hello, Your order has been accepted.");
```

All parameters must be encoded in UTF-8.

And sending:

```php
use Nette\Mail\SendmailMailer;

$mailer = new SendmailMailer;
$mailer->send($mail);
```
