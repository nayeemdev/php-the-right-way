---
title: কোড স্টাইল গাইড
anchor: code_style_guide
---

# কোড স্টাইল গাইড {#code_style_guide_title}

পিএইচপি কমিউনিটি বড় এবং বৈচিত্র্যময়, অসংখ্য লাইব্রেরি সমন্বিত, ফ্রেমওয়ার্ক এবং কম্পোনেন্ট। PHP ডেভেলপারদের পক্ষে এগুলোর মধ্যে কিছু নির্বাচন করা এবং এগুলো একত্রিত করে একটা আলাদা প্রজেক্ট করা সাধারণ বিষয়। এটি গুরুত্বপূর্ণ যে পিএইচপি কোডগুলি একটি সাধারণ কোড স্টাইল অনুসরণ করে যাতে ডেভেলপারদের তাদের প্রজেক্টের জন্য বিভিন্ন লাইব্রেরিতে মেশানো ও মিলানো সহজ হয়।

[Framework Interop Group][fig] একাধিক স্টাইল প্রস্তাব এবং অনুমোদিত করেছে। এগুলির সবগুলিই কোড-স্টাইলে সম্পর্কিত নয়, কিন্তু এগুলো [PSR-1][psr1], [PSR-12][psr12] and [PSR-4][psr4] ব্যবহার করে। এই রিকোমেন্ডেশনগুলো শুধুমাত্র এক সেট নিয়ম যা Drupal, Zend, Symfony, Laravel, CakePHP, phpBB, AWS SDK, FuelPHP, Lithium, ইত্যাদি প্রজেক্টগুলো গ্রহণ করেছে।  এগুলি আপনি আপনার নিজের প্রজেক্টের জন্য ব্যবহার করতে পারেন বা নিজের ব্যক্তিগত স্টাইল ব্যবহার করতে পারেন।

আদর্শভাবে, আপনার পিএইচপি কোডটি লিখতে হবে যা একটি পরিচিত স্ট্যান্ডার্ডকে মেনে চলে। এটি পিএসআর বা কোনও একটি কোডিং স্ট্যান্ডার্ড এর  সংমিশ্রণ হতে পারে
যা PEAR বা Zend  এর তৈরী। এর মানে হলো  অন্যান্য ডেভেলপাররা সহজেই আপনার কোডটি পড়তে এবং কাজ করতে পারে এবং কম্পোনেন্টগুলো  বাস্তবায়নকারী অ্যাপ্লিকেশনগুলির প্রচুর থার্ড পার্টি কোডের সাথে কাজ করার পরেও ধারাবাহিকতা থাকতে পারে।

* [PSR-1 সম্পর্কে পড়ুন][psr1]
* [PSR-12 সম্পর্কে পড়ুন][psr12]
* [PSR-4 সম্পর্কে পড়ুন][psr4]
* [PEAR Coding Standards সম্পর্কে পড়ুন][pear-cs]
* [Symfony Coding Standards সম্পর্কে পড়ুন ][symfony-cs]

আপনি [PHP_CodeSniffer][phpcs] ব্যবহার করতে পারেন এই রিকোমেন্ডেশনগুলির মধ্যে যেকোনোটির কোড চেক করতে, এবং [Sublime Text][st-cs] এর মতো কোড এডিটর এর মধ্যে প্লাগিনের সাহায্যে সাথে সাথে ফিডব্যাক পেতে পারেন।

আপনি নিম্নলিখিত টুলগুলোর একটি ব্যবহার করে কোড লেআউট স্বয়ংক্রিয়ভাবে ঠিক করতে পারেন:

- একটি হলো [PHP Coding Standards Fixer][phpcsfixer] যার একটি খুব ভাল পরীক্ষিত কোডবেস আছে।
- আর এই [PHP Code Beautifier and Fixer][phpcbf] টুল টি যা PHP_CodeSniffer এর সাথে অন্তর্ভুক্ত রয়েছে সেই অনুসারে আপনার কোডটি সামঞ্জস্য করতে ব্যবহার করা যেতে পারে।

এবং আপনি শেল থেকেও  ম্যানুয়ালি phpcs চালাতে পারেন:

    phpcs -sw --standard=PSR1 file.php

এটি ত্রুটিগুলি দেখায় এবং সেগুলি কীভাবে ঠিক করা যায় তা বর্ণনা করবে।
এই কম্যান্ডটি গিট হুকের অন্তর্ভুক্ত করার ক্ষেত্রেও এটি  সহায়ক হতে পারে।
এইভাবে, যে ব্রাঞ্চ গুলো স্ট্যান্ডার্ড এর বিপরীতে অর্থাৎ স্ট্যান্ডার্ড লংঘন করে সেগুলো ঠিক করা না পর্যন্ত রিপোসিটোরি তে ঢুকতে পারে না।

আপনার যদি PHP_CodeSniffer থাকে, তবে আপনি [PHP Code Beautifier and Fixer][phpcbf] এর দ্বারা উল্লিখিত কোড লেআউট সমস্যাগুলি স্বয়ংক্রিয়ভাবে ঠিক করতে পারেন।

    phpcbf -w --standard=PSR1 file.php

এর জন্য অন্য একটি বিকল্প হলো [PHP Coding Standards Fixer][phpcsfixer]।
কোড স্ট্রাকচারের ঠিক করার আগে এটির মধ্যে কোন ধরণের ত্রুটি ছিল তা এটি দেখায়।

    php-cs-fixer fix -v --rules=@PSR1 file.php

সমস্ত প্রতীক নাম এবং কোড অবকাঠামোর জন্য ইংরেজি পছন্দ করা হয়। মন্তব্যগুলি যে কোনও ভাষায় লেখা হতে পারে, কোডবেসে কাজ করা সমস্ত বর্তমান এবং ভবিষ্যতের কারোর দ্বারা সহজেই পড়ার এবং বুঝার জন্য।

পরিশেষে, পরিষ্কার পিএইচপি কোড লেখার জন্য একটি ভাল পরিপূরক রিসোর্স হ'ল [Clean Code PHP][cleancode].

[fig]: https://www.php-fig.org/
[psr1]: https://www.php-fig.org/psr/psr-1/
[psr12]: https://www.php-fig.org/psr/psr-12/
[psr4]: https://www.php-fig.org/psr/psr-4/
[pear-cs]: https://pear.php.net/manual/en/standards.php
[symfony-cs]: https://symfony.com/doc/current/contributing/code/standards.html
[phpcs]: https://pear.php.net/package/PHP_CodeSniffer/
[phpcbf]: https://github.com/squizlabs/PHP_CodeSniffer/wiki/Fixing-Errors-Automatically
[st-cs]: https://github.com/benmatselby/sublime-phpcs
[phpcsfixer]: https://cs.symfony.com/
[cleancode]: https://github.com/jupeter/clean-code-php
