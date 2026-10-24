# 👗 ClosetLoop - Sustainable Fashion & AI Wardrobe Platform

**ClosetLoop** แพลตฟอร์มจัดการตู้เสื้อผ้าดิจิทัล (Digital Wardrobe) และตลาดกลางซื้อขายเสื้อผ้ามือสอง (Pre-loved Marketplace) พร้อมระบบ **AI Outfit Curator** ช่วยคิวเรตและจับคู่ลุคการแต่งตัวตามสไตล์ สภาพอากาศ และโอกาสใช้งาน ภายใต้แนวคิดแฟชั่นหมุนเวียนที่ยั่งยืน (Circular & Sustainable Fashion)

---

## 👥 ผู้จัดทำโครงการ (Team Members)

* **67160385** นางสาวอัญชิสา นิยมชัย
* **67160354** นางสาวปาณิศา วงศ์รัตนสังวร

---

## ✨ ฟีเจอร์หลักของระบบ (Key Features)

* 📊 **Overview Dashboard:** สรุปภาพรวมตู้เสื้อผ้า สถิติการใช้งาน และรายการสินค้าใหม่ในตลาดแฟชั่น
* 👔 **My Closet:** ตู้เสื้อผ้าดิจิทัลส่วนตัว รองรับการเพิ่ม ลบ และจัดหมวดหมู่เสื้อผ้า (Tops, Bottoms, Dresses, Shoes, Bags, Accessories)
* ✨ **AI Outfit Curator:** ระบบ AI สไตลิสต์ คิวเรตและจับคู่ชุดให้อัตโนมัติโดยคำนวณจาก Style Preferences, โอกาสที่สวมใส่ (Occasion) และสภาพอากาศ (Weather)
* 🛍️ **Marketplace & Direct Selling:** ตลาดซื้อขายและแลกเปลี่ยนเสื้อผ้ามือสอง พร้อมระบบลงขายสินค้าของฝั่ง Seller
* 📦 **Single-Item Inventory System:** รองรับธรรมชาติของสินค้ามือสอง ล็อกสต็อกสินค้าให้มีเพียง 1 ชิ้นต่อรายการ (`quantity = 1`) เสมอ ป้องกันการซื้อซ้ำ
* 🔄 **Automated Closet Transfer:** เมื่อคำสั่งซื้อสำเร็จ ระบบจะโอนย้ายความเป็นเจ้าของ (Ownership) ของสินค้านั้น เข้าสู่ตู้เสื้อผ้าดิจิทัลของผู้ซื้อโดยอัตโนมัติทันที
* 🛒 **Cart & Orders Management:** ระบบตะกร้าสินค้า ติดตามคำสั่งซื้อฝั่งผู้ซื้อ (My Orders) และระบบจัดการคำสั่งซื้อพร้อมระบุเลขพัสดุฝั่งผู้ขาย (Seller Orders)
* 🔑 **Multi-Role & Admin System:** ระบบ RBAC (Role-Based Access Control) รองรับ 3 บทบาท (`Buyer`, `Seller`, `Admin`) พร้อมหน้าจอ **Admin Dashboard** สำหรับตรวจสอบภาพรวมสถิติ จัดการผู้ใช้ และอนุมัติ/ตรวจสอบสินค้ามือสอง
* 🔔 **Notification Bell API:** ระบบแจ้งเตือนแบบเรียลไทม์ เช่น แจ้งเตือนเมื่อสินค้าขายได้ แจ้งเตือนเมื่อคำสั่งซื้อสำเร็จและโอนชุดเข้าตู้ และแจ้งเตือนสถานะการจัดส่ง
* ✉️ **Forgot & Reset Password with OTP:** ระบบกู้คืนรหัสผ่านผ่านทางอีเมล รองรับทั้งรหัสยืนยันตัวตน OTP 6 หลัก และลิงก์ตั้งรหัสผ่านใหม่ที่ปลอดภัย

---

## 🛠️ เทคโนโลยีที่ใช้ (Tech Stack)

* **Frontend:** React 18, Vite, Tailwind CSS, Lucide Icons
* **Backend:** Python 3.11, FastAPI, SQLAlchemy, Uvicorn, Jose (JWT), Pydantic
* **Database:** PostgreSQL 16
* **Database Management:** pgAdmin 4
* **Containerization:** Docker & Docker Compose
* **Email Service:** SMTP (Gmail TLS/SSL)

---

## 🚀 วิธีเปิดใช้งานโปรเจกต์ในเครื่อง (Local Development Setup)

### ข้อกำหนดก่อนเริ่มงาน (Prerequisites)
* ติดตั้ง [Git](https://git-scm.com/)
* ติดตั้ง [Docker Desktop](https://www.docker.com/) และเปิดโปรแกรมให้พร้อมใช้งาน

---

### ขั้นตอนการรันระบบ

#### 1. Clone Repository
เปิด Terminal หรือ Command Prompt แล้วสั่ง Clone โปรเจกต์ลงมาในเครื่อง:
```bash
git clone https://github.com/67160354-Panisa/ClosetLoop_Web-App.git
cd ClosetLoop_Web-App
```

#### 2. สั่งรันระบบผ่าน Docker Compose
สั่ง Build และเริ่มการทำงานของ Container ทั้งหมด (Frontend, Backend, PostgreSQL, pgAdmin) ในเบื้องหลัง:
```bash
docker compose up -d --build
```
> **หมายเหตุ:** ระบบจะทำการดาวน์โหลด Image, ติดตั้ง Dependencies, สร้างฐานข้อมูล และตรวจสอบ Schema ให้อัตโนมัติในคำสั่งเดียว

#### 3. เข้าใช้งานระบบผ่าน Web Browser
เมื่อ Container เริ่มทำงานครบถ้วนแล้ว สามารถเข้าใช้งานส่วนต่าง ๆ ได้ทันที:

| บริการ (Service) | URL สำหรับเข้าใช้งาน | ข้อมูลเข้าสู่ระบบ / หมายเหตุ |
| :--- | :--- | :--- |
| **🖥️ Frontend (Web App)** | [http://localhost:5173](http://localhost:5173) | หน้าเว็บหลักของ ClosetLoop |
| **📑 Backend API Docs (Swagger UI)** | [http://localhost:8000/docs](http://localhost:8000/docs) | เอกสารและเครื่องมือทดสอบ API ทุก Endpoint |
| **🗄️ pgAdmin 4 (Database GUI)** | [http://localhost:5050](http://localhost:5050) | **Email:** `admin@closetloop.com`<br>**Password:** `admin123` |
| **🐘 PostgreSQL Database** | `localhost:5432` | **DB:** `closetloop` \| **User:** `closetloop` \| **Pass:** `closetloop123` |

---

### 👤 บัญชีสำหรับทดสอบระบบ (Test Accounts)

* **Admin Account:**
  * **Email:** `67160354@go.buu.ac.th`
  * สามารถเข้าสู่ระบบเพื่อใช้งานหน้า **Admin Dashboard** สำหรับตรวจสอบสถิติและจัดการระบบ
* **Multi-Role Switching:**
  * สามารถสลับโหมดการทำงานระหว่าง **Buyer**, **Seller** และ **Admin** ได้อย่างอิสระผ่านแถบ **Role Switcher** ตรงมุมบนขวาของหน้าเว็บ (Topbar) หรือแถบเมนูด้านซ้าย (Sidebar)

---

### 🛑 คำสั่งจัดการและบำรุงรักษาระบบ (Helpful Commands)

* **ดูสถานะการทำงานของ Container:**
  ```bash
  docker compose ps
  ```

* **ดู Log การทำงานของระบบแบบ Real-time:**
  ```bash
  docker compose logs -f
  # หรือดูเฉพาะ backend
  docker compose logs -f backend
  ```

* **รีสตาร์ตระบบใหม่:**
  ```bash
  docker compose restart
  ```

* **หยุดการทำงานของระบบทั้งหมด:**
  ```bash
  docker compose down
  ```

* **หยุดการทำงานและล้างข้อมูล Volume ทั้งหมด (Factory Reset):**
  ```bash
  docker compose down -v
  ```

---

## 🌐 การนำขึ้นระบบจริง (Deployment on Render)

โปรเจกต์นี้รองรับการ Deploy บน Render.com:

1. **Database:** สร้าง **PostgreSQL** บน Render (นำ `Internal/External Database URL` ไปใส่ใน Environment Variables)
2. **Backend (Web Service):**
   * **Root Directory:** `backend`
   * **Runtime:** `Python 3`
   * **Build Command:** `pip install -r requirements.txt`
   * **Start Command:** `uvicorn app.main:app --host 0.0.0.0 --port 10000`
   * **Environment Variables:** `DATABASE_URL`, `JWT_SECRET`, `CORS_ORIGINS`, `SMTP_SERVER`, `EMAIL_SENDER`, `EMAIL_PASSWORD`, `FRONTEND_URL`
3. **Frontend (Static Site):**
   * **Root Directory:** `frontend`
   * **Build Command:** `npm install && npm run build`
   * **Publish Directory:** `dist`
   * **Environment Variables:** `VITE_API_URL` (ใส่ URL ของ Backend บน Render)
