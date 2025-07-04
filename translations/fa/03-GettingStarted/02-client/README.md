<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "2342baa570312086fc19edcf41320250",
  "translation_date": "2025-06-17T15:15:35+00:00",
  "source_file": "03-GettingStarted/02-client/README.md",
  "language_code": "fa"
}
-->
در کد قبلی ما:

- کتابخانه‌ها را وارد کردیم
- یک نمونه از کلاینت ایجاد کردیم و با استفاده از stdio برای انتقال به سرور متصل شدیم.
- پرامپت‌ها، منابع و ابزارها را فهرست کردیم و همه را فراخوانی کردیم.

همین است، یک کلاینت که می‌تواند با سرور MCP ارتباط برقرار کند.

در بخش تمرین بعدی وقت می‌گذاریم و هر قطعه کد را جداگانه بررسی می‌کنیم و توضیح می‌دهیم چه اتفاقی می‌افتد.

## تمرین: نوشتن یک کلاینت

همانطور که گفته شد، اجازه دهید کد را با دقت توضیح دهیم و اگر می‌خواهید می‌توانید همزمان کدنویسی کنید.

### -1- وارد کردن کتابخانه‌ها

بیایید کتابخانه‌هایی که نیاز داریم را وارد کنیم، ما به ارجاعاتی به کلاینت و پروتکل انتقال انتخابی خود، stdio، نیاز خواهیم داشت. stdio پروتکلی است برای مواردی که قرار است روی دستگاه محلی شما اجرا شوند. SSE پروتکل انتقال دیگری است که در فصل‌های آینده نشان خواهیم داد اما این گزینه دیگر شماست. فعلاً بیایید با stdio ادامه دهیم.

---

بیایید به مرحله نمونه‌سازی برویم.

### -2- نمونه‌سازی کلاینت و انتقال

ما باید یک نمونه از انتقال و یک نمونه از کلاینت خود ایجاد کنیم:

---

### -3- فهرست کردن ویژگی‌های سرور

حالا یک کلاینت داریم که می‌تواند به سرور متصل شود اگر برنامه اجرا شود. اما در واقع ویژگی‌های سرور را فهرست نمی‌کند، پس بیایید این کار را انجام دهیم:

---

عالی است، حالا همه ویژگی‌ها را دریافت کرده‌ایم. حالا سوال این است که کی از آنها استفاده کنیم؟ خوب، این کلاینت نسبتاً ساده است، ساده به این معنی که ما باید به صورت صریح وقتی می‌خواهیم ویژگی‌ها را صدا بزنیم. در فصل بعدی، کلاینت پیشرفته‌تری ایجاد خواهیم کرد که به مدل زبان بزرگ خود (LLM) دسترسی دارد. فعلاً بیایید ببینیم چطور می‌توانیم ویژگی‌های سرور را فراخوانی کنیم:

### -4- فراخوانی ویژگی‌ها

برای فراخوانی ویژگی‌ها باید مطمئن شویم که آرگومان‌های درست را مشخص کرده‌ایم و در برخی موارد نام چیزی که می‌خواهیم فراخوانی کنیم را وارد کنیم.

---

### -5- اجرای کلاینت

برای اجرای کلاینت، دستور زیر را در ترمینال تایپ کنید:

---

## تمرین

در این تمرین، شما از آنچه یاد گرفته‌اید برای ایجاد یک کلاینت استفاده می‌کنید اما کلاینت خودتان را می‌سازید.

در اینجا یک سرور وجود دارد که می‌توانید از آن استفاده کنید و باید از طریق کد کلاینت خود آن را فراخوانی کنید، ببینید آیا می‌توانید ویژگی‌های بیشتری به سرور اضافه کنید تا جذاب‌تر شود.

---

## راه حل

[راه حل](./solution/README.md)

## نکات کلیدی

نکات کلیدی این فصل درباره کلاینت‌ها به شرح زیر است:

- می‌توانند برای کشف و فراخوانی ویژگی‌ها روی سرور استفاده شوند.
- می‌توانند سرور را در حالی که خودشان شروع می‌شوند راه‌اندازی کنند (مانند این فصل) اما کلاینت‌ها همچنین می‌توانند به سرورهای در حال اجرا متصل شوند.
- راه بسیار خوبی برای آزمایش قابلیت‌های سرور در کنار گزینه‌هایی مانند Inspector است که در فصل قبلی توضیح داده شد.

## منابع بیشتر

- [ساخت کلاینت‌ها در MCP](https://modelcontextprotocol.io/quickstart/client)

## نمونه‌ها

- [ماشین حساب جاوا](../samples/java/calculator/README.md)
- [ماشین حساب .Net](../../../../03-GettingStarted/samples/csharp)
- [ماشین حساب جاوااسکریپت](../samples/javascript/README.md)
- [ماشین حساب تایپ‌اسکریپت](../samples/typescript/README.md)
- [ماشین حساب پایتون](../../../../03-GettingStarted/samples/python)

## ادامه مسیر

- بعدی: [ایجاد کلاینت با LLM](/03-GettingStarted/03-llm-client/README.md)

**سلب مسئولیت**:  
این سند با استفاده از سرویس ترجمه هوش مصنوعی [Co-op Translator](https://github.com/Azure/co-op-translator) ترجمه شده است. در حالی که ما در تلاش برای دقت هستیم، لطفاً توجه داشته باشید که ترجمه‌های خودکار ممکن است حاوی خطاها یا نادرستی‌هایی باشند. سند اصلی به زبان بومی خود باید به عنوان منبع معتبر در نظر گرفته شود. برای اطلاعات حیاتی، استفاده از ترجمه حرفه‌ای انسانی توصیه می‌شود. ما مسئول هیچ گونه سوءتفاهم یا تفسیر نادرستی که ناشی از استفاده از این ترجمه باشد، نیستیم.