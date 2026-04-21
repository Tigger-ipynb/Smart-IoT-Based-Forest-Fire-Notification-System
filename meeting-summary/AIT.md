## **Meeting Summary: Smart IoT-Based Forest Fire Notification System**

### 1. **Stakeholders & Roles**

* **KU (Kasetsart University)**
  รับผิดชอบด้าน Data Analysis และการพัฒนาโมเดล
* **AIT (intERLab)**
  ดูแล IoT Infrastructure และ System Integration
* **Funding Source**
  โครงการเกี่ยวกับฝุ่น PM2.5 และไฟป่า

---

### 2. **System**

**Architecture:**

* Sensor → LoRaWAN → Data Collection

**Key Characteristics:**

* ใช้ LoRaWAN

  * ข้อดี: ส่งข้อมูลได้ไกล (~5 km), ใช้อินเทอร์เน็ตต่ำ
  * ข้อเสีย: Accuracy ต่ำ
* Sensor ปัจจุบัน:

  * วัดได้หลัก ๆ แค่ PM2.5

**Limitations:**

* ความแม่นยำต่ำ
* Feature ของข้อมูลน้อย
* Coverage ยังไม่ครอบคลุมพื้นที่ป่าลึก

---

### 3. **Project Objectives**

1. พัฒนา IoT System ให้มีเสถียรภาพและขยายได้
2. เพิ่ม Accuracy ของข้อมูล
3. ขยาย Sensor Coverage ให้ครอบคลุมพื้นที่มากขึ้น
4. พัฒนาระบบตรวจจับและระบุตำแหน่งไฟป่า (Fire Detection & Tracking)

---

### 4. **Monitoring Approach**

**Stationary Monitoring (Micro-sensors):**

* ติดตั้ง sensor ประจำจุด
* ตัวแปรที่ต้องการ:

  * PM2.5
  * Wind (ความเร็วและทิศทางลม)
  * Sensor housing / protection 
  * อาจมีการติด IOT กับหมวกกันน็อคชาวน็อค

---

### 5. **Data & Modeling**

**Current Data:**

* PM2.5 เป็นหลัก

**Goal:**

* พัฒนา Decision Tree หรือ ML Model ที่แม่นยำขึ้น
* เพิ่ม feature เช่น:

  * ลม
  * ตำแหน่ง (location)
  * เวลา (temporal data)

**Future Capability:**

* วิเคราะห์ย้อนหลังเพื่อ:

  * หาแหล่งกำเนิดไฟป่า
  * วิเคราะห์การกระจายของควัน

---

### 6. **Current Status & Next Steps**

* Real data จะเริ่มมีในปีหน้า

**Tasks ปัจจุบัน:**

1. ออกแบบระบบ IoT ให้รองรับการขยาย
2. วางแผนการติดตั้ง sensor
3. เตรียม data pipeline
4. เริ่มพัฒนา/ทดสอบโมเดลจาก simulated หรือ historical data

---

### 7. **Key Challenges**

* ข้อมูลยังไม่หลากหลาย
* การติดตั้งในพื้นที่ป่า (พลังงาน, สัญญาณ, maintenance)
* ข้อจำกัดของ LoRaWAN:

  * ระยะไกล
  * แต่ bandwidth ต่ำและมี noise

---

### 8. **Recommendations**

* เพิ่ม sensor data :

  * Temperature
  * Humidity
  * Gas (CO, CO₂)
* ใช้ sensor fusion แทนการพึ่ง PM2.5 อย่างเดียว
* รวมข้อมูลจากแหล่งอื่น เช่น satellite (ถ้ามี)
* ใช้ model ที่มีประสิทธิภาพมากขึ้น:

  * Random Forest
  * Gradient Boosting
* ใช้ spatial analysis เพื่อช่วยระบุตำแหน่งต้นกำเนิดไฟ

---