---
title: "نحوه مشارکت"
date: 2021-09-15T16:33:15+04:30
draft: false
tags : ["how-to-contribute", "مشارکت"]
---

خوشحالم که اینجا هستید :)

اگر قصد مشارکت دارید، فقط چند مرحله پیشرو داریم.

---

## 1

همینطور که می‌دانید این یک سایت
static
است که بوسیله
hugo
که یک 
static site generator
است ساخته و توسعه داده می‌شود.

پس در قدم اول نیاز به نصب این ابزار دارید.
هیوگو در مخازن اکثر توزیع های لینوکسی موجوده و میتوانید اون رو به راحتی بریزید.

> - Solus
>
> `sudo eopkg it hugo`

> - Arch
>
>`sudo pacman -S hugo`

> - Fedora
>
> `sudo dnf install hugo`

> - Ubuntu
>
> `sudo apt-get install hugo`

> - SUSE
>
>`sudo zypper in hugo`

---

## 2

فورک و کلون کردن ریپازیتوری.
دومین قدم اینه که این سایت رو از
[این ادرس](https://github.com/bit-orbit/bit-orbit.github.io)
fork
کنید و سپس روی سیستم لوکالتون
clone
کنید.

> - clone
> 
> ```
> git clone --recurse-submodules <Your_repo_addr>
> ```

---

## 3

بعد از نصب باید با چند دستور فایلتون رو بسازید، بنویسید، مشاهده کنید و در
آخر به ریپازیتوری آپلود کنید
<br>
<br>

- 3.1(ایجاد فصل)

برای ساخت یک فصل این دستور را بعد از اینکه وارد پوشه
clone 
شده، شدید وارد کنید. و فقط جای
ToolName
اسم ابزاری که می‌نویسید را جایگذاری کنید.

```
hugo new content/posts/ToolName/ToolName.md
```

- 3.2(مشاهده)

بعد از اینکه فایل رو ساختین شروع به نوشتن کنید :)
اما به این نیاز دارید که موقع نوشتن فایل، قالب نوشته های خود را بعد از
مستقر شدن ببینید، برای اینکه پیش از مستقر شدن در سایت اصلی، محتوای خودتون رو مشاهده
کنید، این دستور را وارد کنید و بعد وارد
[این آدرس](http://localhost:1313/the-secret-bit/)
بشید.

```
hugo server -D
```

- 3.3(آپلود به مخزن)

بعد از اینکه نوشتن رو تمام کردین، و نوشته ها رو پیش از استقرار مرور کردین،
کافیه که با این دستور همه زحماتتون رو به مخزن آپلود کنید.

```
git push
```

بعد وارد گیتهاب که شدید، وارد آدرس مخزنی که
fork
کردید بشید و دکمه
merge request
رو بزنید تا نوشته های شما به مخزن اصلی اضافه بشود.

---

## 4

برای درک بهتر خواننده های کتاب، باید ساختار نوشتاری یکسانی رو رعایت کنیم.
به این دلیل که کتاب به دست جامعه نوشته می‌شود، ممکن است هر نویسنده‌ای اصول و سبک متفاوتی
داشته باشد، بنابراین همینجا توافق می‌کنیم که از چند اصل نوشتاری کتاب پیروی کنیم.

- 4.1(فصل)

یک ابزار در یک فصل تشریح می‌شود.
برای مثال ابزار
wget
یک فصل دارد که این ابزار را توضیح می‌دهد.

- 4.2(کامند و خروجی)

اگر دستوری را می‌نوسید، قبل از دستور علامت
`$`
قرار دهید.

و برای مشخص کردن خروجی یک دستور از علامت
`#`
در پشت دستور استفاده کنید.

```
$ ls -lh

# drwxr-xr-x 2 root root 4.0K ژانویه   4 21:41 Desktop
# drwxr-xr-x 6 root root 4.0K فوریه   25 12:22 snap
# drwxr-xr-x 2 root root 4.0K ژانویه   4 13:06 Templates
```

- 4.3(الگو)

تمامی فصل ها از یک الگوری
markdown
پیروی می‌کنند.

```md

<div dir='rtl'>

[!["Image Alt"](img src)](Link of image)

فهرست

- [مقدمه](id)
- [قسمت دوم](id)

---

### مقدمه
توضیحات

---

# قسمت اول
توضیحات

---

### قسمت دوم
توضیحات

---

Author or Authors:

- name1 <email@example.com>
- name2 <email2@some.com>

</div>

```

---

## 5

برای نمایش دادن عکس ها کافیست یک پوشه داخل پوشه ابزار به نام پوشه اصلی بسازید
مثلا اگر شما در پوشه
wget
هستید، باید یک پوشه به همین نام درون همین پوشه بسازید
و عکس ها را درون آن قرار بدهید.

```
wget
│── wc.md
└── wget
    └── wget
        │── 1.jpg
        │── 2.png
        └── 3.gif
```