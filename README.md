# CodeMobile Challenge

## สร้างโปรเจค C# WPF MVVM

<b>1. สร้าง Route ขึ้นมา 3 Page</b>
 - Login Page
 - Home Page
 - Detail Page

<b>2. ค่าเริ่มต้น Redirect มาหน้า Login Page</b>

<b>3. หน้า Login Page มี UI ดังนี้</b>

3.1 ช่อง input Email  

3.2 ช่อง input Password  

3.3 ปุ่มเข้าสู่ระบบ
  
3.4 เพิ่ม Validation

- ตรวจสอบ Format Email โดยใช้ Regex
- ตรวจสอบความรหัสผ่าน ความยาว 8 ตัวขึ้นไป
  
3.5 เมื่อกดปุ่มเข้าสู่ระบบ ตรวจสอบ Email = aa@bb.cc และ Password = 12345678 

        - ถ้าถูกต้อง Redirect ไปหน้า Home Page
         
        - ถ้าผิดให้ Alert ข้อความ "Email or password incorrect"

<b>4. หน้า Home Page มีเงื่อนไขตามนี้</b>

4.1 fetch ข้อมูล GET: https://dummyjson.com/products

4.2 แปลงข้อมูล JSON ข้อ 4.1 เป็น Class (ชื่อ Product) 

4.3 แสดงข้อมูลที่ fetch ได้เป็น Table แบบ Virtualizing มี Column ดังนี้
  - Thumbnail
  - Title
  - Price
  - Stock
  - ปุ่ม Detail

4.4 เมือกดปุ่ม Detail ให้ส่ง id product ผ่าน parameters ไปหน้า Detail Page
 
<b>5. เพิ่ม input ช่องค้นหาข้อมูลสินค้า ค้นหาชื่อสินค้าแบบ Debound Time(1 วินาที) และ contain string ในหน้า Home Page</b>

<b>6. เพิ่มปุ่ม Dropdown 5 เมนู ในหน้า Home Page เพื่อเปลี่ยนแปลงค่า Product array</b>
  - ทั้งหมด (แสดงสินค้าทั้งหมด)
  - ราคามากว่า 1000 (กรองสินค้าที่มีราคา 1000 ขึ้นไป และมี %ส่วนลด มากกว่า 0)  
  - แสดงราคารวมต่อชิ้น (เพิ่ม Column ขึ้นมาอีก 1 Column สำหรับแสดง ราคารวมต่อชิ้น) [เพิ่ม key totalPrice เข้าไปใน Class Product เพื่อแสดงใน column]
  - เรียงเรตติ้ง (เรียง rating สินค้าแบบ desc และ price แบบ asc)  
  - แสดงราคารวมทั้งหมด (คำนวนราคาสินค้าทั้งหมด ของ array สินค้า) [เพิ่ม Label ราคารวม ไว้เป็น Footer Table]
 
<b>7. หน้า Detail Page</b>

7.1 Get id product จาก parameters และ fetch ข้อมูลสินค้า GET:https://dummyjson.com/products/:id   

7.2 แสดงข้อมูลสินค้า ตามสวยงาม
  - Images 150*150
  - Title
  - Price
  - Stock
 
<b>8. เพิ่ม Interceptor http นำมาใช้กับหน้า Home Page</b>

8.1 Add header key CMReq = “request” ตอน Request http

8.2 Add header key CMERes = “response” ตอน Response http
  
