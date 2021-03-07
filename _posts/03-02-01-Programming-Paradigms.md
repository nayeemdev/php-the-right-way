---
title: প্রোগ্রামিং দৃষ্টান্ত
isChild: true
anchor:  programming_paradigms
---

## প্রোগ্রামিং দৃষ্টান্ত {#programming_paradigms_title}

PHP হ'ল নমনীয়, গতিশীল ভাষা যা বিভিন্ন প্রোগ্রামিং কৌশল সমর্থন করে। এটি কয়েক বছর ধরে নাটকীয়ভাবে বিকশিত হয়েছে, উল্লেখযোগ্যভাবে পিএইচপি 5.0 (2004) এ একটি শক্ত অবজেক্ট-ভিত্তিক মডেল, পিএইচপি 5.3 (2009) এ অ্যানোনিমাস ফাংশন এবং নেমস্পেস এবং পিএইচপি 5.4 (2012) এ ট্রেইটস যুক্ত করেছে।

### অবজেক্ট ওরিয়েন্টেড প্রোগ্রামিং

PHP-তে ক্লাস, অ্যাবস্ট্রাক্ট ক্লাস, ইন্টারফেস, ইনহেরিটেন্স, কন্সট্রাক্টর, ক্লোনিং, এক্সেপশন এবং আরও অনেক কিছু সহ অবজেক্ট ওরিয়েন্টেড প্রোগ্রামিং বৈশিষ্ট্যগুলির একটি খুব সম্পূর্ণ সেট আছে।

* [অবজেক্ট ওরিয়েন্টেড PHP সম্পর্কে পড়ুন][oop]
* [ট্রেইটস সম্পর্কে পড়ুন][traits]

### ফাংশনাল প্রোগ্রামিং

PHP ফার্স্ট-ক্লাস  ফাংশনগুলিকে সমর্থন করে, যার অর্থ একটি ফাংশন একটি ভেরিয়েবলের জন্য বরাদ্দ করা যেতে পারে। উভয় ব্যবহারকারী-সংজ্ঞায়িত এবং বিল্ট-ইন ফাংশন একটি ভ্যারিয়েবল এবং ডায়নামিক ভাবে ইনভোক দ্বারা রেফারেন্স করা যেতে পারে। ফাংশনগুলি অন্যান্য ফাংশনগুলিতে আর্গুমেন্ট হিসাবে পাস করা যেতে পারে (_Higher-order Functions_) এবং ফাংশনগুলি অন্যান্য ফাংশনগুলি ফিরিয়ে দিতে পারে।

পুনরাবৃত্তি(_Recursion_), এমন একটি বৈশিষ্ট্য যা কোনও ফাংশনকে নিজেকে কল করার অনুমতি দেয়, ল্যাঙ্গুয়েজ দ্বারা এটি সমর্থিত, তবে বেশিরভাগ PHP কোড পুনরাবৃত্তির উপর ফোকাস  করে।

PHP 5.3 (২০০৯) থেকে নতুন অ্যানোনিমাস ফাংশন (closures সমর্থিত) উপস্থিত রয়েছে।

PHP ৫.৪ এ অবজেক্ট স্কোপ এর সাথে ক্লোসার বাইন্ড করার ক্ষমতা যোগ করা হয়েছে এবং callable এর জন্য সাপোর্ট উন্নতি করা হয়েছে যাতে এগুলোকে সব ক্ষেত্রে অ্যানোনিমাস ফাংশন এর সাথে ব্যবহার করা যায়।

* পড়া চালিয়ে যান [Functional Programming in PHP](/pages/Functional-Programming.html)
* [Anonymous Functions সম্পর্কে পড়ুন][anonymous-functions]
* [the Closure class সম্পর্কে পড়ুন][closure-class]
* [Closures RF সম্পর্কে পড়ুন][closures-rfc]
* [Callables সম্পর্কে পড়ুন][callables]
* [dynamically invoking functions with `call_user_func_array()` সম্পর্কে পড়ুন][call-user-func-array]

### মেটা প্রোগ্রামিং

পিএইচপি রিফ্লেকশন এপিআই এবং ম্যাজিক মেথডগুলোর মতো ব্যবস্থার মাধ্যমে বিভিন্ন ধরনের মেটা-প্রোগ্রামিং সমর্থন করে। এখানে অনেকগুলো ম্যাজিক মেথড এভেইলেবল আছে যেমন `__get()`, `__set()`, `__clone()`, `__toString()`, `__invoke()`, ইত্যাদি। that allow developers to hook into class behavior. Ruby ডেভেলপাররা প্রায়শই বলে থাকেন যে PHP -তে `method_missing` এর অভাব রয়েছে, তবে এটি `__call ()` এবং `__callStatic ()` হিসাবে এভেইলেবল।

* [Magic Methods সম্পর্কে পড়ুন][magic-methods]
* [Reflection সম্পর্কে পড়ুন][reflection]
* [Overloading সম্পর্কে পড়ুন][overloading]


[oop]: https://secure.php.net/language.oop5
[traits]: https://secure.php.net/language.oop5.traits
[anonymous-functions]: https://secure.php.net/functions.anonymous
[closure-class]: https://secure.php.net/class.closure
[closures-rfc]: https://wiki.php.net/rfc/closures
[callables]: https://secure.php.net/language.types.callable
[call-user-func-array]: https://secure.php.net/function.call-user-func-array
[magic-methods]: https://secure.php.net/language.oop5.magic
[reflection]: https://secure.php.net/intro.reflection
[overloading]: https://secure.php.net/language.oop5.overloading

