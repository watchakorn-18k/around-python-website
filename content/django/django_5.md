---
title: "การเขียนเว็บไซต์บน Python ด้วย Django 5 (Views(วิว) ใน Django)"
date:  2022-09-08T21:50:03+07:00
draft: false
author: wk18k
keywords: ['django','python']
tags: ['django','python']
categories: ['django']
weight: 5
---

![](https://cdn.discordapp.com/attachments/585069524445822986/1017447206602674226/unknown.png) 

### Views(วิว)

Views Django เป็นฟังก์ชันใน Python ที่รับคำขอ http และส่งคืนค่า http ตอบกลับ เช่นเอกสาร HTML

หน้าเว็บที่ใช้ Django เต็มไปด้วย Views ที่จะมีงาน และภารกิจที่แตกต่างกันออกไป

โดยปกติแล้ว Views จะใส่ไว้ในไฟล์ชื่อ`views.py`ที่อยู่ในโฟลเดอร์ของแอปที่สร้างขึ้น

อย่างเช่น `views.py` อยู่ในโฟลเดอร์ `members`ของคุณที่มีลักษณะดังนี้:

`members/views.py`:

```python
from django.shortcuts import render

# Create your views here.
```

อธิบายเพิ่มเติมนิดหน่อย `from django.shortcuts import render` คือ การเรียก render() มาใช้งาน render() คือการรวมเทมเพลตมาใช้งานแล้วแสดงผลกลับ อ่านเพิ่มเติมได้ที่ [Django shortcut functions | Django documentation | Django](https://docs.djangoproject.com/en/4.1/topics/http/shortcuts/)

![](https://cdn.discordapp.com/attachments/585069524445822986/1017473806509559879/unknown.png)

หลังจากได้เจอแล้วใส่คำสั่งนี้ไปแทนที่ได้เลย :

`members/views.py`:

```python
from django.shortcuts import render
from django.http import HttpResponse

def index(request):
    return HttpResponse("สวัสดีชาวโลก")
```

อธิบายเพิ่มเติมนิดหน่อย `from django.http import HttpResponse` คือ การเรียก HttpResponse() มาใช้งาน HttpResponse() คือเมื่อมีคำขอหน้า Django จะทำการสร้างวัตถุ HttpReques ที่มีข้อมูลเมตาเกี่ยวกับคำขอ จากนั้น Django จะโหลด Views ที่เหมาะสม โดยส่งผ่านอาร์กิวเมนต์แรกของ HttpRequest ไปยังฟังก์ชัน Views แต่ละ Views มีหน้าที่ในการส่งวัตถุ HttpResponse คืนกลับ อ่านเพิ่มที่ : [Request and response objects | Django documentation | Django](https://docs.djangoproject.com/en/4.1/ref/request-response/)

![](https://cdn.discordapp.com/attachments/585069524445822986/1017476581414932520/unknown.png)

นี่เป็นตัวอย่างง่ายๆ เกี่ยวกับวิธีการส่งคำตอบกลับไปยังเบราว์เซอร์

แต่เราจะแสดงผลที่เราเขียน Views ได้ยังไงหล่ะ เราจะต้องเรียก Views ผ่าน URL

## URLs

เมื่อผู้ใช้ส่งคำขอ URL มาจากนั้น Django จะตัดสินใจว่าจะส่งไป ที่ *Views* ต่างๆ

โดยให้สร้างไฟล์ที่มีชื่อว่า `urls.py` โดยให้อยู่อยู่ในโฟลเดอร์เดียวกับ `views.py`ไฟล์ แล้วพิมพ์โค้ดนี้ลงไป:

`members/urls.py`:

```python
from django.urls import path
from . import views

urlpatterns = [
    path('', views.index, name='index'),
]
```

![](https://cdn.discordapp.com/attachments/585069524445822986/1017482683422605353/unknown.png)

จากนั้นไปที่โฟลเดอร์ `my_web` ซึ่งอาจจะงงเพราะ my_web มีสองอัน เลือกอันที่สองที่ไม่ใช่อันแรกที่สร้าง อาจจะงงคอยดูรูปดีกว่า โดยไปแทนที่ไฟล์ในนั้นด้วยคำสั่งนี้ :

`my_web/urls.py`:

```python
from django.contrib import admin
from django.urls import include, path

urlpatterns = [
    path('members/', include('members.urls')),
    path('admin/', admin.site.urls),
]
```

`from django.contrib import admin` คือที่อยู่ของหน้าสำหรับ แอดมิน

`from django.urls import include, path` 

path() คือระบบเส้นทาง

include() คือตำแหน่งไฟล์ Views ของ แอป members

`path(' ชื่อเส้นทาง url ', include('ชื่อแอปที่สร้าง.urls')`

![](https://cdn.discordapp.com/attachments/585069524445822986/1017479691243900998/unknown.png)

จากนั้นรันเซิฟเวอร์ ด้วยคำสั่งนี้ (อย่าลืมทุกอย่างด้วยนะไม่งั้น error):

```
py manage.py runserver
```

ในหน้าต่างเบราว์เซอร์ ให้พิมพ์`[127.0.0.1:8000/members/](http://127.0.0.1:8000/members/)`ในแถบที่อยู่

ที่มา : [Django Views](https://www.w3schools.com/django/django_views.php)