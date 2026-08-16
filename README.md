# Mactile (MVP) — แพลตฟอร์มบริหารจัดการจองคิวและการเข้าถึงเครื่องรีโมท
> **กลุ่มที่ 4** | โครงการพัฒนาระบบบริหารจัดการคิวและรีเซ็ตสภาพแวดล้อมเครื่องรีโมทอัตโนมัติ

---

## 📖 สารบัญเอกสารโครงการ (Documentation Index)

| เอกสาร | รายละเอียด | ลิงก์ |
| :--- | :--- | :---: |
| **1. Project Charter** | ข้อเสนอโครงการ, วัตถุประสงค์, ขอบเขต MVP 4 เสาหลัก, แผนงาน และความเสี่ยง | [project_charter.md](./docs/project_charter.md) |
| **2. Software Requirements (SRS)** | ข้อกำหนดเชิงหน้าที่ (FR-1 ถึง FR-4), NFR, Sequence Diagram, และโมเดลสิทธิ์ | [Requirement_specification.md](./docs/Requirement_specification.md) |
| **3. Acceptance Criteria & UAT** | เกณฑ์การตรวจรับระบบรูปแบบ Gherkin (Given-When-Then), Checklists, และ Sign-off Matrix | [Acceptance_criteria.md](./docs/Acceptance_criteria.md) |
| **4. Database Design** | โครงสร้างฐานข้อมูล PostgreSQL, Entity-Relationship Diagram (ERD), Data Dictionary และ SQL DDL Scripts | [database_design.md](./docs/database_design.md) |

---

## 🚀 ฟังก์ชันหลักของระบบ (Core MVP Features)

1. **ระบบจองคิวและการเข้าถึง (Queue Booking & Access Management):**
   - ตาราง Slot เวลา, การจำกัดสิทธิ์ตามเวลา (Time-based Access Control), การนับเวลาถอยหลัง และการขอต่อเวลา/คืนเครื่องก่อนกำหนด
2. **ระบบจัดการและรีเซ็ตสภาพแวดล้อมเบื้องต้น (Environment Management & Basic Reset):**
   - Host Agent Daemon พร้อมระบบ Heartbeat, สคริปต์ล้างไฟล์/แคช/Process ตกค้าง และระบบตรวจสอบความพร้อมหลังรีเซ็ต (Health Check) ภายใน 60 วินาที
3. **การเชื่อมต่อรีโมทด้วยโปรแกรมสำเร็จรูป (Remote Connection Integration):**
   - รองรับโปรแกรมรีโมทสำเร็จรูป (RustDesk, VNC, RDP, AnyDesk, SSH) พร้อมแจกจ่าย One-time Credential และสุ่มเปลี่ยนรหัสผ่านทุกรอบการใช้งาน
4. **หน้า Dashboard ผู้ดูแลระบบ (Admin Dashboard):**
   - ตรวจสอบสถานะเครื่อง Fleet แบบ Real-time, ระบบควบคุมฉุกเฉิน (Force Disconnect / Force Reset / Maintenance Mode) และ Audit Logs

---

## 🛠️ โครงสร้างไฟล์ในโครงการ (Project Structure)

```text
LAB-DOC/
├── README.md                          # ภาพรวมโครงการและสารบัญเอกสาร
└── docs/
    ├── project_charter.md             # เอกสารข้อเสนอโครงการ
    ├── Requirement_specification.md   # ข้อกำหนดความต้องการของระบบ (SRS)
    ├── Acceptance_criteria.md         # เกณฑ์การยอมรับและการตรวจรับระบบ (UAT)
    └── database_design.md             # การออกแบบฐานข้อมูลและสคริปต์ SQL DDL
```
