# گزارش کار پروژه FastAPI

# فایل init :  برای اینکه پایتون هر پوشه را به عنوان پکیج بشناسد.

# فایل crud: 
از sqlalchemy  کلاس Session  را فراخوانی میکند. از فایلمون models,schemas  را فراخوانی میکند و این ساختارها برای اعتبارسنجی و ارسال  داده ها به پایگاه داده استفاده میشود.

  <img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%A7%D9%88%D9%84.PNG?raw=true" />

  این تابع شناسه دانشجو را به عنوان ورودی میگیرد و از پایگاه داده مورد نظر اطلاعات دانشجو را میگیرد و در این تابع ابتدا یک اتصال به پایگاه داده برقرار میشود و فیلتر داده از جدول را بر اساس شناسه  دانشجو انجام میشود و first اولین رکورد را برمیگرداند. create_student اطلاعات دانشجو را ایجاد کرده و به پایگاه داده ارسال میکند.

 <img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%AF%D9%88%D9%85.PNG?raw=true" /> 
  
این تابع removeestudent, شناسه دانشجو را به عنوان ورودی میگیرد و پایگاه داده, رکورد مربوط به دانشجوی مورد نظر را حذف میکند.
<img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%B3%D9%88%D9%85.PNG?raw=true" />

این تابع update_student شناسه دانشجو را به عنوان ورودی میگیرد و پایگاه داده, رکورد مربوط به دانشجوی مورد نظر را بروزرسانی میکند.
<img src="https://github.com/zahraw-rz/zahra/blob/main/%DA%86%D9%87%D8%A7%D8%B1%D9%85.PNG?raw=true" />

این تابع شناسه یک استاد را به عنوان ورودی میگیرد و از پایگاه داده مورد نظر اطلاعات استاد را میگیرد و در این تابع ابتدا یک اتصال به پایگاه داده برقرار میشود و فیلتر داده از جدول را بر اساس شناسه  استاد انجام میشود و first اولین رکورد را برمیگرداند. create_ostad اطلاعات استاد را ایجاد کرده و به پایگاه داده ارسال میکند.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D9%BE%D9%86%D8%AC%D9%85(1).PNG?raw=true" />

این تابع update_ostad شناسه استاد را به عنوان ورودی میگیرد و پایگاه داده,رکورد مربوط به استاد مورد نظر را بروزرسانی(اپدیت) میکند.
<img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%B4%D8%B4%D9%85.PNG?raw=true" />

این تابع removeostad, شناسه استاد را به عنوان ورودی میگیرد و پایگاه داده رکورد مربوط به استاد مورد نظر را حذف میکند.
<img src="https://github.com/zahraw-rz/zahra/blob/main/%D9%87%D9%81%D8%AA%D9%85.PNG?raw=true" />

این تابع شناسه درس را به عنوان ورودی میگیرد و از پایگاه داده مورد نظر اطلاعات درس را میگیرد و در این تابع ابتدا یک اتصال به پایگاه داده برقرار میشود و فیلتر داده از جدول را بر اساس شناسه  درس انجام میشود و first اولین رکورد را برمیگرداند. create_cours اطلاعات درس را ایجاد کرده و به پایگاه داده ارسال میکند.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D9%87%D8%B4%D8%AA%D9%85.PNG?raw=true" />

این تابع update_course شناسه درس را به عنوان ورودی میگیرد و پایگاه داده,رکورد مربوط به درس مورد نظر را بروزرسانی میکند.
<img src="https://github.com/zahraw-rz/zahra/blob/main/%D9%86%D9%87%D9%85.PNG?raw=true" />

این تابع removecource شناسه درس را به عنوان ورودی میگیرد و پایگاه داده رکورد مربوط به درس مورد نظر را حذف میکند.
<img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%AF%D9%87%D9%85.PNG?raw=true" />


# فایل database:
این کد یک تنظیمات پایه ای را برای اتصال به یک دیتابیس SQLite با استفاده از sqlalchemy را انجام میدهد و از این تنظیمات میتوان برای تعریف مدل های دیتابیس و ایجاد جدول ها استفاده کرد. اول ما کتابخانه های مورد نیاز را ایمپورت میکنیم.دوم ادرس دیتابیس را تعریف میکنیم.سوم موتور اتصال به دیتابیس را ایجاد میکنیم. چهارم SessionLocal را تعریف میکنیم و در آخر یک کلاس پایه برای مدل ها تعریف میکنیم.
<img src="https://github.com/zahraw-rz/zahra/blob/main/%DB%8C%D8%A7%D8%B2%D8%AF%D9%87%D9%85.PNG?raw=true" />


# فایل dockerfile:
 این from pythin یعنی زبانی که میخواهیم استفاده کنیم و نسخه آن را نشان میدهد. WORkDIR یعنی پوشه ای که فایل های پروشه در آن قرار دارد. COPY یعنی کپی کردن فایل کتابخانه های مورد نیاز در پوشه داکر. RUN یعنی نصب تمام کتابخانه های مورد نیاز از روی فایل کتابخانه های مورد نیاز. COPY یعنی کپی کردن فایل های پروژه در پوشه داکر. CMD این یه دستور در ترمینال اجرا میکند و پروژه را ران میکند.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%AF%D9%88%D8%A7%D8%B2%D8%AF%D9%87%D9%85.PNG?raw=true" />


# فایل main:
این کد یک API برای مدیریت دانشجویان و اساتید و دروس با استفاده از fastapi و sqlalchemy انجام میدهد. اول کتابخانه های مورد نیاز را ایمپورت میکنیم.sys برای رفع مشکل parent پکیج است. و بعد ماژول های داخلی پروژه را ایمپورت میکنیم. بعد جداول دیتابیس را ایجاد میکنیم.
<img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%B3%DB%8C%D8%B2%D8%AF%D9%87%D9%85.PNG?raw=true" />

این کد برنامه Fastapi را ایجاد میکند. تابع get_db یک اتصال به پایگاه داده را ایجاد و به صورت موقت در اختیار قرار میدهد. سپس در پایان اتصال را به صورت خودکار میبندد. از try  برای مدیریت استثناها استفاده میشود و از yeild به عنوان یک روش مدیریت منابع عمل کرده که در ان شی پایگاه داده برای استفاده در جای دیگری برگردانده میشود.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%DA%86%D9%87%D8%A7%D8%B1%D8%AF%D9%87%D9%85.PNG?raw=true" />

این کد یک تابع به اسم create_student را تعریف میکند که با روش post برای ایجاد یک دانشجو در یک پایگاه داده را فراهم میکند.اول بررسی میکند که ایا دانشجو با همان شناسه وجود دارد یا نه، و اگر وجود داشته باشد خطا را برمیگرداند.دوم صحت دانشجو و روابط انتخاب شده برای دروس و اساتید را بررسی میکند.و در آخراگر همه چیز درست باشد دانشجو را در پایگاه داده ایجاد میکند.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D9%BE%D8%A7%D9%86%D8%B2%D8%AF%D9%87%D9%85.PNG?raw=true" />

















