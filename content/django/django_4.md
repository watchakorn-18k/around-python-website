---
title: "การเขียนเว็บไซต์บน Python ด้วย Django 4 (สร้างแอป Django)"
date:  2022-09-08T21:50:03+07:00
draft: false
author: wk18k
keywords: ['django','python']
tags: ['django','python']
categories: ['django']
weight: 4
---

![](https://cdn.discordapp.com/attachments/585069524445822986/1017447206602674226/unknown.png) 

### แอปคืออะไร

แอปคือเว็บแอปพลิเคชันที่มีความหมายเฉพาะเจาะจงในโครงการของคุณ เช่น หน้าแรก หน้าแบบฟอร์มติดต่อ หรือหน้าแสดงข้อมูลสมาชิก และอื่นๆ ซึ่งจะสร้างอะไรก็ได้ แต่ตัวอย่างนี้ เราจะสร้างแอพที่ช่วยให้เราสามารถแสดงรายการและลงทะเบียนสมาชิกลงในฐานข้อมูล

แต่ก่อนอื่น เรามาสร้างแอป Django ง่ายๆ ที่แสดงคำว่า "สวัสดีชาวโลก" กันก่อนแล้วกัน



## สร้างแอพ

ขอตั้งชื่อแอปว่า `members`

ก่อนจะสร้างอย่าลืมหยุดเซิฟเวอร์ก่อน จากนัน้ใช้คำสั่ง

```
py manage.py startapp members
หรือ
python manage.py startapp members
```

![](https://cdn.discordapp.com/attachments/585069524445822986/1017471906963800234/rtset.gif)

เป็นอันจบการสร้างแอพ

ที่มา : [Django Create App](https://www.w3schools.com/django/django_create_app.php)