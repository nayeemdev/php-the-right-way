---
title: উইন্ডোস সেটআপ
isChild: true
anchor:  windows_setup
---

## উইন্ডোস সেটআপ {#windows_setup_title}

আপনি [windows.php.net/download][php-downloads] থেকে বাইনারিজ ডাউনলোড করতে পারবেন। PHP এক্সট্র্যাক্ট করার পরে যাতে আপনি যেকোন জায়গা থেকে এক্সিকিউট করতে পারেন তাই PHP ফোল্ডার(যেখানে php.exe আছে) এর Root [PATH][windows-path] সেট করুন।

লোকাল ডেভেলপমেন্ট এবং শেখার জন্য আপনি বিল্ট-ইন ওয়েব সার্ভার ব্যবহার করতে পারেন যাতে আপনাকে সার্ভার কনফিগার নিয়ে কোনো চিন্তা না করতে হয়। আপনি [Web Platform Installer][wpi], [XAMPP][xampp], [EasyPHP][easyphp], [OpenServer][openserver] এবং [WAMP][wamp] ব্যবহার করতে পারেন এগুলো উইন্ডোস এনভায়রনমেন্ট দ্রুত সেটআপ করতে সাহায্য করবে।  তবে আপনি উইন্ডোস এনভায়রনমেন্ট এ কাজ করে লিনাক্স এনভায়রনমেন্ট এ ডেপ্লয় করতে চাইলে এই টুলস ব্যবহার এর ক্ষেত্রে সতর্ক হতে হবে কারণ ইটা প্রোডাকশন থেকে কিছুটা আলাদা।

আপনি যদি প্রোডাকশন সিস্টেম উইন্ডোস এ রান করতে চান, তাহলে IIS7 আপনাকে সবথেকে ভালো পারফরমেন্স দেবে। সাধারণ PHP ম্যানেজ এবং কনফিগার এর জন্য আপনি [phpmanager][phpmanager] (IIS7 এর জন্য GUI প্লাগিন)  ব্যবহার করতে পারেন। IIS7 আসে FastCGI built-in এবং ready to go সিস্টেম নিয়ে, আপনার শুধুমাত্র PHP কনফিগার করতে হবে হ্যান্ডলার হিসেবে। PHP এর আরও রিসোর্স এবং সাপোর্ট এর জন্য [iis.net এর ডেডিকেটেড সাইট][php-iis].

সাধারণত ডেভেলপমেন্ট এবং প্রোডাকশন এর জন্য আলাদা এনভায়রনমেন্ট এ চালাতে গেলে লাইভ সার্ভার এ বিভিন্ন ধরণের বাগ/এরর সামনে আস্তে পারে। যদি আপনি ডেভেলপমেন্ট এর জন্য উইন্ডোস বেছে নেন এবং ডেপ্লয় অন্য সার্ভার এ করেন যেটা উইন্ডোস না সেক্ষত্রে আপনার [ভার্চুয়াল মেশিন](/#virtualization_title) ব্যবহার করা উচিত।

ক্রিস ট্যানকারলে খুব সহায়ক একটি ব্লগ পোস্ট তৈরি করেছেন সে কি কি টুলস সে ব্যবহার করে [উইন্ডোস এ PHP ডেভেলপমেন্ট][windows-tools] এর ক্ষেত্রে। 

[easyphp]: http://www.easyphp.org/
[phpmanager]: http://phpmanager.codeplex.com/
[openserver]: http://open-server.ru/
[wamp]: http://www.wampserver.com/en/
[php-downloads]: http://windows.php.net/download/
[php-iis]: http://php.iis.net/
[windows-path]: http://www.windows-commandline.com/set-path-command-line/
[windows-tools]: http://ctankersley.com/2016/11/13/developing-on-windows-2016/
[wpi]: https://www.microsoft.com/web/downloads/platform.aspx
[xampp]: http://www.apachefriends.org/en/xampp.html
