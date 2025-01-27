# ভ্যারিয়েবল ও ডাটা টাইপস

## ভ্যারিয়েবল

প্রোগ্রামিং করতে গেলে প্রায়শই আমাদের বিভিন্ন ধরনের তথ্য উপাত্ত সংরক্ষণ করা লাগে । এই তথ্যগুলো আমরা কম্পিউটারের মেমোরীতে সংরক্ষন করে থাকি । ভ্যারিয়েবল হলো কম্পিউটার এর মেমোরীতে থাকা ছোট ছোট ব্লক যেখানে আমরা আমাদের প্রয়োজনমত ডাটা রাখতে পারি । এই মেমোরী ব্লকগুলোতে সংরক্ষিত ডাটা পরে এ্যাক্সেস করার জন্য আমরা আমাদের সুবিধামত নাম দিয়ে দেই । পিএইচপিতে ভ্যারিয়েবল তৈরি করা খুবই সহজ । সব ভ্যারিয়েবলই শুরু হবে ডলার সাইন \(`$`\) দিয়ে, ডলার সাইনের পরপরই ভ্যারিয়েবল এর নাম । এরপর ইকুয়াল সাইন \(`=`\) এর পর ঐ ভ্যারিয়েবল এর ভ্যালু ।

যেমন:

```php
<?php 
$name = "Abu Ashraf Masnun";
```

এখানে আমরা একটি ভ্যারিয়েবল তৈরি করলাম `$name` । ভ্যারিয়েবল এর নাম অবশ্যই আন্ডারস্কোর অথবা কোন এ্যালফাবেট দিয়ে শুরু হতে হবে । নামের শুরুতেই সংখ্যা ব্যবহার করা যাবে না । নামটি কেইস সেনসিটিভ । অর্থাৎ `$name` আর `$Name` সম্পূর্ণ আলাদা ভ্যারিয়েবল নাম ।

## ডাটা টাইপ

আমাদের দৈনন্দিন জীবনে ব্যবহৃত ডাটা নানা ধরনের হয়ে থাকে । কোনটা টেক্সট, কোনটা সংখ্যা, সংখ্যার ভিতরে আবার কোনটা পূর্ণ সংখ্যা, কোনটা ভগ্নাংশ - এই সব ডাটার একেকটা কম্পিউটার একেক ভাবে সংরক্ষণ করে । এখান থেকেই মূলত ডাটা টাইপ কনসেপ্ট এর উৎপত্তি ।

পিএইচপিতে আমরা কোন ভ্যারিয়েবল এর টাইপ জানতে `gettype()` ফাংশনটি ব্যবহার করতে পারি । যেমন:

```php
<?php
$age = 23; 
echo gettype($age); // integer
```

পিএইচপি তে বহুল ব্যবহৃত ডাটা টাইপ গুলো হলো:

### বুলিয়ান

বুলিয়ান টাইপ ব্যবহার করে আমরা কোন কিছু সত্য না মিথ্যা তা প্রকাশ করে থাকি । আরেকটু গভীরভাবে চিন্তা করলে আমরা দেখবো যখন কোন ভ্যারিয়েবল ঠিক বিপরীতধর্মী দুইটা ভ্যালুর যে কোন একটা গ্রহন করে তখন আমরা সেটাকে সচারচর বুলিয়ান টাইপ দিয়ে প্রকাশ করি ।

পিএইচপিতে বুলিয়ান টাইপের ভ্যালু হতে পারে `TRUE` অথবা `FALSE` ।

উদাহরণ:

```php
<?php

$isMarried = FALSE; 
$isAlive = TRUE;
```

### ইন্টিজারস

ইন্টিজার ব্যবহার করি আমরা পূর্ণ সংখ্যা প্রকাশ করার জন্য । এই পূর্ণ সংখ্যা ধনাত্বক বা ঋণাত্বক হতে পারে । যেমন: কারো বয়স ।

```php
<?php

$age = 75;
```

লক্ষ্যনীয় যে ইন্টিজার ডেসিম্যাল, অক্টাল, হেক্সাডেসিম্যাল কিংবা বাইনারি ফরমাটেও প্রকাশ করা যায়:

```php
<?php
$a = 1234; // ডেসিম্যাল
$a = -123; // ঋণাত্বক
$a = 0123; // অক্টাল, ডেসিম্যালে কনভার্ট করলে পাবো ৮৩
$a = 0x1A; // হেক্সাডেসিম্যাল, ডেসিম্যালে মান হবে ২৬ 
$a = 0b11111111; // বাইনারী, ডেসিম্যালে মান হবে ২৫৫
```

\(উদাহরণটি পিএইচপি ম্যানুয়াল থেকে নেওয়া, কমেন্ট বাংলায় অনুবাদ করা\)

### ফ্লোটিং পয়েন্ট বা ডাবল

ভগ্নাংশ কিংবা দশমিক সংখ্যা প্রকাশ করার জন্য আমরা ফ্লোটিং পয়েন্ট টাইপ ব্যবহার করি । এটাকে ডাবল কিংবা রিয়াল নাম্বার ও বলা হয় ।

```php
<?php

$temperature = 30.45;
```

### স্ট্রিংস

স্ট্রিংস হলো অনেকগুলো ক্যারেক্টারের সমষ্টি । স্ট্রিং ভ্যারিয়েবল তৈরি করতে হলে সাধারনত ডাবল কিংবা সিঙ্গল কোট ব্যবহার করা হয় ।

```php
<?php
$name = "The Doctor";
$planet = 'Gallifrey';
```

এছাড়াও `heredoc` এবং `nowdoc` ফরম্যাটেও স্ট্রিং তৈরি করা যায়:

```php
<?php
#herodoc
$doc = <<<DOC //herodoc এর label এইভাবেও লেখা যায় <<<"DOC" (Double Quotation দিয়ে)
Hello world!
DOC;

#nowdoc
$doc = <<<'DOC'
Hello world!
DOC;
```

এখানে, আমরা প্রথমে `<<<` এবং পরপরই একটি আইডেন্টিফায়ার \(আমাদের এক্ষেত্রে `DOC` \) ব্যবহার করি । এরপর একটি লাইন ব্রেক দিয়ে আমাদের স্ট্রিং লেখা হয় । ব্লক শেষ করার জন্য উপরোক্ট আইডেন্টিফায়ার টি নতুন লাইনে আবার লিখে সেমিকোলন দিয়ে স্টেটমেন্ট শেষ করা হয় । মনে রাখতে হবে শেষ লাইনে আইডেন্টিফায়ার এর আগে বা পরে কোন স্পেইস বা অন্য কোন ক্যারেক্টার ব্যবহার করা যাবে না ।
nowdoc herodoc এর মতই শুধু label টাকে `Signle Quotation` দিয়ে আটকাতে হবে।

### এ্যারে

এ্যারে হলো একটি তালিকা । যেখানে একটি ইনডেক্স এর বিপরীতে আমরা একটি ভ্যালু সংরক্ষণ করি । এ্যারে তৈরি করার জন্য আমরা বিল্ট ইন `array` কন্সট্র্যাক্ট ব্যবহার করি । ইনডেক্স এর বিপরীতে ভ্যালু ডিফাইন করার জন্য আমরা `=>` সিম্বল ব্যবহার করি ।

```php
<?php
$array = array(
    "foo" => "bar",
    "bar" => "foo",
);
```

এখানে `$array` একটি এ্যারে যার `foo` ইনডেক্স বা কি এর ভ্যালু `bar` এবং `bar` এর ভ্যালু `foo` । উদাহরণটি পিএইচপি ম্যানুয়াল থেকে নেওয়া ।

লক্ষ্যনীয় বিষয়: এ্যারে এর ইনডেক্স বা কি শুধুমাত্র স্ট্রিং বা ইন্টিজার হবে । তবে ইনডেক্স এর ভ্যালু যে কোন টাইপের হতে পারে ।

আমরা চাইলে, ইনডেক্স এর ভ্যালু স্কিপ করতে পারতাম । সেক্ষেত্রে পিএইচপি নিজে থেকেই ইনডেক্স এর ভ্যালু হিসেবে ক্রমিক সংখ্যা ব্যবহার করতো ।

```php
<?php
$list = array('a', 'c', 3, 'wow', 5);
```

এখানে এই এ্যারের ইনডেক্সগুলো হবে - 0, 1, 2, 3, 4 - মনে রাখতে হবে, এই ইনডেক্স হলো জিরো বেইড, অর্থাৎ ইনডেক্স গননা শুরু হয় জিরো থেকে । প্রথম আইটেমের ইনডেক্স তাই জিরো হয়, যে কোন আইটেমের ইনডেক্স হয় তার নিউমেরিক্যাল পজিশন থেকে এক কম।

পিএইচপি 5.4 থেকে এ্যারে ডিফাইন করার জন্য শর্টহ্যান্ড ব্যবহার করা যায়:

```php
 <?php

 $array = [
    "foo" => "bar",
    "bar" => "foo",
];

$list = ['a', 'z', 2, 10];
```

এখানে আমরা `array` এর পরিবর্তে `[` এবং `]` এর মধ্যে কি-ভ্যালু ডিফাইন করি ।

পিএইচপির এ্যারে ডাটা টাইপটি একই সাথে এ্যারে, লিস্ট, ডিকশনারী, স্ট্যাক, কিউ, কালেকশান প্রভৃতির কাজ করতে পারে । এ্যারে নিয়ে বিস্তারিত আলোচনা থাকছে `মাস্টারিং এ্যারে` চ্যাপ্টারে ।

### অবজেক্ট টাইপ

পিএইচপি ক্লাস থেকে `new` কিওয়ার্ড ব্যবহার করে অবজেক্ট ইন্সট্যান্স তৈরি করা যায় । অবজেক্ট সম্পর্কে আরো বিস্তারিত আমরা অবজেক্ট ওরিয়েন্টেড প্রোগ্রামিং চ্যাপ্টারে দেখবো ।

### নাল টাইপ

`null` হল একটি স্পেশাল ডাটা টাইপ। একটি ভ্যারিয়েবল তিন ভাবে `null` হতে পারে। 
- ভ্যারিয়েবল টাকে যদি `null` হিসেবে এসাইন করা হয়। 
- ভ্যারিয়েবল আনডিফাইন্ড হলে। ভ্যারিয়েবলের ভ্যালু সেট করার আগ পর্যন্ত তা `null` থাকে। 
- ভ্যারিয়েবল টাকে `unset` করলে। 

যখন কোন ভ্যারিয়েবলের কোন ভ্যালু থাকে না তখন সেটা নাল টাইপ এর হয় । এই টাইপের একমাত্র গ্রহনযোগ্য ভ্যালু হলো - `null` - যার মানে ঐ ভ্যারিয়েবল এর কোন ভ্যালু নেই ।

## টাইপ কনভার্শন

### অটোমেটিক কনভার্শন

পিএইচপিতে আমরা ভ্যারিয়েবল ডিক্লেয়ার করার সময় এর টাইপ নির্ধারণ করে দিতে পারি না । ভ্যারিয়েবল এর ভ্যালুর উপর নির্ভর করে পিএইচপি নিজে থেকেই ডাটা টাইপ নির্বাচন করে নেয় । যেমন `$var` এর ভ্যালু হিসেবে যদি আমরা `hello world` পাস করি, তাহলে `$var` হবে স্ট্রিং, পরবর্তীতে যদি `$var` এর ভ্যালু হিসেবে `23` হয় তবে সেটি হবে ইন্টিজার ।

পিএইচপি কনটেক্সট অনুযায়ী ভ্যারিয়েবল এর টাইপ স্বয়ংক্রিয়ভাবে পরিবর্তন করে নেয় । যেমন, আমরা যখন যোগ করি তখন যদি উভয় পাশই ইন্টিজার ভ্যালু হয় তখন রেজাল্ট ও হবে ইন্টিজার । কিন্তু যে কোন একটি যদি ডাবল হয় তাহলে রেজাল্ট হবে ডাবল ।

এসব ক্ষেত্রে মূল ভ্যারিয়েবল এর টাইপ পরিবর্তন হয় না কিন্তু ফলাফলের পরিবর্তন হয় । পিএইচপির এই অটোমেটিক টাইপ কনভার্শন এর ব্যাপারে খেয়াল রাখা জরুরী । নাহলে অনাকাঙ্ক্ষিত ফলাফল পাওয়া অসম্ভব কিছুই না ।

### ম্যানুয়াল টাইপ কনভার্শন

ম্যানুয়ালি টাইপ কনভার্ট করতে আমরা `settype()` ফাংশনটি ব্যবহার করি । এটি ঐ ভ্যারিয়েবল এর টাইপ এবং ভ্যালু দুটোই পরিবর্তন করতে পারে ।

```php
<?php
$age = 23;
$name = "masnun";

settype($age, "string");
settype($name, "integer");

var_dump($age); 
var_dump($name);
```

