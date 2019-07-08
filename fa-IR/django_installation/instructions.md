> قسمت‌هایی از این بخش بر اساس دوره آموزشی Geek Girls Carrots است (https://github.com/ggcarrots/django-carrots).
> 
> قسمتهایی نیز بر پايه دوره آموزشی [django-marcador tutorial](http://django-marcador.keimlink.de/) و با با مجوز Creative Commons Attribution-ShareAlike 4.0 International License است. حقوق دوره آموزشی django-marcador متعلق به Markus Zapke-Gründemann و همکاران می‌باشد.

## محیط مجازی

قبل از اینکه ما جنگو را نصب کنیم، ابزاری بسیار پراستفاده به شما می‌دهیم تا با نصب آن محیط برنامه نویسی خود را بر روی کامپیوترتان تمیز و مرتب نگه دارید. می‌توانید برای ادامه کار از این مرحله صرف نظر کنید اما استفاده از آن بسیار توصیه می‌شود. شروع کار با تنظیمات مناسب جلوی بسیاری از مشکلات در آینده را می‌گیرد!

بنابراین، اجازه دهید یک ** محیط مجازی ** یا virtual environment بسازیم (همچنین به آن * virtualenv* هم گفته می‌شود). محیط مجازی، تنظیمات پایتون/جنگو را برای هر پروژه و جدا از دیگر پروژه‌ها قرنطینه و حفظ خواهد کرد. یعنی هر تغییری که در تنظیمات یک وبسایت انجام می‌دهید، بر روی دیگر وبسایت‌هایی که در حال توسعه آن‌ها هستید تاثیر نخواهد گذاشت. خب، درست است؟

آنچه شما باید انجام دهید این است که یک پوشه را پیدا کنید که در آن می‌خواهید ` محیط مجازی` را ایجاد کنید. برای مثال، پوشه home. در ویندوز، چیزی شبیه `C:\Users\Name` است (که در آن `Name` نام کاربری شما است که با آن وارد ویندوز شده‌اید).

> **نکته: ** در ویندوز اطمینان حاصل کنید که نام این پوشه حاوی کاراکترهای خاص یا دارای اعراب نیست؛ اگر نام کاربری شما دارای کاراکترهای خاص است، از یک پوشه دیگر استفاده کنید، به عنوان مثال `C:\djangogirls`.

برای این آموزش ما از یک پوشه جدید `djangogirls` در پوشه اصلی شما استفاده خواهیم کرد:

{% filename %}خط فرمان{% endfilename %}

    $ mkdir djangogirls
    $ cd djangogirls
    

ما یک محیط مجازی به نام `myvenv` خواهیم ساخت. فرمان کلی در این قالب خواهد بود:

{% filename %}خط فرمان{% endfilename %}

    $ python3 -m venv myvenv
    

<!--sec data-title="Virtual environment: Windows" data-id="virtualenv_installation_windows"
data-collapse=true ces-->

برای ایجاد یک ` محیط مجازی` جدید، باید محیط دستورات command prompt را باز کنید و دستور <`python -m venv myvenv` را اجرا کنید. شبیه این خواهد شد:

{% filename %}خط فرمان{% endfilename %}

    C:\Users\Name\djangogirls> python -m venv myvenv
    

در اینجا `myvenv` نام `محیط مجازی` شماست. می‌توانید هر نام دیگری انتخاب کنید اما از حروف کوچک استفاده کنید و از اسپیس، اعراب گذاری و کاراکترهای خاص استفاده نکنید. فکر خوبی است که اسم کوتاهی نیز انتخاب کنید چون بعدتر ارجاعات زیادی به آن خواهید داشت!

<!--endsec-->

<!--sec data-title="Virtual environment: Linux and OS X" data-id="virtualenv_installation_linuxosx"
data-collapse=true ces-->

می‌توانیم با دستور `python3 -m venv myvenv` هم در لینوکس و هم در OS X `محیط مجازی` بسازیم. شبیه این خواهد بود:

{% filename %}خط فرمان{% endfilename %}

    $ python3 -m venv myvenv
    

نام `محیط مجازی` شما، `myvenv` است. می‌توانید هر نام دیگری انتخاب کنید اما از حروف کوچک استفاده کنید و از اسپیس استفاده نکنید. فکر خوبی است که اسم کوتاهی نیز انتخاب کنید چون بعدتر ارجاعات زیادی به آن خواهید داشت!

> **نکته: ** در بعضی نسخه‌های دبیان/اوبونتو ممکن است چنین پیغام خطایی دریافت کنید:
> 
> {% filename %}خط فرمان{% endfilename %}
> 
>     The virtual environment was not created successfully because ensurepip is not available.  On Debian/Ubuntu systems, you need to install the python3-venv package using the following command.
>        apt install python3-venv
>     You may need to use sudo with that command.  After installing the python3-venv package, recreate your virtual environment.
>     
> 
> در این موارد دستورالعمل داده شده در بالا را دنبال کنید. پکیج `python3-venv` را نصب کنید: {% filename %}خط فرمان{% endfilename %}
> 
>     $ sudo apt install python3-venv
>     
> 
> **نکته: ** در بعضی نسخه‌های دبیان/اوبونتو ساختن محیط مجازی با این دستور ممکن است باعث چنین خطایی بشود:
> 
> {% filename %}خط فرمان{% endfilename %}
> 
>     Error: Command '['/home/eddie/Slask/tmp/venv/bin/python3', '-Im', 'ensurepip', '--upgrade', '--default-pip']' returned non-zero exit status 1
>     
> 
> برای حل این مشکل، از دستور `virtualenv` استفاده کنید.
> 
> {% filename %}خط فرمان{% endfilename %}
> 
>     $ sudo apt install python-virtualenv
>     $ virtualenv --python=python3.6 myvenv
>     
> 
> **نکته: ** اگر چنین خطایی گرفتید
> 
> {% filename %}خط فرمان{% endfilename %}
> 
>     E: Unable to locate package python3-venv
>     
> 
> در عوض از این دستور استفاده کنید:
> 
> {% filename %}خط فرمان{% endfilename %}
> 
>     sudo apt install python3.6-venv
>     

<!--endsec-->

## کار کردن با محیط مجازی

دستور بالا یک پوشه به نام `myvenv` می‌سازد (یا هر نام دیگری که شما گذاشته باشید) که شامل محیط مجازی ماست (درواقع مجموعه‌ای از پوشه‌ها و فایل‌ها).

<!--sec data-title="Working with virtualenv: Windows" data-id="virtualenv_windows"
data-collapse=true ces-->

محیط مجازی خود را با اجرای دستور زیر فعال کنید:

{% filename %}خط فرمان{% endfilename %}

    C:\Users\Name\djangogirls> myvenv\Scripts\activate
    

> **نکته: ** در ویندوز 10 و در هنگام استفاده از Windows PowerShell ممکن است با این خطا مواجه شوید `execution of scripts is disabled on this system`. در این شرایط یک بار دیگر Windows PowerShell را با گزینه "Run as Administrator" اجرا کنید. سپس دستورات زیر را قبل از فعال کردن محیط مجازی خود، اجرا کنید:
> 
> {% filename %}خط فرمان{% endfilename %}
> 
>     C:\WINDOWS\system32> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned
>         Execution Policy Change
>         The execution policy helps protect you from scripts that you do not trust. Changing the execution policy might expose you to the security risks described in the about_Execution_Policies help topic at http://go.microsoft.com/fwlink/?LinkID=135170. Do you want to change the execution policy? [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): A
>     

<!--endsec-->

<!--sec data-title="Working with virtualenv: Linux and OS X" data-id="virtualenv_linuxosx"
data-collapse=true ces-->

محیط مجازی را با دستور زیر فعال کنید:

{% filename %}خط فرمان{% endfilename %}

    $ source myvenv/bin/activate
    

به یاد داشته باشید که `myvenv` را با نامی که برای `محیط مجازی` خود انتخاب کرده‌اید عوض کنید!

> **نکته: ** گاهی اوقات ممکن است پوشه `source` در دسترس نباشد. در این مواقع دستور زیر را امتحان کنید:
> 
> {% filename %}خط فرمان{% endfilename %}
> 
>     $ . myvenv/bin/activate
>     

<!--endsec-->

> **NOTE:** For users of the popular editor VS Code, which come with an integrated terminal based off windows powershell, if you wish to stick with the integrated terminal, you may run the following command to activate your virtual environment:
> 
>     $ . myvenv\Scripts\activate.ps1
>     
> 
> The advantage is that you don't have to switch between editor windows and command-line windows

هنگامی که پیشوند `(myvenv)` در کنسول خط فرمان اضافه شود به معنی آن است که `محیط مجازی` شما فعال شده است.

وقتی درون یک محیط مجازی کار می‌کنید کلمه `python` به صورت اتوماتیک به نسخه صحیح پایتون ارجاع می‌دهد در نتیجه می‌توانید به جای `python3` از `python` استفاده کنید.

بسیار خوب، ما همه نیازمندی‌ها را داریم حالا می‌توانیم جنگو را نصب کنیم!

## نصب جنگو

حالا که `محیط مجازی` شما فعال شده است می‌توانید جنگو را نصب کنید.

قبل از آن باید مطمئن شویم که آخرین نسخه `pip` که برای نصب جنگو استفاده می‌شود در محیط مجازی فعال باشد:

{% filename %}خط فرمان{% endfilename %}

    (myvenv) ~$ python -m pip install --upgrade pip
    

### نصب جنگو به کمک فایل الزامات

یک فایل الزامات فایلی است که لیستی از پکیج های وابسته است که می‌باید به کمک `pip install` نصب شوند:

در ابتدا یک فایل `requirements.txt` در پوشه `djangogirls/` بسازید. معمولاً می‌توانید از خود ویرایشگر کد که قبل‌تر نصب کرده‌اید هم برای ساختن فایل جدید استفاده کنید. یک فایل جدید در ویرایشگر کد بسازید و سپس به نام `requirements.txt`در پوشه `djangogirls/` ذخیره‌اش کنید. پوشه شما شبیه این خواهد بود:

    djangogirls
    ┘───requirements.txt
    

در فایل `djangogirls/requirements.txt` باید خط زیر را اضافه کنید:

{% filename %}djangogirls/requirements.txt{% endfilename %}

    Django~={{ book.django_version }}
    

حالا دستور `pip install -r requirements.txt` را اجرا کنید تا جنگو نصب شود.

{% filename %}خط فرمان{% endfilename %}

    (myvenv) ~$ pip install -r requirements.txt
    Collecting Django~={{ book.django_version }} (from -r requirements.txt (line 1))
      Downloading Django-{{ book.django_version }}-py3-none-any.whl (7.1MB)
    Installing collected packages: Django
    Successfully installed Django-{{ book.django_version }}
    

<!--sec data-title="Installing Django: Windows" data-id="django_err_windows"
data-collapse=true ces-->

> If you get an error when calling pip on Windows platform, please check if your project pathname contains spaces, accents or special characters (for example, `C:\Users\User Name\djangogirls`). If it does, please consider using another place without spaces, accents or special characters (suggestion: `C:\djangogirls`). Create a new virtualenv in the new directory, then delete the old one and try the above command again. (Moving the virtualenv directory won't work since virtualenv uses absolute paths.)

<!--endsec-->

<!--sec data-title="Installing Django: Windows 8 and Windows 10" data-id="django_err_windows8and10"
data-collapse=true ces-->

> Your command line might freeze after when you try to install Django. If this happens, instead of the above command use:
> 
> {% filename %}command-line{% endfilename %}
> 
>     C:\Users\Name\djangogirls> python -m pip install -r requirements.txt
>     

<!--endsec-->

<!--sec data-title="Installing Django: Linux" data-id="django_err_linux"
data-collapse=true ces-->

> If you get an error when calling pip on Ubuntu 12.04 please run `python -m pip install -U --force-reinstall pip` to fix the pip installation in the virtualenv.

<!--endsec-->

عالی! بالاخره در نهایت آماده شدید تا یک برنامه جنگو بسازید!