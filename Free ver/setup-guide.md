# 🎨 Setup Guide - Logo & Donation

## 📦 ไฟล์ที่ต้องเตรียม

### 1. Logo (logo.png)
- **ขนาด:** 320x320 พิกเซล
- **ชื่อไฟล์:** `logo.png`
- **ตำแหน่ง:** วางไฟล์ในโฟลเดอร์เดียวกับ index.html

**หน้าที่แสดง:**
- ✅ index.html - ขนาด 320x320px (หน้าแรก)
- ✅ lucky-draw.html - ขนาด 120x120px (Desktop)
- ✅ lucky-draw.html (mobile) - ขนาด 80x80px

**กรณีไม่มีไฟล์:**
- จะแสดง emoji 🎰 แทน
- ระบบทำงานได้ปกติ

---

### 2. QR Code สำหรับรับบริจาค (qr-code.png)
- **ชื่อไฟล์:** `qr-code.png`
- **ตำแหน่ง:** วางไฟล์ในโฟลเดอร์เดียวกับ donate.html
- **ขนาดแนะนำ:** 300x300 พิกเซล ขึ้นไป

**หน้าที่แสดง:**
- ✅ donate.html - แสดงในกรอบ 300x300px

**กรณีไม่มีไฟล์:**
- จะแสดง placeholder พร้อมคำแนะนำ
- ยังสามารถใช้เลขบัญชีธนาคารได้

---

## 🏦 ตั้งค่าข้อมูลบัญชีธนาคาร

แก้ไขไฟล์ `donate.html` ที่บรรทัด:

### Bank 1 (กสิกรไทย)
```html
<div class="bank-name">ธนาคารกสิกรไทย</div>
<div class="account-number" id="account1">XXX-X-XXXXX-X</div>
<div class="account-name">ชื่อบัญชี: [ใส่ชื่อของคุณ]</div>
```

**แก้เป็น:**
```html
<div class="bank-name">ธนาคารกสิกรไทย</div>
<div class="account-number" id="account1">123-4-56789-0</div>
<div class="account-name">ชื่อบัญชี: นายทดสอบ ระบบ</div>
```

### Bank 2 (ไทยพาณิชย์)
```html
<div class="bank-name">ธนาคารไทยพาณิชย์</div>
<div class="account-number" id="account2">XXX-X-XXXXX-X</div>
<div class="account-name">ชื่อบัญชี: [ใส่ชื่อของคุณ]</div>
```

---

## ➕ เพิ่มบัญชีธนาคารเพิ่มเติม

คัดลอกโค้ดนี้ไปใส่หลังจาก Bank 2:

```html
<!-- Bank 3 -->
<div class="bank-item">
    <div class="bank-icon">🏦</div>
    <div class="bank-details">
        <div class="bank-name">ธนาคารกรุงเทพ</div>
        <div class="account-number" id="account3">XXX-X-XXXXX-X</div>
        <div class="account-name">ชื่อบัญชี: [ใส่ชื่อของคุณ]</div>
    </div>
    <button class="copy-btn" onclick="copyAccount('account3')">📋 คัดลอก</button>
</div>
```

---

## 🎨 เปลี่ยนสี Background

### Index.html & Lucky Draw
ปัจจุบันใช้ **Black-Gray Gradient**

**แก้ไข Background:**
```css
body {
    background: linear-gradient(135deg, #1a1a1a 0%, #4a4a4a 100%);
}
```

**ตัวอย่างสีอื่นๆ:**
```css
/* สีม่วง-ชมพู */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* สีน้ำเงิน-เขียว */
background: linear-gradient(135deg, #11998e 0%, #38ef7d 100%);

/* สีส้ม-แดง */
background: linear-gradient(135deg, #ff6b6b 0%, #ee5a6f 100%);

/* สีทอง */
background: linear-gradient(135deg, #f7971e 0%, #ffd200 100%);
```

---

## 📂 โครงสร้างไฟล์

```
📦 Lucky Draw System/
├── 🖼️ logo.png (320x320px) - โลโก้หลัก
├── 📱 qr-code.png (300x300+) - QR Code รับเงิน
│
├── 🖥️ Desktop Version/
│   ├── index.html
│   ├── lucky-draw.html
│   └── donate.html
│
└── 📱 Mobile Version/
    ├── index.html
    ├── lucky-draw.html
    └── donate.html
```

---

## ✨ ฟีเจอร์ของหน้า Donate

### 1. QR Code
- แสดง QR Code สำหรับสแกนจ่ายเงิน
- รองรับ PromptPay, QR บัตรเครดิต

### 2. คัดลอกเลขบัญชี
- กดปุ่ม "📋 คัดลอก" เพื่อคัดลอกเลขบัญชี
- แสดงการแจ้งเตือน "✅ คัดลอกแล้ว!"

### 3. Responsive Design
- ใช้งานได้ทั้ง Desktop และ Mobile
- ปรับขนาดอัตโนมัติ

---

## 🔧 การทดสอบ

### ทดสอบ Logo
1. เปิด index.html
2. ตรวจสอบว่า logo แสดงหรือไม่
3. ถ้าไม่แสดง → ตรวจสอบชื่อไฟล์ว่าเป็น `logo.png`

### ทดสอบ Donate Page
1. เปิด donate.html
2. ตรวจสอบ QR Code แสดงหรือไม่
3. ทดสอบปุ่มคัดลอกเลขบัญชี
4. ทดสอบลิงก์กลับหน้าแรก

---

## 📱 Mobile Version

ไฟล์ใน `/mobile-version/` มีการตั้งค่าเหมือนกับ Desktop Version
- ใช้ logo.png เดียวกัน
- ใช้ qr-code.png เดียวกัน
- ใช้ donate.html เดียวกัน

---

## 🎯 Checklist

- [ ] เตรียม logo.png (320x320px)
- [ ] เตรียม qr-code.png (300x300px+)
- [ ] แก้ไขเลขบัญชีธนาคารใน donate.html
- [ ] แก้ไขชื่อบัญชีใน donate.html
- [ ] ทดสอบการแสดงผลบน Desktop
- [ ] ทดสอบการแสดงผลบน Mobile
- [ ] ทดสอบปุ่มคัดลอกเลขบัญชี
- [ ] ทดสอบลิงก์ Buy me a coffee

---

## 💡 เคล็ดลับ

1. **Logo ไม่แสดง?**
   - ตรวจสอบชื่อไฟล์ต้องเป็น `logo.png` (ตัวพิมพ์เล็กทั้งหมด)
   - วางไฟล์ในโฟลเดอร์เดียวกับ HTML

2. **QR Code ไม่แสดง?**
   - ตรวจสอบชื่อไฟล์ต้องเป็น `qr-code.png`
   - ทดสอบเปิดรูปโดยตรงว่าเสียหรือไม่

3. **ต้องการเปลี่ยน Copyright?**
   - ค้นหา "2024 natto109©. All Rights Reserved."
   - แก้ไขเป็นชื่อของคุณ

---

**Created by:** natto109  
**Version:** 1.0  
**Last Updated:** 2024