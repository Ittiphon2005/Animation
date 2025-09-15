# Animation
# 2D Platformer Game Project

**เวอร์ชัน Unity:** 6.1.0f1  
**ประเภทเกม:** 2D Platformer  

## คำอธิบายโปรเจกต์
โปรเจกต์นี้เป็นเกม 2D Platformer ที่ผู้เล่นควบคุมตัวละครหลักเพื่อเดินและกระโดดหลบสิ่งกีดขวาง ตัวละครมีแอนิเมชันการเคลื่อนไหวหลายแบบ ได้แก่:

- ยืน (Idle)
- เดินหน้าและเดินถอยหลัง (Walk/Run)
- กระโดด (Jump)
- บาดเจ็บ (Hurt)
- ตาย (Death/Stop Movement)

## การออกแบบและการทำงาน

### ฉากเกม
- ถูกสร้างด้วย **Tilemap 2D** สำหรับพื้น, ผนัง และสิ่งกีดขวาง
- เพิ่มความสะดวกในการออกแบบและจัดวางฉาก

### ตัวละครหลัก
- ใช้ **Sprite 2D** พร้อม:
  - `Rigidbody 2D` สำหรับฟิสิกส์
  - `Capsule Collider 2D` สำหรับตรวจจับการชน
  - `Animator` สำหรับจัดการแอนิเมชันต่าง ๆ

### การบังคับ
ใช้ **Input System** โดยมีการควบคุมดังนี้:

| ปุ่ม | การกระทำ |
|------|-----------|
| D    | เดินไปขวา |
| A    | เดินไปซ้าย |
| Space| กระโดด |

### สคริปต์
- `GatherInput` – รับข้อมูลการกดปุ่มจากผู้เล่น
- `PlayerMoveControls` – จัดการการเคลื่อนไหวและแอนิเมชันของตัวละคร

### กลไกเกม
- ตัวละครจะบาดเจ็บเมื่อชนสิ่งกีดขวาง
- หากบาดเจ็บ **2 ครั้ง** เกมจะถือว่า **ตัวละครตาย/เกมจบ**
- การตายจะหยุดการเคลื่อนไหวและแสดงแอนิเมชันตาย

ภาพเดินหน้า
<img width="937" height="473" alt="image" src="https://github.com/user-attachments/assets/d46422de-68e9-43a3-9969-3ab3429d74e1" />

ภาพถอยหลัง
<img width="947" height="466" alt="image" src="https://github.com/user-attachments/assets/4441b64d-59d8-48c0-8258-ba5859b8a41f" />

ภาพกระโดด
<img width="937" height="463" alt="image" src="https://github.com/user-attachments/assets/230d4e4f-6658-4e87-b0eb-947f1051827c" />

ภาพได้รับบาดเจ็บ
<img width="942" height="467" alt="image" src="https://github.com/user-attachments/assets/55947c3b-5e51-45e8-a7f2-8bc6dfb288c1" />

ภาพตาย(หยุดการเคลื่อนไหว)
<img width="937" height="461" alt="image" src="https://github.com/user-attachments/assets/c6208879-a095-4111-baa0-ddc189a89207" />



## สรุป
โปรเจกต์นี้เป็นตัวอย่างของการสร้างเกม 2D Platformer โดยใช้ Unity พร้อมระบบฟิสิกส์และแอนิเมชันพื้นฐาน รวมถึงกลไกการบาดเจ็บและการตายของตัวละคร
