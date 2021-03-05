---
isChild: true
anchor:  mac_setup
---

## Mac সেটআপ {#mac_setup_title}

macOS এ PHP আগে থেকে ইনস্টল করা থাকে তবে কিছুটা পুরোনো স্ট্যাবল ভার্সন থাকতে পারে। macOS PHP ইনস্টল করার অনেকগুলো উপায় আছে।

### Homebrew এর মাধ্যমে PHP ইনস্টল করুন

[Homebrew] হলো macOS এর প্যাকেজ ম্যানেজার যার মাধ্যমে অনেক সহজে PHP এবং অন্যান্য অনেক এক্সটেনশন ইনস্টল করা যায়। Homebrew এর মূল রিপোজিটরি PHP 5.6, 7.0, 7.1, 7.2, 7.3, 7.4, and PHP 8.0 এর জন্য "Formulae" প্রোভাইড করে থাকে। বর্তমান ভার্সন ইনস্টল করার জন্য নিচের কম্যান্ড টি চালান:

```
brew install php@8.0
```

আপনি `PATH` ভ্যারিয়েবল টি পরিবর্তন করে PHP এর আলাদা আলাদা ভার্সন এ যেতে পারবেন। এছাড়াও আপনি [brew-php-switcher][brew-php-switcher] ব্যবহার করে অটোমেটিক PHP ভার্সন পরিবর্তন করতে পারবেন।

### Macports এর মাধ্যমে PHP ইনস্টল করুন

OS X অপারেটিং সিস্টেম এ কম্যান্ড লাইন এর মাধ্যমে ইনস্টল, কম্পাইল, আপগ্রেড সহজতর করার জন্য [MacPorts] প্রজেক্ট টি হচ্ছে একটি ওপেন-সোর্স কমিউনিটি  উদ্যোগ 

MacPorts pre-compile binaries সাপোর্ট করে, তাই আপনার সব ডিপেন্ডেন্সি কে পুনরায় মূল ফাইল থেকে কম্পাইল করতে হয় না, এটা আপনার কাজ কে সহজ করে যদি আপনার সিস্টেম এ আগে থেকে কোনো প্যাকেজ ইনস্টল করা না থাকে। 

এই মুহুর্তে, আপনি `port install` কম্যান্ড এর সাহায্যে `php54`, `php55`, `php56`, `php70`, `php71`, `php72`, `php73`, `php74` অথবা `php80` ইনস্টল করতে পারেন ,উদাহরণ স্বরূপ:

    sudo port install php74
    sudo port install php80

এবং আপনি `select` কম্যান্ড এর মাধ্যমে আপনার বর্তমান PHP ভার্সন পরিবর্তন করতে পারবেন:

    sudo port select --set php php80

### phpbrew এর মাধ্যমে PHP ইনস্টল করুন

পিএইচপি এর একাধিক ভার্সন ইনস্টল এবং ম্যানেজ করার জন্য [phpbrew] একটা ভালো টুল। আপনি যদি ভার্চুয়াল মেশিন ব্যবহার না করেন এবং দুটি আলাদা প্রজেক্ট এর জন্য আলাদা PHP ভার্সন এর দরকার তাহলে এই টুল আপনাকে অনেক সাহায্য করবে।

### Liip's binary installer এর মাধ্যমে PHP ইনস্টল করুন

অন্য একটি জনপ্রিয় অপশন হলো [php-osx.liip.ch] যেটা আপনাকে ভার্সন 5.3 থেকে 7.3 পর্যন্ত এক লাইন এর ইনস্টলেশন পদ্ধতির সুবিধা দিয়ে থাকে।
এটি অ্যাপল দ্বারা ইনস্টল করা পিএইচপি বাইনারিগুলি ওভাররাইট করে না, কিন্তু আলাদা আলাদা লোকেশন(/usr/local/php5) এ ইনস্টল করে।

### সোর্স থেকে কম্পাইল করা 

PHP ইনস্টল এর অন্য একটি অপশন হলো [নিজে কম্পাইল][mac-compile] করা। এই মাধ্যমে অবশ্যই আপনাকে দেখতে হবে [Xcode][xcode-gcc-substitution] অথবা Apple's substitute
["Command Line Tools for XCode"] ইনস্টল করা আছে কি না যেটা Apple's Mac ডেভেলপার সেন্টার থেকে ডাউনলোড করা যায়।

### All-in-One ইনস্টলার

উপরের সবগুলো পদ্ধতি PHP নিজে হ্যান্ডেল করে এবং  [Apache][apache], [Nginx][nginx] or a SQL server এগুলো প্রোভাইড করে না।"All-in-one" যেমন [MAMP][mamp-downloads] এবং [XAMPP][xampp] হলো এমন সফটওয়্যার যেটা এই সবগুলো একসাথে থাকে এবং দ্রুত সেটআপ করা যায়।

[Homebrew]: https://brew.sh/
[Homebrew PHP]: https://github.com/Homebrew/homebrew-php#installation
[MacPorts]: https://www.macports.org/install.php
[phpbrew]: https://github.com/phpbrew/phpbrew
[php-osx.liip.ch]: https://php-osx.liip.ch/
[mac-compile]: https://secure.php.net/install.macosx.compile
[xcode-gcc-substitution]: https://github.com/kennethreitz/osx-gcc-installer
["Command Line Tools for XCode"]: https://developer.apple.com/downloads
[apache]: https://httpd.apache.org/
[nginx]: https://www.nginx.com/
[mamp-downloads]: https://www.mamp.info/en/downloads/
[xampp]: https://www.apachefriends.org/index.html
[brew-php-switcher]: https://github.com/philcook/brew-php-switcher
