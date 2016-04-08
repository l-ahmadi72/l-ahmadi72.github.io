---
layout: post
title:  "نکات مهم در کد نويسی جاوا اسکريپت"
date:   2016-04-07 21:35:44 +0430
categories: jekyll update
---

نکات مهم در کد نويسی جاوا اسکريپت


در این قسمت از آموزش جاوا اسکریپت ، می خواهیم نکات مهم در کدنویسی جاوا اسکریپت را در چهار مورد بیان کنیم .

جاوا اسکریپت به بزرگ یا کوچک بودن حروف حساس است.

برخلاف html جاوا اسکریپت به بزرگ یا کوچک بودن حروف حساس است و در مواقع نام گذاری توابع و تعاریف باید به این موضوع توجه کرد عدم رعایت این نکته موجب بروز خطا در صفحه خواهد شد و هر یک از دستورات و کلمات کلیدی در جاوا اسکریپت فقط به یک صورت که استاندارد باش نوشته شوند . در مثال زير 2 متغير با نام های يکسان ، ولی متفاوت در بزرگ يا کوچک بودن حروف به نام های "Matn" و "matn" ايجاد و مقدار دهی شده اند . خروجی کد نشان می دهد که اين دو متغير کاملا با هم متفاوت هستند و هر يک مقدار مخصوص به خود را دارند :

    <script type="text/javascript">
      var matn = "This is a Variable ." ;
      var Matn = "This is another Variable ." ;
      document.write ( matn ) ;
      document.write ( Matn ) ;
    </script>     کد
    خروجی :  This is a Variable .This is another Variable .

شکل صحيح نوشتن متد چاپ خروجی در جاوا اسکريپت به صورت documnet.write است . در مثال زير ابتدا دستور را به شکل نادرست و با حروف بزرگ به صورت Documnet.Write نوسته ايم ، که باعث ايجاد خطا در صفحه شده و خروجی نداريم . اما در حالت دوم آنرا به شکل صحيح نوشته ايم ، که خروجی درست را نيز مشاهده می کنيم :

    <script type="text/javascript">
      var Str = "An Investigation for Development" ;
      Document.Write ( Str ) ;
    </script>    
      خروجی :  

    <script type="text/javascript">
      var Str = "An Investigation for Development" ;
      document.write ( Str ) ;
    </script>    
    خروجی :  An Investigation for Development

جاوا اسکریپت فواصل خالی اضافی در کدنویسی را نادیده می گیرد

استفاده از فواصل خالی اضافه توسط کدهای جاوا اسکریپت از سوی مرورگر نادیده گرفته می شود و تاثیری ندارد.بين دستورات و کلمات کليدی بايد حداقل يک فاصله وجود داشته باشد ، در اينجا منظور از فاصله اضافی ، بيش از يک کاراکتر فاصله است .

نوشتن عبارت های متنی در بیش از یک خط

در هنگام تعریف و استفاده از عبارت های متنی در دستوراتی نظير document.write و ... ، می توان ادامه متن را به کمک يک کاراکتر \ به سطر بعدی انتقال داد . اين مسئله در زمانی که عبارت های متنی طولانی استفاده می شود ، کاربرد دارد .

    <script type="text/javascript">
      document.write ( "Java Script is a client side language . \
      It`s codes executes in the computer of visitor " ) ;
    </script>
    خروجی : Java Script is a client side language . It`s codes executes in the computer of visitor

درج توضيحات ( comments ) مورد نظر در بخش کد نويسی

 در اسکريپت های نوشته شده به زبان جاوا اسکريپت ، می توان توضيحات مورد نظر را به صورت ويژه ای در درون کدها وارد کرد . اين توضيحات به طور کامل از سوی مرورگر ناديده گرفته شده و در خروجی نمايش داده نمی شوند . از توضيحات معمولا برای نشانه گذاری يا ارائه توضيحاتی راجع به کدهای برنامه استفاده می شود .
دو نوع توضيح در جاوا اسکريپت می توان ايجاد کرد :

1 . توضيحات يک خطی : اين توضيات به کمک دو بک اسلش // به صورت زير وارد می شود . توضيحات ارائه شده به اين صورت حداکثر می تواند در يک خط باشد . به مثال زير دقت کنيد . در اين مثال خط اول يک comment خط دوم يک دستور چاپ خروجی است . همانظور که در خروجی کد مشخص است ، دستور چاپ توسط مرورگر اجرا شده ولی comment نمايش دادده نمی شود :

    <script type="text/javascript">
      // this is a one line comment . navigator won`t show it .
      document.write ( "How to write a comment" ) ;
    </script>
    خروجی : How to write a comment

2 . توضيحات چند خطی : با استفاده از يک نماد */ در ابتدای اولين خط توضيحات و يک نماد /* در آخرين خط توضيحات ، می توان توضيحات چند خطی در اسکريپت ها وارد کرد . از اين حالت برای ارائه توضيحات طولانی استفاده می شود . به مثال زير دقت کنيد . در اين مثال هم يک دستور و يک comment چند خطی قرار داده شده است . دستور توسط مرورگر اجرا شده ، ولی comment نمايش داده نمی شود :

    <script type="text/javascript">
    /* this is a multi line comment . navigator won`t show it .
    We use it for long comments .
    It can be several lines */

    document.write ( "How to write a multi line comment" ) ;
    </script>     کد
    خروجی : How to write a multi line comment
