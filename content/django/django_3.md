---
title: "การเขียนเว็บไซต์บน Python ด้วย Django 3 (สร้างโปรเจ็ค Django)"
date:  2022-09-08T21:50:03+07:00
draft: false
author: wk18k
keywords: ['django','python']
tags: ['django','python']
categories: ['django']
weight: 3
---

![](https://cdn.discordapp.com/attachments/585069524445822986/1017447206602674226/unknown.png) 

### สร้างโปรเจ็คแรกของคุณ

หากคุณคิดชื่อที่เหมาะสมได้แล้วหรือหากว่ายังไม่ได้ก็ใช้ชื่อ `my_web` ไปก่อนก็ได้จะได้ลดปัญหาคิดชื่อไม่ได้ โดยใช้คำสั่ง:

```
django-admin startproject my_web
```

![](https://cdn.discordapp.com/attachments/585069524445822986/1017466075899764766/rtset.gif)

Django สร้าง `my_web` ข้อมูลในโฟลเดอร์มีดังนี้:

![](https://cdn.discordapp.com/attachments/585069524445822986/1017466681439821834/unknown.png)

### ลุยกันต่อโดยการให้โปรเจ็คทำงาน

ตอนนี้คุณมีโปรเจ็กต์ Django แล้ว ขากนัน้เราจะไปดูว่าหน้าเว็บไซต์มีหน้าตาเป็นยังไงโดยใช้คำสั่ง :

```
python manage.py runserver
หรือ
py manage.py runserver
```

ถ้าหากว่าเรารันตอนนี้จะ error หรือมีข้อผิดพลาด เพราะว่า โปรแกรมหาที่อยู่ของ ไฟล์ manage.py ไม่เจอ เพราะอย่างนั้นเราจะต้องเข้าไปในโฟลเดอร์ `my_web` ก่อนถึงจะสามารถใช้คำสั่งด้านบน โดยสามารถใช้วิธี 2 วิธีเหมือนในรูปภาพด้านล่างนี้ได้ แต่แนะนำให้ใช้แบบที่ 2

![](https://cdn.discordapp.com/attachments/585069524445822986/1017468172435214346/rtset.gif)

จากนั้นใช้คำสั่งอีกรอบ:

```
python manage.py runserver
หรือ
py manage.py runserver
```

ก็จะได้เว็บไซต์มา โดยให้เราไปที่ url `http://127.0.0.1:8000/`

![](https://cdn.discordapp.com/attachments/585069524445822986/1017469227726291044/rtset.gif)

ในการหยุดเซิฟเวอร์ ให้กด CTRL+ C หรือทำการหยุดเซิฟเวอร์

ที่มา : [Django Create Project](https://www.w3schools.com/django/django_create_project.php)