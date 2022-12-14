---
title: "บทที่ 2 ตัวแปร"
date: 2022-08-19T06:47:40+07:00
draft: flase
language: "ไทย"
keywords: ['Python']
tags: ['การเขียนภาษาโปรแกรม Python พื้นฐาน']
categories: ['สอนเขียนโปรแกรม']
weight: 2
---

## ทำความเข้าใจเกี่ยวกับตัวแปร

### นิยามของตัวแปร

    คำว่าตัวแปรเรามักได้ยินมาจากในที่หลายๆแหล่ง ตัวอย่างเช่น เขาคือตัวแปรสำคัญ หรือ ตัวแปร X มีค่าเท่ากับ 10

### ตัวแปรในโลกของการเขียนโปรแกรม

    จะหมายถึง สิ่งที่ใช้แทนสิ่งหนึ่งโดยไม่จำเป็นจะต้องเป็นตัวเลขเสมอไป ตัวอย่างเช่น

        - นาย A เดินไปหา นาย B

    ในตัวอย่างข้างต้นเราอาจจะให้นาย A มีชื่อว่า สมชาย ส่วนนาย B มีชื่อ สมัย ดังนั้นประโยคข้างต้นจะเปลี่ยนใหม่เป็น

        - นาย สมชาย เดินไปหา นาย สมัย

### ตัวอย่างการสร้างตัวแปร

    หรือระบุตัวแปรขึ้นมา ใน Python นั้นการสร้างตัวแปรจะตัวมีชื่อตัวแปร จากนั้นก็ตามด้วย ค่า หรือ ข้อมูล ที่จะเพิ่มลงไปในตัวแปรนั้นๆ เช่น

        X = 50

        X คือ ชื่อตัวแปร

        50 คือ ค่า หรือ ข้อมูล ของตัวแปร

    สังเกตว่าจะหลัง X มีเครื่องหมายเท่ากับ (=) อยู่ เพราะว่า เราจะใช้เครื่องหมายเท่ากับ (=) เป็นตัวเชื่อมระหว่างตัวแปรกับค่าของตัวแปรนั้นๆ

### สามารถใช้ภาษาไทยได้

    แต่ไม่แนะนำเพราะอาจจะมีปัญหาเรื่องของตัวสระบางทำให้เกิดข้อผิดพลาดได้ ตัวอย่างเช่น

           น้ำ = แม่น้ำสายหลัก

    ปัญหาก็คือคำว่า น้ำ มีสระ อำ และ ไม้โท อาจจะยุ่งยากในการนำไปใช้งาน จึงแนะนำให้ใช้ภาษาอังกฤษที่เป็นคำศัพท์ หรือ คำกริยา ว่ากำลังทำอะไร ตัวอย่างเช่น

            water = แม่น้ำสายหลัก (ถ้าเป็นอย่างนี้แล้วจะดูอ่านง่ายกว่าเดิม)

    และที่สำคัญชื่อตัวแปรที่สร้างนั้นไม่ควรซ้ำกัน เพราะหากซ้ำกันค่าของตัวแปรจะเปลี่ยนไป เช่น

            water = แม่น้ำสายหลัก

            water = น้ำ

    ตัวแปร water จะมีค่าเท่ากับ น้ำ

## ประเภทของตัวแปรทั่วไป

    ตัวแปร ที่ใช้ทั่วไปในโลกของการเขียนโปรแกรมจะแบ่งประเภทคราวๆเป็นดังนี้

- ### ตัวแปรประเภท ข้อความ
  
  - สามารถระบุ ชื่อ คน สัตว์ สิ่งของ ตัวอักษร รวมถึงข้อความทุกประเภท ที่ไม่ได้ใช้ในการคำนวณทางคณิตศาตร์ หรือก็คือไม่ใช้ในการหาผลลัพธ์จากการ บวก ลบ คูณ หาร

- ### ตัวแปรประเภท ตัวเลข
  
  - สามารถระบุ แค่ตัวเลข **เท่านั้น** ตัวชื่อ เพราะตัวแปรประเภทตัวเลขจะนำไปใช้ในการหาผลลัพธ์ทางการคำนวณ

- ### ตัวแปรประเภท บูลีน หรือ บูล
  
  - คือข้อมูลที่ จริง กับ ไม่จริง หรือ true (ทรู) กับ false (ฟอลส) จะใช้ในการเปรียบเทียบเช่น 1 เท่ากับ 1 จริงหรือไม่จริง

## ประเภทของตัวแปรใน Python

    ประเภทตัวแปรใน Python ก็จะคล้ายๆกับ ประเภทตัวแปรข้างต้น แต่อาจจะมีชื่อพิเศษที่ใช้เรียกดังนี้

#### สตริง (string)

- สตริง (string) มีตัวย่อคือ **str** คือ ตัวแปรประเภทข้อความ ซึ่งประเภทตัวแปรนี้จะพิเศษกว่าตัวแปรอื่น เพราะว่าจะต้องมีเครื่องหมายบางเครื่องหมายระบุก่อน นั้นก็คือ
  
  - เครื่องหมายซิงเกิ้ลโขด (single quotes) โดยมีหน้าตาคือ <mark>'   '</mark>
  
  - เครื่องหมายดับเบิ้ลโขด (double quotes) โดยมีหน้าตาคือ <mark>"    "</mark>

- ตัวอย่างการใช้งานเช่น

```python
water = "แม่น้ำสายหลัก"

oil = 'น้ำมันพืช'
```

#### อินทีเจ้อ (integer)

- อินทีเจ้อ (integer) มีตัวย่อคือ **int** คือ ตัวแปรประเภทตัวเลขจำนวนเต็ม ความหมายของจำนวนเต็มก็คือ จำนวนที่เป็นจำนวนนับ หรือจะเป็น จำนวนนับที่ติดลบ หรือศูนย์

- ตัวอย่างการใช้งานเช่น

```python
one = 50

two = 200
```

#### โฟลท (float)

- โฟลท (float) **ไม่มีตัวย่อ** คือ ตัวแปรประเภทตัวเลขทศนิยม จำนวนที่เขียนในรูปทศนิยมจะมีจุด (**.**) หรือภาษาอังกฤษเรียกว่า dot (ดอท) หรือ point (พ้อย)

- ตัวอย่างการใช้งานเช่น

#### บูล (bool)

- บูล (bool) **ไม่มีตัวย่อ** คือ ตัวแปรประเภทจริงหรือเท็จ true กับ false

- ตัวอย่างการใช้งานเช่น

```python
is_walk = true

is_walk = false
```

#### ลิสต์ (list)

- ลิสต์ (list) **ไม่มีตัวย่อ** คือ ตัวแปรประเภทรายการ หรือชุดข้อมูล ซึ่งสามารถมีค่ามากกว่า 1 หรือเท่ากับ 1 ก็ได้ โดยมีเครื่องหมายพิเศษ นั่นก็คือ
  
  - เครื่องหมายวงเล็บรูปเหลี่ยม (square brackets) โดยมีหน้าตาคือ <mark>[   ]</mark>

- ตัวอย่างการใช้งานเช่น

```python
list1 = [1,2,3,4,5,6,7,8,9]

list_name = ["สมัย","สมชาย","สมอน"]
```

> หากต้องการเพิ่มจำนวนข้อมูลในลิสต์สามารถใช้เครื่องหมายลูกน้ำ (,) เป็นตัวคั่นระหว่างข้อมูลได้

#### ดิกชั่นนารี (Dictionary)

- ดิกชั่นนารี (Dictionary) **ตัวย่อคือ** dict คือตัวแปรที่คล้ายๆกับลิสต์ แต่แตกต่างตรงที่ จะต้องระบุคีย์ (Key) กับ ค่าข้อมูล (Value อ่านว่า แวลูว)
  
  - โดยมีเครื่องหมายโคลอน (:) เป็นตัวเชื่อมกัน และมีเครื่องหมายปีกกา <mark>{   }</mark> ครอบมัน

- ตัวอย่างโครงสร้าง

```js
{key : value}
```

- ตัวอย่างการใช้งานเช่น

```python
dict1 = { "ชื่อ" : "สมัย" , "อายุ" : 28 , "โสด", true }
```

- > หากต้องการเพิ่มจำนวนข้อมูลสามารถใช้เครื่องหมายลูกน้ำ (,) เป็นตัวคั่นระหว่างข้อมูลได้

    ประเภทตัวแปรใน Python ที่ยกตัวอย่างมาข้างต้น เป็นเพียงแค่ตัวแปรคร่าวๆ ที่นิยมใช้ส่วนอื่นสามารถศึกษาเพิ่มเติมได้ในอินเตอร์เน็ต