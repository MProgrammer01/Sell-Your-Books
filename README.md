<div align="center">
  <h1>📚 Sell Your Books</h1>
</div>

هو تطبيق Full-Stack لإدارة وبيع الكتب، يتيح للبائعين إنشاء وإدارة الكتب الخاصة بهم، مع نظام مصادقة وتفويض آمن، وإدارة الحسابات والبائعين والكتب.

تم تطوير المشروع باستخدام **Flutter وDart** في الواجهة الأمامية، و**ASP.NET Core Web API وC#** في الواجهة الخلفية، مع **SQL Server** كقاعدة بيانات.

يعتمد المشروع على **3-Tier Architecture**، ويطبق مجموعة من ممارسات تطوير الـAPIs الآمنة مثل **JWT Authentication، Refresh Tokens، Role-Based Authorization، BCrypt، Rate Limiting، Security Auditing وOwnership Validation**.

---

# 🔗 روابط المشاريع

يمكنك الاطلاع على الـFrontend Repository من هنا:

👉 **[Sell Your Books — Frontend](https://github.com/MProgrammer01/Simple-Sell-Books-frontend.git)**

يمكنك الاطلاع على الـBackend Repository من هنا:

👉 **[Sell Your Books — Backend](https://github.com/MProgrammer01/Simple-Sell-Books-backend.git)**
## 🚀 المميزات الرئيسية

### 🔐 المصادقة والتفويض

* تسجيل دخول المستخدمين باستخدام **JWT Access Token**
* استخدام **Refresh Token** لتجديد الـAccess Token
* تشفير كلمات المرور باستخدام **BCrypt**
* نظام **Role-Based Authorization**
* حماية الـAPI Endpoints
* استخراج معلومات المستخدم من JWT Claims
* التحقق من صلاحية المستخدم للوصول إلى الموارد
* التحقق من ملكية الموارد قبل تعديلها أو حذفها
* دعم صلاحيات `Admin` و`Seller`

---

### 👤 إدارة البائعين

يوفر النظام مجموعة من العمليات الخاصة بالبائعين:

* إنشاء حساب Seller
* تسجيل الدخول
* عرض معلومات البائع
* تعديل معلومات البائع
* حذف البائع
* إدارة معلومات المتجر
* ربط بيانات Seller ببيانات Person
* التحقق من ملكية الموارد
* تنفيذ العمليات الحساسة باستخدام Database Transactions

---

### 📚 إدارة الكتب

يمكن للبائع إدارة الكتب الخاصة به من خلال:

* إضافة كتاب
* عرض الكتب
* عرض كتاب حسب الـID
* تعديل كتاب
* حذف كتاب
* التحقق من ملكية الكتاب
* تحديد تصنيف الكتاب
* تحديد حالة الكتاب
* تحديد حالة جودة الكتاب
* إدارة السعر
* إدارة المخزون
* إضافة وصف للكتاب
* إضافة صورة الغلاف
* Pagination لعرض الكتب

كل كتاب مرتبط ببائع محدد، ويتم التحقق من أن البائع الحالي هو صاحب الكتاب قبل تنفيذ العمليات الحساسة.

---

# 🛡️ الأمان

تم تصميم الـAPI مع التركيز على حماية الموارد والبيانات.

يستخدم المشروع:

* **JWT Authentication**
* **Role-Based Authorization**
* **BCrypt Password Hashing**
* **Refresh Tokens**
* **Token Expiration**
* **Ownership Authorization**
* **Rate Limiting**
* **Security Audit Logs**
* **Protected API Endpoints**
* **SQL Server Constraints**
* **Database Transactions**

---

# 🏗️ Architecture

الـBackend مبني باستخدام **3-Tier Architecture**:

```text
┌──────────────────────────────────────────┐
│              Flutter Client              │
│              Dart / Cubit                │
└─────────────────────┬────────────────────┘
                      │
                      │ HTTP / REST API
                      ▼
┌──────────────────────────────────────────┐
│                API Layer                 │
│          ASP.NET Core Web API            │
│               Controllers                │
└─────────────────────┬────────────────────┘
                      │
                      ▼
┌──────────────────────────────────────────┐
│             Business Layer               │
│             Business Logic               │
└─────────────────────┬────────────────────┘
                      │
                      ▼
┌──────────────────────────────────────────┐
│               Data Layer                 │
│    SQL Server / DTOs / EF Core / SPs     │
└──────────────────────────────────────────┘
```

## API Layer

مسؤولة عن:

* استقبال HTTP Requests
* إرسال HTTP Responses
* Controllers
* Authentication
* Authorization
* Middleware
* HTTP Status Codes
* التعامل مع Requests وResponses

## Business Layer

مسؤولة عن:

* Business Logic
* Validation
* Authentication Logic
* Authorization Logic
* Seller Operations
* Book Operations

## Data Layer

مسؤولة عن:

* الاتصال بقاعدة البيانات
* Entity Framework Core
* DTOs
* Stored Procedures
* Database Transactions
* CRUD Operations
* Database Entities
* العلاقات بين الجداول

---

# 📱 Flutter Architecture

تم بناء تطبيق Flutter باستخدام **Cubit / Bloc** لإدارة حالة التطبيق.

هيكلة الـFeatures تعتمد على فصل المسؤوليات:

```text
Feature
│
├── Data
│   ├── Models
│   └── Data Sources
│
├── Business
│   └── Business Logic
│
├── Cubit
│   ├── Cubit
│   └── States
│
└── Presentation
    ├── Screens
    └── Widgets
```

مسؤول عن:

* واجهة المستخدم
* Navigation
* Authentication State
* التواصل مع الـAPI
* Forms
* Loading States
* Error Handling
* Pagination
* إدارة البائعين
* إدارة الكتب

---

# 🧰 التقنيات المستخدمة

## Frontend

* **Flutter**
* **Dart**
* **Cubit / Bloc**
* **Dio**
* REST API Integration
* Responsive UI

## Backend

* **ASP.NET Core Web API**
* **C#**
* **.NET**
* **Entity Framework Core**
* **RESTful APIs**
* **DTOs**
* **3-Tier Architecture**
* **Middleware**

## Database

* **Microsoft SQL Server**
* **Entity Framework Core**
* **Stored Procedures**
* **Transactions**
* **Foreign Keys**
* **Primary Keys**
* **Unique Constraints**
* **Relational Database Design**

## Security

* **JWT Bearer Authentication**
* **Refresh Tokens**
* **BCrypt**
* **Role-Based Authorization**
* **Rate Limiting**
* **Security Audit Logging**
* **Ownership Authorization**

---

# 🔑 Authentication Flow

يعتمد نظام المصادقة على **Access Token** و**Refresh Token**.

```text
المستخدم
   │
   │ Login
   ▼
ASP.NET Core API
   │
   ├── التحقق من بيانات الدخول
   │
   ├── التحقق من كلمة المرور باستخدام BCrypt
   │
   ├── إنشاء Access Token
   │
   └── إنشاء Refresh Token
   │
   ▼
Flutter Client
```

يحتوي الـJWT على Claims تسمح للـAPI بالتعرف على المستخدم ودوره.

من الـClaims المستخدمة:

```text
NameIdentifier
Email
Role
```

ويتم استعمال هذه المعلومات للتحقق من:

```text
المستخدم
   │
   ▼
JWT Token
   │
   ▼
Claims Validation
   │
   ▼
Authentication
   │
   ▼
Authorization
   │
   ▼
Ownership / Role Check
```

---

# 👥 نظام الصلاحيات

يدعم النظام مجموعة من الأدوار، أهمها:

### Admin

يمتلك صلاحيات إدارية حسب العمليات المسموح بها في النظام.

### Seller

يمكن للبائع:

* إدارة معلومات حسابه
* إدارة معلومات متجره
* إضافة الكتب
* تعديل كتبه
* حذف كتبه
* إدارة المخزون الخاص به

ويتم تطبيق **Ownership Validation** لمنع Seller من تعديل أو حذف موارد تخص Seller آخر.

---

# 🔒 Ownership Authorization

قبل تنفيذ العمليات الحساسة، يتم التأكد من أن المورد المطلوب يعود للمستخدم الحالي.

مثلاً عند محاولة Seller تعديل أو حذف Book:

```text
Authenticated User
        │
        ▼
      Person
        │
        ▼
      Seller
        │
        ▼
      Book
        │
        ▼
هل الكتاب تابع لهذا البائع؟
        │
    ┌───┴───┐
     نعم       لا
    │       │
    ▼       ▼
  السماح    الرفض
```

هذا يمنع المستخدم من الوصول إلى أو تعديل بيانات مستخدم آخر.

---

# ⚡ Rate Limiting

يستخدم الـAPI **Rate Limiting** للحد من عدد Requests المسموح بها خلال فترة زمنية معينة.

ويمكن تطبيق حدود مختلفة حسب نوع الـEndpoint، مثل:

* Login
* Refresh Token
* Create Book
* Update Book
* Delete Book
* General API Requests

ويمكن اعتماد الـIP Address و/أو المستخدم المصادق عليه لتحديد معدل الطلبات.

---

# 📝 Security Audit Logs

يحتوي المشروع على نظام لتسجيل العمليات الأمنية المهمة باستخدام **Security Audit Logs**.

يمكن تسجيل أحداث مثل:

* محاولات تسجيل الدخول
* محاولات التسجيل
* العمليات الفاشلة
* العمليات الحساسة
* العمليات المرتبطة بالمستخدمين

هذا يوفر طبقة إضافية من المراقبة والتدقيق الأمني.

---

# 🗄️ تصميم قاعدة البيانات

يعتمد المشروع على قاعدة بيانات SQL Server مترابطة.

العلاقات الرئيسية:

```text
People
   │
   └── Sellers
          │
          └── Books
                 │
                 ├── Categories
                 ├── Conditions
                 └── Statuses

SecurityAuditLogs
   │
   └── People
```

## الجداول الرئيسية

| الجدول              | الوصف                      |
| ------------------- | -------------------------- |
| `People`            | معلومات المستخدمين         |
| `Sellers`           | معلومات البائعين           |
| `Books`             | الكتب التي يضيفها البائعون |
| `Categories`        | تصنيفات الكتب              |
| `Conditions`        | حالة وجودة الكتاب          |
| `Statuses`          | حالة الكتاب                |
| `SecurityAuditLogs` | سجل العمليات الأمنية       |

---

# 📖 معلومات الكتاب

يحتوي الكتاب على مجموعة من المعلومات، منها:

* العنوان
* المؤلف
* الوصف
* السعر
* المخزون
* التصنيف
* الحالة
* Condition
* صورة الغلاف
* تاريخ الإنشاء
* تاريخ آخر تعديل
* البائع

---

# 🔄 Database Transactions

يتم استخدام **Database Transactions** في العمليات التي تتطلب تنفيذ عدة عمليات مترابطة بشكل ذري.

مثلاً عند إنشاء Seller:

```text
BEGIN TRANSACTION

    إنشاء Person
          │
          ▼
    إنشاء Seller
          │
          ▼
    التحقق من نجاح العمليات

        ┌───────────────┐
        │               │
      نجاح            خطأ
        │               │
        ▼               ▼
     ROLLBACK         COMMIT
```

إذا فشلت إحدى العمليات، يتم تنفيذ `ROLLBACK` لمنع بقاء بيانات ناقصة أو غير متناسقة.

---

# 🌐 REST API

يوفر الـBackend RESTful API للتعامل مع الموارد الرئيسية.

أمثلة:

```text
/api/People
/api/Sellers
/api/Books
```

ويستخدم HTTP Methods:

| Method   | الاستخدام          |
| -------- | ------------------ |
| `GET`    | جلب البيانات       |
| `POST`   | إنشاء بيانات جديدة |
| `PUT`    | تعديل البيانات     |
| `DELETE` | حذف البيانات       |

ويستخدم المشروع HTTP Status Codes للتعبير عن نتيجة العملية:

```text
200 OK
201 Created
400 Bad Request
401 Unauthorized
403 Forbidden
404 Not Found
409 Conflict
429 Too Many Requests
500 Internal Server Error
```

---

# 📑 Stored Procedures

يستخدم المشروع **SQL Server Stored Procedures** لتنفيذ مجموعة من عمليات قاعدة البيانات.

من بينها عمليات خاصة بـ:

* تسجيل المستخدم
* تسجيل Seller
* جلب بيانات المستخدم
* جلب Seller
* تعديل Seller
* جلب الكتب
* إضافة الكتب
* تعديل الكتب
* حذف الكتب
* Pagination

يساعد هذا الأسلوب على تنظيم عمليات قاعدة البيانات والتحكم فيها من خلال طبقة الـData Layer.

---

# 📄 Pagination

يستخدم المشروع **Pagination** عند جلب الكتب لتجنب تحميل عدد كبير من السجلات في Request واحد.

مثال:

```text
Page Number = 1
Page Size   = 10
```

بدلاً من جلب جميع الكتب:

```text
Database
   │
   ├── Books 1 - 10
   ├── Books 11 - 20
   ├── Books 21 - 30
   └── ...
```

يتم جلب الجزء المطلوب فقط.

---

# 🎨 Flutter UI

تحتوي واجهة Flutter على الشاشات والوظائف الأساسية للتطبيق، مثل:

* تسجيل الدخول
* التسجيل
* Seller Profile
* Book Listing
* Book Details
* إضافة كتاب
* تعديل كتاب
* Seller Management
* Settings

ويتواصل تطبيق Flutter مع الـASP.NET Core API باستخدام **Dio**.

---

# 🔌 API Communication

يستخدم Flutter مكتبة **Dio** للتواصل مع REST API.

```text
Flutter
   │
   │ Dio
   ▼
ASP.NET Core Web API
   │
   ▼
Business Layer
   │
   ▼
Data Layer
   │
   ▼
SQL Server
```

يتم تحويل API Responses إلى Models داخل Flutter، ثم تتم إدارة النتائج باستخدام Cubit States.

---

# 📦 State Management

يستخدم المشروع **Cubit / Bloc** لإدارة حالة التطبيق.

من الحالات المستخدمة:

```text
Initial
Loading
Success
BadRequest
Unauthorized
Forbidden
NotFound
TooManyRequests
ServerError
```

هذا يسمح للواجهة بالتفاعل بشكل صحيح مع مختلف نتائج الـAPI.

---


# ❗اشارة

تأكد من أن **API Base URL** في Flutter يشير إلى عنوان ASP.NET Core API الذي يعمل عندك.

---


# 📂 هيكلة المشروع

هيكلة تقريبية للمشروع:

```text
SellYourBooks/
│
├── Backend/
│   │
│   ├── SimpleSellBooks_API/
│   │   ├── Controllers/
│   │   ├── Middleware/
│   │   └── Program.cs
│   │
│   ├── SimpleSellBooks_BusinessLayer/
│   │   ├── Business/
│   │   └── Services/
│   │
│   └── SimpleSellBooks_DataLayer/
        ├── DTOs/
│       ├── Entities/
│       ├── DbContext/
│       └── Data Access/
│
├── Database/
│   ├── Tables/
│   ├── Stored Procedures/
│
└── Flutter/
    └── sell_your_books/
        ├── lib/
        │   ├── Features/
        │   ├── Core/
        │   └── main.dart
        │
        └── pubspec.yaml
```

---

# 🎯 أهداف المشروع

تم تطوير المشروع لتطبيق وإظهار الخبرة العملية في:

* Full-Stack Development
* Flutter Development
* ASP.NET Core Web API
* C#
* SQL Server
* RESTful API Development
* 3-Tier Architecture
* Entity Framework Core
* Stored Procedures
* Database Transactions
* JWT Authentication
* Refresh Tokens
* Role-Based Authorization
* Ownership Authorization
* BCrypt
* Rate Limiting
* Security Auditing
* Cubit / Bloc
* Dio
* CRUD Operations
* Pagination
* Secure API Development

---

# 🔮 التطويرات المستقبلية

سوف يتم تحسين و اضافة اشياء جديدة في المستقبل.
---

# 📈 حالة المشروع

🚧 **قيد التطوير**

تم تطوير مجموعة من المكونات الأساسية للمشروع، بما في ذلك:

* Authentication
* Authorization
* Seller Management
* Book Management
* REST API
* SQL Server Integration
* 3-Tier Architecture
* JWT Security
* Refresh Tokens
* Ownership Validation
* Rate Limiting
* Security Auditing
* Flutter State Management

---

# 👨‍💻 المطور

**Mouad El Kharraz**

---

# 📄 الترخيص

تم تطوير هذا المشروع لأغراض تعليمية، تطبيقية، وضمن معرض الأعمال الشخصي.

<div align="center">
  <p>هذا المشروع مفتوح المصدر ومتوفر تحت رخصة <strong>Apache License 2.0</strong>.</p>
</div>

---

⭐ إذا أعجبك المشروع، يمكنك استكشاف الكود ومتابعة مراحل تطوير **Sell Your Books**.

<div align="center">
  <p>صُنع بـ MProgrammer01 للتعلم والتطوير</p>
</div>
