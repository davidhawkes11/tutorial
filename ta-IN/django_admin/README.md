# டான்ஜோ நிர்வாகி

நாங்கள் மாதிரியுள்ள பதில்களைச் சேர்க்க, திருத்த மற்றும் நீக்க, நாங்கள் டிஜாங்கோ நிர்வாகியைப் பயன்படுத்துவோம்.

குறியீட்டு ஆசிரியர் உள்ள`வலைப்பதிவு/ admin.py`கோப்பைத் திறந்து, அதனுடன் அதன் உள்ளடக்கங்களை மாற்றலாம்:

{% filename%}வலைப்பதிவு/admin.py {%endfilename%}

```python
django.contrib இறக்குமதி நிர்வாகி இருந்து
இருந்து. மோடல்கள் இறக்குமதி போஸ்ட்

admin.site.register (போஸ்ட்)
```

நீங்கள் பார்க்க முடியும் என, நாம் முந்தைய அத்தியாயத்தில் வரையறுக்கப்பட்ட போஸ்ட் மாதிரி (அடங்கும்) இறக்குமதி. நிர்வாகி பக்கத்தில் எங்கள் மாதிரி தெரியும், நாங்கள்`admin.site.register`உடன் மாதிரி பதிவு செய்ய வேண்டும்.

சரி, எங்கள் போஸ்ட் மாதிரி பார்க்க நேரம். Remember to run `python manage.py runserver` in the console to run the web server. உங்கள் உலாவிக்கு சென்று, முகவரி http://127.0.0.1.100000/admin/. இது போன்ற உள்நுழைவுப் பக்கத்தைக் காண்பீர்கள்:

![புகுபதிகை பக்கம்](images/login_page2.png)

உள்நுழைய, நீங்கள் * superuser*உருவாக்க வேண்டும் - தளத்தில் உள்ள எல்லாவற்றையும் கட்டுப்படுத்தும் ஒரு பயனர் கணக்கு. மீண்டும் கட்டளை வரியில் சென்று,`python manage.py createsuperuser`என டைப் செய்து Enter விசையை அழுத்தவும்.

> நினைவில், வலை சேவையகம் இயங்கும் போது புதிய கட்டளைகளை எழுத, ஒரு புதிய முனைய சாளரத்தை திறந்து, உங்கள் விர்ச்சுவல்வாவை செயல்படுத்தவும். ** உங்கள் முதல் டான்ஜோ திட்டம்!**அத்தியாயம், ** வலை சேவையகத்தை**பிரிவில் துவக்க புதிய கட்டளைகளை எப்படி எழுதுவது என்பதை நாங்கள் மதிப்பாய்வு செய்தோம்.

{% filename%} Mac OS X அல்லது Linux: {% endfilename%}

    (myvenv) ~/djangogirls$ python manage.py createsuperuser
    

{% filename %}Windows:{% endfilename %}

    (myvenv) C:\Users\Name\djangogirls> python manage.py createsuperuser
    

கேட்கப்படும் போது, உங்கள் பயனர் பெயர் (ஸ்மால், ஸ்பேஸ் இல்லை), மின்னஞ்சல் முகவரி மற்றும் கடவுச்சொல்லை உள்ளிடவும். **நீங்கள் தட்டச்சு செய்யும் கடவுச்சொல்லைப் பார்க்க முடியாது என்று கவலைப்பட வேண்டாம் - இது எப்படி இருக்க வேண்டும் என்று.**அதை உள்ளிடவும், தொடர `உள்ளிடவும்`அழுத்தவும். வெளியீடு இதைப் போல இருக்க வேண்டும் (பயனர்பெயர் மற்றும் மின்னஞ்சல் உங்கள் சொந்தவையாக இருக்க வேண்டும்):

    பயனர்பெயர்: ஓலா
    மின்னஞ்சல் முகவரி: ola@example.com
    கடவுச்சொல்:
    கடவுச்சொல் (மீண்டும்):
    சூப்பர்ஸர் வெற்றிகரமாக உருவாக்கப்பட்டது.
    

உங்கள் உலாவிக்குத் திரும்புக. நீங்கள் தேர்ந்தெடுத்த சூப்பர்ஸரின் சான்றுகளுடன் உள்நுழைக; நீங்கள் Django நிர்வாக கட்டுப்பாட்டு அறை பார்க்க வேண்டும்.

![டான்ஜோ நிர்வாகி](images/django_admin3.png)

இடுகைகளுக்கு சென்று சிறிது முயற்சி செய். ஐந்து அல்லது ஆறு இடுகைகள் சேர்க்கவும். உள்ளடக்கத்தைப் பற்றி கவலைப்பட வேண்டாம் - இது உங்கள் உள்ளூர் கணினியில் மட்டுமே உங்களுக்கு தெரியும் - நேரம் சேமிக்க இந்த டுடோரியலில் இருந்து சில உரைகளை நகலெடுக்கலாம். :)

குறைந்தபட்சம் இரண்டு அல்லது மூன்று பதிவுகள் (ஆனால் அனைத்தையும் அல்ல) வெளியீட்டு தேதி தொகுப்பு என்பதை உறுதிப்படுத்தவும். இது பின்னர் உதவியாக இருக்கும்.

![டான்ஜோ நிர்வாகி](images/edit_post3.png)

நீங்கள் ஜான் நிர்வாகி பற்றி மேலும் தெரிந்து கொள்ள விரும்பினால், நீங்கள் டிஜாங்கோவின் ஆவணங்களை சரிபார்க்க வேண்டும்: https://docs.djangoproject.com/en/2.0/ref/contrib/admin/

இது ஒரு காபி (அல்லது தேநீர்) அல்லது உங்களை மீண்டும் உற்சாகப்படுத்துவதற்கு சாப்பிட ஏதாவது ஒரு நல்ல தருணமாக இருக்கலாம். நீங்கள் உங்கள் முதல் ஜான்ஜோ மாடலை உருவாக்கிவிட்டீர்கள் - சிறிது இடைவெளி தேவை!