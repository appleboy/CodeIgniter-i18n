Internationalization (i18n) library for CodeIgniter
========================

It is a simple internationalization (i18n) for CodeIgniter 2.1.X

Requirement
========================

* CodeIgniter 2.1.X
* Enable Session

What it does
========================

Have the language field in the URL, exapmle:

* http://xxx.com/?lang=en-us
* http://xxx.com/index.php/welcome/index?lang=en-us

Installation
========================

copy application/config/language.php to your_app/application/config/
copy application/core/MY_Lang.php to your_app/application/core/

    $ cp application/config/language.php our_app/application/config/
    $ cp application/core/MY_Lang.php your_app/application/core/

Configuration
========================

Open application/config/language.php file

* language_field

You can find this field in URL, default value is "lang", example: xxx.com/?lang=zh-tw

* language_default_key

Default language you want to output.

* language_list

The language array lists you can support.

    key: defined from $_['HTTP_ACCEPT_LANGUAGE']
    value: corresponding to your language folder.

How to use
========================

application/language/english/about_lang.php

    <?php  if ( ! defined('BASEPATH')) exit('No direct script access allowed');
    $lang['home'] = "Home";
    $lang['introduction'] = "Introduction";
    $lang['location'] = "Location";

View

    <p><?php echo lang('about.home')?></p>
    <p><?php echo lang('about.introduction')?></p>
    <p><?php echo lang('about.location')?></p>

The language class will add prefix value on all language array key automatically.

example:

    about_lang.php => key: about.xxxx
    api_lang.php => Key: api.xxxx

Copyright
========================

Copyright (C) 2011 Bo-Yi Wu ( appleboy AT gmail.com )
