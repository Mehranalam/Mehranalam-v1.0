---
title: نحوه نوشتن نرم افزار با علوم ریاضی
date: 2023-03-32
description: کامپیوترهای مدرن به دلیل کار دانشمند کامپیوتر لزلی لامپورت می توانند به طور موثر با یکدیگر هماهنگ شوند. او از آن زمان توجه خود را به کارآمدتر کردن برنامه نویسی معطوف کرد.
image: images/Lamport.jpg
tags:
   - ریاضیات
   - نرم‌افزارها 
   - برنامه‌نویسی
   - تکنولوژی
---

[eslie Lamport](http://www.lamport.org/) ممکن است نام آشنای نباشد، اما او پشت تعدادی از آنها برای دانشمندان کامپیوتر است: برنامه حروفچینی LaTeX و کاری که زیرساخت ابری را در گوگل و آمازون ممکن کرد. او همچنین توجه بیشتری را به چند مسئله معطوف کرد و نام‌های متمایزی مانند الگوریتم نانوایی و مسئله ژنرال‌های بیزانسی به آن‌ها داد. این تصادفی نیست دانشمند کامپیوتر 81 ساله به طور غیرعادی در مورد نحوه استفاده و تفکر مردم در مورد نرم افزار فکر می کند.

در سال 2013 برنده جایزه A.M. جایزه تورینگ که جایزه نوبل محاسبات را به خاطر کارش بر روی سیستم های توزیع شده، که در آن اجزای متعدد در شبکه های مختلف برای رسیدن به یک هدف مشترک هماهنگ می شوند، در نظر گرفته می شود. جستجوهای اینترنتی، محاسبات ابری و هوش مصنوعی، همگی شامل سازماندهی لشگرهای ماشین‌های محاسباتی قدرتمند برای کار با هم هستند. البته این نوع هماهنگی شما را در برابر مشکلات بیشتری باز می کند.

لامپورت یک بار گفت: «سیستم توزیع‌شده سیستمی است که در آن خرابی رایانه‌ای که حتی از وجود آن اطلاعی نداشتید، می‌تواند رایانه شما را غیرقابل استفاده کند».

یکی از بزرگترین منابع مشکلات، «سیستم‌های همزمان» است، که در آن چندین عملیات محاسباتی در طول برش‌های زمانی روی هم می‌افتند که منجر به ابهام می‌شود: ساعت کدام کامپیوتر مناسب است؟ لامپورت در مقاله‌ای [1978](https://dl.acm.org/doi/10.1145/359545.359563)، مفهوم «علیت» را با استفاده از بینشی از نسبیت خاص برای حل این مسئله معرفی کرد. ممکن است دو ناظر در مورد ترتیب رویدادها با هم اختلاف داشته باشند، اما اگر یک رویداد باعث دیگری شود، ابهام را از بین می برد. و ارسال یا دریافت پیام می تواند علیت را در بین چندین فرآیند ایجاد کند. ساعت‌های منطقی - که اکنون ساعت‌های Lamport نیز نامیده می‌شوند - یک راه استاندارد برای استدلال در مورد سیستم‌های همزمان ارائه می‌کنند.

با در دست داشتن این ابزار، دانشمندان کامپیوتر بعداً تعجب کردند که چگونه می‌توانند این رایانه‌های متصل را به‌طور سیستماتیک بزرگ‌تر کنند، بدون اینکه باگ‌هایی اضافه کنند. لامپورت یک راه حل زیبا ارائه کرد: Paxos، یک «الگوریتم اجماع» که به چندین رایانه اجازه می دهد تا وظایف پیچیده را انجام دهند. بدون Paxos و خانواده الگوریتم‌های آن، محاسبات مدرن نمی‌توانست وجود داشته باشد.

عکس تالیا هرمان برای مجله کوانتا; ویدیوی امیلی بودر و مارکوس روشا برای مجله کوانتا

در اوایل دهه 1980، زمانی که لامپورت این رشته را توسعه داد، LaTeX را نیز ایجاد کرد، یک سیستم آماده‌سازی اسناد که راه‌های پیچیده‌ای را برای تایپ کردن فرمول‌های پیچیده و قالب‌بندی اسناد علمی ارائه می‌دهد. LaTeX به استانداردی برای قالب بندی مقالات نه تنها در ریاضیات و علوم کامپیوتر بلکه در بیشتر حوزه های علمی تبدیل شده است.

کار لامپورت از دهه 1990 بر روی "تأیید رسمی"، استفاده از اثبات های ریاضی برای تأیید صحت سیستم های نرم افزاری و سخت افزاری متمرکز شده است. قابل ذکر است، او یک "زبان مشخصات" به نام [TLA+](https://lamport.azurewebsites.net/tla/tla.html) (برای منطق زمانی اقدامات) ایجاد کرد. مشخصات نرم افزار مانند یک نقشه یا دستور العمل برای یک برنامه است. توضیح می دهد که نرم افزار چگونه باید در سطح بالایی رفتار کند. همیشه لازم نیست، زیرا کدگذاری یک برنامه ساده شبیه به جوشاندن تخم مرغ است. اما یک کار پیچیده تر با سهام بالاتر - معادل کدگذاری یک ضیافت نه دوره - به دقت بیشتری نیاز دارد. شما باید هر یک از اجزای هر غذا را آماده کنید، آنها را به روشی دقیق ترکیب کنید، سپس آنها را به ترتیب صحیح برای هر مهمان سرو کنید. این امر مستلزم دستور العمل‌ها و دستورالعمل‌های دقیقی است که به زبانی واضح و مختصر نوشته شده باشند، اما توصیف‌هایی که به نثر انگلیسی نوشته شده‌اند می‌توانند جایی برای تفسیر نادرست باقی بگذارند. TLA+ از زبان دقیق ریاضیات برای جلوگیری از اشکالات و جلوگیری از نقص های طراحی استفاده می کند.

با استفاده از دستور پخت، یا مشخصات، به عنوان ورودی، برنامه ای به نام مدل بررسی می کند که آیا دستور العمل منطقی است و مطابق خواسته کار می کند، و یک غذا را همانطور که سرآشپز می خواهد تولید می کند. لامپورت ابراز تاسف می کند که چگونه برنامه نویسان اغلب قبل از نوشتن مشخصات مناسب، یک سیستم را با هم ترکیب می کنند، در حالی که سرآشپزها هرگز نمی توانند یک ضیافت را بدون اینکه قبلاً بدانند که دستور العمل های آنها جواب می دهد، ترتیب می دهند.

_Quanta_ با لامپورت در مورد کارش بر روی سیستم های توزیع شده، مشکلات آموزش علوم کامپیوتر و اینکه چگونه استفاده از TLA+ می تواند به برنامه نویسان در ساختن سیستم های بهتر کمک کند، صحبت کرد. مصاحبه برای وضوح فشرده و ویرایش شده است.

<img src="https://raw.githubusercontent.com/Mehranalam/Mehranalam-v1.0/master/static/images/Lamport_1.jpg" alt="lamport">

## معرفی

### بیایید با Paxos شروع کنیم، زیرا این الگوریتم بسیار تأثیرگذار است. چه شد که در وهله اول شروع به کار روی آن کردید؟

مردم در حال ساختن یک سیستم با مقداری کد بودند، و من این تصور را داشتم که آنچه که کد آنها سعی در انجام آن دارد غیرممکن است. بنابراین تصمیم گرفتم آن را ثابت کنم و در عوض الگوریتمی را ارائه کردم که مردم باید برای سیستم خود از آن استفاده می کردند.

### الگوریتم اصلی آنها چه اشکالی داشت؟

خوب، آنها یک الگوریتم نداشتند، فقط یک دسته کد داشتند. تعداد بسیار کمی از برنامه نویسان به الگوریتم فکر می کنند. وقتی می خواهید یک سیستم همزمان بنویسید، اگر فقط آن را بدون الگوریتم کدنویسی کنید، هیچ راهی وجود ندارد که برنامه شما پر از اشکال نباشد.

 - منبع : https://www.quantamagazine.org/computing-expert-says-programmers-need-more-math-20220517/
