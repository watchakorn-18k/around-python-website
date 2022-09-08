---
title: "การเขียนเว็บไซต์บน Python ด้วย Django 2 (เตรียมเครื่องมือ)"
date:  2022-09-08T21:50:03+07:00
draft: false
author: wk18k
keywords: ['django','python']
tags: ['django','python']
categories: ['django']
weight: 2
---

![](https://cdn.discordapp.com/attachments/585069524445822986/1017447206602674226/unknown.png) 

# เตรียมเครื่องมือ

# ตัวแก้ไขโค้ด

แนะนำว่าใช้ vscode จะสะดวกกว่า สามารถดาวน์โหลดได้ที่ [Download Visual Studio Code - Mac, Linux, Windows](https://code.visualstudio.com/download) 



## Django จำเป็นต้องมี Python

ตรวจสอบว่าระบบของคุณติดตั้ง Python แล้วหรือยังหากยังไม่ได้ติดตั้งสามารถโหลดมาติดตั้งได้ที่ : https://www.python.org/ แนะนำ python เวอร์ชั่น 3.9 ขึ้นไป

## คำสั่งตรวจสอบเวอร์ชั่น Python

```shell
python --version
```

## สร้างโฟลเดอร์ที่จะเก็บโปรเจ็คไว้ก่อน

อาจจะสร้างไว้ใน ไดรฟ์ C หรือ ไดรฟ์ D ก็ได้ หากท่านใช้งานบน Windows หลังจากสร้างโฟลเดอร์เสร็จ สามารถเข้าถึง cmd ได้โดยไม่ต้องใช้คำสั่งอะไรมากมายได้

![](https://media.discordapp.net/attachments/585069524445822986/1017461838994227310/rtset.gif)

## แนะนำให้ใช้ Virtual Environment

เพื่อที่จะได้สามารถลบ Package ได้ตลอดเวลาจะได้ประหยัดพื้นที่ในเครื่อง ใช้คำสั่ง :

Windows :

```shell
py -m venv WEB_DJANGO
```

Unix/MacOS:

```
python -m venv WEB_DJANGO
```

จากนั้นใช้คำสั่งเพื่อเปิดใช้งานคือ :

Windows :

```
WEB_DJANGO\Scripts\activate
```

Unix/MacOS:

```
source WEB_DJANGO/bin/activate
```

![](https://media.discordapp.net/attachments/585069524445822986/1017463291590750270/rtset.gif)

### เมื่อเปิดใช้งานแล้ว คุณจะเห็นผลลัพธ์นี้:

Windows

```
(WEB_DJANGO) C:\Users\Your Name>
```

Unix/MacOS:

```
(WEB_DJANGO) ... $
```

## ติดตั้ง Django

Windows :

```
pip install Django
```

Unix/MacOS:

```
python -m pip install Django
หรือ
python3 -m pip install Django
```

รอจนกระทั่งติดตั้งเสร็จเรียบร้อย 

![](https://cdn.discordapp.com/attachments/585069524445822986/1017463964491329576/rtset.gif)

## ตรวจสอบเวอร์ชั่น Django

```
django-admin --version
```

![](https://cdn.discordapp.com/attachments/585069524445822986/1017463948636860486/unknown.png)

ที่มา : [Django Getting Started](https://www.w3schools.com/django/django_getstarted.php)