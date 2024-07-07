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

این کد یک تابع به اسم read_student تعریف میکند که با روش get اطلاعات یک دانشجو را دریافت میکند و پارامتر student_id  شناسه دانشجو را میگیرد. با استفاده از get_db یک اتصال به پایگاه داده برقرار میشود.تابع crud.get_student اطلاعات دانشجو را از پایگاه داده با استفاده از student_id دریافت میکند. بررسی میکند اگر دانشجو وجود نداشته باشد کد 404 را برمیگرداند و اگر دانشجو وجود داشته باشد، اطلاعات دانشجو را برمیگرداند.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%B4%D8%A7%D9%86%D8%B2%D8%AF%D9%87%D9%85.PNG?raw=true" />

این کد یک تابع به اسم update_student تعریف میکند که با روش put که اطلاعات یک دانشجو را بروزرسانی میکند، با استفاده از get_db  یک اتصال به پایگاه داده برقرار میشود. تابع crud.update_student اطلاعات دانشجو در پایگاه داده بروزرسانی میشود.اگر دانشجو وجود نداشت یک خطا با کد 404 برمیگرداند.از schema.validate_student  برای بررسی اعتبار اطلاعات دانشجو فراخوانی میشود. scourseids کد های دروس از رشته جدا شده و هرکدام بررسی میشود که ایا در پایگاه داده موجود است یا خیر که اگر کدی دریافت نشد، خطای مربوطه در error_relation  ذخیره شود.اگر هرگونه خطای ارتباطی وجود داشته باشد( مثلا کد درس یا استاد نامعتبر باشد)  یک خطای HTTP با کد 400 جزییات خطاها برمیگرداند. اگر همه چیز درست باشد، اطلاعات بروزرسانی شده دانشجو برگردانده میشود.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D9%87%D9%81%D8%AF%D9%87%D9%85.PNG?raw=true" />

این کد یک تابع به اسم  del_student تعریف میکند که به روش delete  برای حذف یک دانشجو عمل میکند. با استفاده از get_db یک اتصال به پایگاه داده برقرار میشود.تابع crud.get_student اطلاعات دانشجو را از پایگاه داده با استفاده از student_id دریافت میکند. بررسی میکند اگر دانشجو وجود نداشته باشد کد 404 (یافت نشد)  را برمیگرداند. اگر دانشجو وجود داشته باشد با استفاده از crud.removestudent دانشجو از پایگاه داده حذف میشود.و در اخر اطلاعات دانشجوی حذف شده به عنوان پاسخ برگردانده میشود.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D9%87%DB%8C%D8%AC%D8%AF%D9%87%D9%85.PNG?raw=true" />

این کد یک تابع به اسم create_ostad را تعریف میکند که با روش post برای ایجاد یک استاد در یک پایگاه داده را فراهم میکند.اول بررسی میکند که ایا استادی با شناسه lid وجود دارد یا نه، و اگر وجود داشته باشد خطا با کد 400 را برمیگرداند. کد دروس از رشته جدا شده و کدوم به صورت جدا بررسی میشوند ایا در پایگاه داده موجود هستند یا خیر که اگر کدی دریافت نشود یک خطا با کد 400 و با جزییات خطاها برگردانده میشود.و در آخراگر همه چیز درست باشد استاد را در پایگاه داده ایجاد میشود.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D9%86%D9%88%D8%B2%D8%AF%D9%87%D9%85.PNG?raw=true" />


این کد یک تابع به اسم read_ostad تعریف میکند که با روش get اطلاعات یک استاد را دریافت میکند و پارامتر ostad_id  شناسه استاد را میگیرد. با استفاده از get_db یک اتصال به پایگاه داده برقرار میشود.تابع crud.get_ostad اطلاعات استاد را از پایگاه داده با استفاده از ostad_id دریافت میکند. بررسی میکند اگر استاد وجود نداشته باشد کد 404 را برمیگرداند و اگر استاد وجود داشته باشد، اطلاعات استاد را به صورت یک مدل  schemas.ostad_response برمیگرداند.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%A8%DB%8C%D8%B3%D8%AA%D9%85.PNG?raw=true" />

این کد یک تابع به اسم update_ostad تعریف میکند که با روش put که اطلاعات یک استاد را بروزرسانی میکند، با استفاده از get_db  یک اتصال به پایگاه داده برقرار میشود. تابع crud.update_ostad اطلاعات استاد در پایگاه داده بروزرسانی میشود.اگر استاد وجود نداشت یک خطا با کد 404 برمیگرداند.از schema.validate_ostad  برای بررسی اعتبار اطلاعات استاد فراخوانی میشود.  کد های دروس از رشته جدا شده و هرکدام بررسی میشود که ایا در پایگاه داده موجود است یا خیر که اگر کدی دریافت نشد، خطای مربوطه در error_relation  ذخیره شود.اگر هرگونه خطای ارتباطی وجود داشته باشد یک خطای HTTP با کد 400  و جزییات خطاها برمیگرداند. اگر همه چیز درست باشد، اطلاعات بروزرسانی شده استاد را به عنوان پاسخ برگردانده میشود.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%A8%DB%8C%D8%B3%D8%AA%20%D9%88%20%DB%8C%DA%A9%D9%85.PNG?raw=true" />

ین کد یک تابع به اسم  del_ostad تعریف میکند که به روش delete  برای حذف یک استاد عمل میکند. با استفاده از get_db یک اتصال به پایگاه داده برقرار میشود.تابع crud.get_ostad اطلاعات استاد را از پایگاه داده با استفاده از ostad_id دریافت میکند. بررسی میکند اگر استاد وجود نداشته باشد کد 404 (استاد پیدا نشد)  را برمیگرداند. اگر استاد وجود داشته باشد با استفاده از crud.removeostad اطلاعات استاد از پایگاه داده حذف میشود.و در اخر اطلاعات استاد حذف شده به عنوان پاسخ برگردانده میشود.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%A8%DB%8C%D8%B3%D8%AA%20%D9%88%20%D8%AF%D9%88%D9%85.PNG?raw=true" />

ین کد یک تابع به اسم create_course را تعریف میکند که با روش post برای ایجاد یک درس جدید در یک پایگاه داده را فراهم میکند.با استفاده از get_db یک اتصال به پایگاه داده برقرار میشود. crud.get_course اول بررسی میکند که ایا درسی با شناسه cid وجود دارد یا نه، و اگر وجود داشته باشد خطا با کد 400  و پیام (درس قبلا ثبت شده) را برمیگرداند. تابع schemas.validate_course برای بررسی اعتبار اطلاعات درس فراخوانی میشود.و در آخراگر همه چیز درست باشد، یک درس در پایگاه داده ایجاد میشود.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%A8%DB%8C%D8%B3%D8%AA%20%D9%88%20%D8%B3%D9%88%D9%85.PNG?raw=true" />

این کد یک تابع به اسم read_course تعریف میکند که با روش get اطلاعات یک درس را دریافت میکند و پارامتر course_id  شناسه درس را میگیرد. با استفاده از get_db یک اتصال به پایگاه داده برقرار میشود.تابع crud.get_course اطلاعات درس را از پایگاه داده با استفاده ازcourse_id دریافت میکند. بررسی میکند اگر درس وجود نداشته باشد کد 404 را برمیگرداند و اگر درس وجود داشته باشد، اطلاعات درس را برمیگرداند.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%A8%DB%8C%D8%B3%D8%AA%20%D9%88%20%DA%86%D9%87%D8%A7%D8%B1%D9%85.PNG?raw=true" />

این کد یک تابع به اسم update_course تعریف میکند که با روش put که اطلاعات یک درس را بروزرسانی میکند، با استفاده از get_db  یک اتصال به پایگاه داده برقرار میشود. تابع crud.update_course اطلاعات درس در پایگاه داده بروزرسانی میشود.اگر درس وجود نداشت یک خطا با کد 404 برمیگرداند.از schema.validate_course  برای بررسی اعتبار اطلاعات درس فراخوانی میشود. اگر همه چیز درست باشد، اطلاعات بروزرسانی شده درس را به عنوان پاسخ برگردانده میشود.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%A8%DB%8C%D8%B3%D8%AA%20%D9%88%20%D9%BE%D9%86%D8%AC%D9%85.PNG?raw=true" />

این کد یک تابع به اسم  del_course تعریف میکند که به روش delete  برای حذف یک درس عمل میکند. با استفاده از get_db یک اتصال به پایگاه داده برقرار میشود.تابع crud.get_course اطلاعات درس را از پایگاه داده با استفاده از course_id دریافت میکند. بررسی میکند اگر درس وجود نداشته باشد کد 404 را برمیگرداند. اگر درس وجود داشته باشد با استفاده از crud.removecourse اطلاعات درس از پایگاه داده حذف میشود.و در اخر اطلاعات درس حذف شده به عنوان پاسخ برگردانده میشود.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%A8%DB%8C%D8%B3%D8%AA%20%D9%88%20%D8%B4%D8%B4%D9%85.PNG?raw=true" />

# فایل Models:
این کد شامل تعریف مدل های دیتابیس با استفاده از SQLAlchemy است. اول کتابخانه های مورد نیاز را ایمپورت میکنیم. sys برای رفع مشکل مسیر پروژه است.بعد ماژول های داخلی پروژه را ایمپورت میکنیم.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%A8%DB%8C%D8%B3%D8%AA%20%D9%88%20%D9%87%D9%81%D8%AA%D9%85.PNG?raw=true" />

یک کلاس به اسم student میسازیم و جدول student را در ان ایجاد میکنیم که این جدول شامل ستون های مختلفی برای نمایش اطلاعات دانشجو در پایگاه داده تعریف میکند مثل نام، نام خانوادگی، شماره دانشجویی، تاریخ تولد، آدرس و...

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%A8%DB%8C%D8%B3%D8%AA%20%D9%88%20%D9%87%D8%B4%D8%AA%D9%85.PNG?raw=true" />

یک کلاس به اسم ostad میسازیم و جدول ostad را در آن ایجاد میکنیم که این جدول شامل ستون های مختلفی برای نمایش اطلاعات استاد در پایگاه داده تعریف میکند.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%A8%DB%8C%D8%B3%D8%AA%20%D9%88%20%D9%86%D9%87%D9%85.PNG?raw=true" />

یک کلاس به اسم course میسازیم و جدول course را در آن ایجاد میکنیم که این جدول شامل ستون های مختلفی برای نمایش اطلاعات درس در پایگاه داده تعریف میکند.

<img src="https://github.com/zahraw-rz/zahra/blob/main/%D8%B3%DB%8C%20%D8%A7%D9%85.PNG?raw=true" />

# فایل schemas:
اول کتابخانه ها را وارد میکنیم.Union برای تعریف دادههای پیچیدس، HTTPException  برای مدیریت خطاها ، Session  برای مدیریت جلسات پایگاه داده.pydantic برای ایجاد مدل های داده، re برای استفاده از عبارات منظم و.... و کلاس student با استفاده از BaseModel  ایجاد شده است که داده های مختلفی در ان وجود دارد.

<img src="



















