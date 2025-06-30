# 📦 Laventory - Laravel Inventory Management System

<p align="center">
    <img src="https://img.shields.io/badge/Laravel-12.x-red.svg" alt="Laravel Version">
    <img src="https://img.shields.io/badge/PHP-8.2+-blue.svg" alt="PHP Version">
    <img src="https://img.shields.io/badge/React-19.x-blue.svg" alt="React Version">
    <img src="https://img.shields.io/badge/Inertia.js-2.x-purple.svg" alt="Inertia.js Version">
    <img src="https://img.shields.io/badge/Tailwind-4.x-cyan.svg" alt="Tailwind CSS Version">
    <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License">
</p>

## 📋 About Laventory

Laventory เป็นระบบจัดการสินค้าคงคลัง (Inventory Management System) ที่พัฒนาด้วย Laravel 12 และ React พร้อม Inertia.js เพื่อให้การทำงานเป็น SPA (Single Page Application) ที่รวดเร็วและใช้งานง่าย

### ✨ ฟีเจอร์หลัก

- 🏪 **การจัดการสินค้า** - เพิ่ม แก้ไข ลบ และค้นหาสินค้า
- 📦 **การจัดการสต็อก** - ติดตามสินค้าคงคลัง เข้า-ออก
- 🛒 **ระบบการสั่งซื้อ** - จัดการใบสั่งซื้อและสถานะ
- 📄 **ระบบใบเสนอราคา** - สร้างและจัดการใบเสนอราคา
- 👥 **จัดการลูกค้าและซัพพลายเออร์** - ข้อมูลคู่ค้า
- 📊 **รายงานและสถิติ** - Dashboard แสดงข้อมูลสำคัญ
- 🧾 **การออกใบกำกับภาษี** - ระบบออกใบเสร็จ/ใบกำกับภาษี
- 📤 **Export/Import** - นำเข้า-ส่งออกข้อมูลผ่าน Excel
- 📱 **Responsive Design** - รองรับการใช้งานบนอุปกรณ์ทุกขนาด

## 🛠 เทคโนโลยีที่ใช้

### Backend
- **Laravel 12** - PHP Framework
- **SQLite/MySQL** - Database
- **Laravel Sanctum** - API Authentication
- **Inertia.js** - Modern Monolith

### Frontend
- **React 19** - JavaScript Library
- **TypeScript** - Type Safety
- **Tailwind CSS 4** - Utility-first CSS Framework
- **React Icons** - Icon Library
- **Ziggy** - Laravel Routes in JavaScript

### Additional Packages
- **anayarojo/shoppingcart** - Shopping Cart Management
- **haruncpi/laravel-id-generator** - ID Generation
- **phpoffice/phpspreadsheet** - Excel Operations
- **picqer/php-barcode-generator** - Barcode Generation

## 📋 ความต้องการของระบบ

- PHP >= 8.2
- Composer
- Node.js >= 18
- NPM หรือ Yarn
- SQLite (default) หรือ MySQL/MariaDB

## 🚀 การติดตั้ง

### 1. Clone Repository
```bash
git clone <repository-url>
cd laventory
```

### 2. ติดตั้ง PHP Dependencies
```bash
composer install
```

### 3. ติดตั้ง Frontend Dependencies
```bash
npm install
```

### 4. ตั้งค่า Environment
```bash
cp .env.example .env
php artisan key:generate
```

### 5. ตั้งค่า Database
```bash
# สำหรับ SQLite (default)
touch database/database.sqlite

# รัน Migration และ Seeder
php artisan migrate --seed
```

### 6. Build Assets
```bash
# Development
npm run dev

# Production
npm run build
```

### 7. เริ่มต้น Development Server
```bash
php artisan serve
```

เข้าใช้งานได้ที่: `http://localhost:8000`

## 📁 โครงสร้างโปรเจ็กต์

```
app/
├── Enums/                      # Enum Classes
│   ├── OrderStatus.php
│   ├── PaymentType.php
│   └── ...
├── Http/Controllers/           # Controllers
│   ├── Dashboard/
│   ├── Product/
│   ├── Order/
│   ├── Purchase/
│   └── ...
├── Models/                     # Eloquent Models
│   ├── Category.php
│   ├── Product.php
│   ├── Order.php
│   └── ...
└── ...

resources/
├── js/                         # React Components
├── css/                        # Styles
└── views/                      # Blade Templates

database/
├── migrations/                 # Database Migrations
├── seeders/                    # Database Seeders
└── factories/                  # Model Factories
```

## 🔧 คำสั่งที่สำคัญ

```bash
# Development
npm run dev                     # Start Vite dev server
php artisan serve              # Start Laravel server

# Database
php artisan migrate            # Run migrations
php artisan db:seed           # Run seeders
php artisan migrate:fresh --seed  # Fresh migration with seed

# Production
npm run build                  # Build for production
php artisan optimize          # Optimize for production
```

## 📱 ฟีเจอร์หน้าจอหลัก

### Dashboard
- สรุปข้อมูลสำคัญ (สินค้า, คำสั่งซื้อ, ลูกค้า)
- กราฟแสดงสถิติ 30 วันล่าสุด
- ข้อมูลรายวัน

### การจัดการสินค้า
- เพิ่ม/แก้ไข/ลบสินค้า
- จัดหมวดหมู่สินค้า
- จัดการหน่วยนับ
- สร้าง Barcode

### ระบบคำสั่งซื้อ
- สร้างใบสั่งซื้อ
- ติดตามสถานะ (รอดำเนินการ, เสร็จสิ้น, ครบกำหนด)
- พิมพ์ใบสั่งซื้อ

### ระบบซื้อ
- จัดการใบสั่งซื้อจากซัพพลายเออร์
- อนุมัติการซื้อ
- ติดตามสถานะการซื้อ

## 🤝 การพัฒนา

### Git Workflow
1. Fork repository
2. สร้าง feature branch
3. Commit การเปลี่ยนแปลง
4. Push ไปยัง branch
5. สร้าง Pull Request

### Code Style
- ใช้ Laravel Pint สำหรับ PHP
- ใช้ ESLint/Prettier สำหรับ JavaScript/TypeScript
- ตั้งชื่อ commit ตาม conventional commits

## 📄 License

โปรเจ็กต์นี้เผยแพร่ภายใต้ [MIT License](https://opensource.org/licenses/MIT)

## 🙏 Credits

- [Laravel Framework](https://laravel.com)
- [React](https://reactjs.org)
- [Inertia.js](https://inertiajs.com)
- [Tailwind CSS](https://tailwindcss.com)

---

**สร้างด้วย ❤️ โดยใช้ Laravel และ React**
