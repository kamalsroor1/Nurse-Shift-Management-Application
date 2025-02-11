# **🏥 Nurse Shift Management Application**

## **🔹 Overview**
This application is designed to help nurses efficiently manage their hospital work schedules. It provides features for shift registration, status management, and recording shift sales or exchanges with other nurses. The application supports multiple hospitals and integrates with Firebase for secure Google login. The interface is fully presented in Arabic.

---

## **🔹 Application Flow**

### **1️⃣ Login**
- The user first sees the **Google Login Page** via Firebase.
- Users **cannot access** any feature before logging in.

### **2️⃣ Hospital Management**
- After login, the user sees a **list of hospitals** they work at.
- They can:
  - ✅ **Add a new hospital**
  - ✏️ **Edit an existing hospital**
  - ❌ **Delete a hospital**

### **3️⃣ Managing Months**
- Clicking on a hospital opens a **list of registered months.**
- The user can:
  - ✅ **Register a new month**
  - 🗓 **View and manage previous months**
- When registering a new month, the user **selects the days they will work** and sets the **shift type (Night or Long).**

### **4️⃣ Shift Registration**
- After registering the month, the user **chooses the days they will work in that month.**
- Each day entry includes:
  - ✅ **Date selection**
  - 🌙 **Shift type (Night or Long)**

### **5️⃣ Shift Management**
- Once shifts are registered, users can update their status to:
  - ✅ **Attended** – The shift was completed.
  - ❌ **Absent** – The shift was missed.
  - 💰 **Sold** – The shift was sold to another nurse.
    - 🔹 The user **must enter the nurse’s name** who purchased it.
  - 🔄 **Exchanged** – The shift was exchanged with another nurse.
    - 🔹 The user **must select the new shift date**.
    - 🔹 The exchanged shift **is automatically recorded in the new date.**

---

## **🔹 Multi-Hospital Support**
✅ **Nurses can manage shifts across multiple hospitals.**  
✅ **Privacy:** Each nurse sees **only their own shifts.**  

---

## **🔹 Firebase Integration 🔥**
- Authentication is handled via **Google Login** using Firebase.

✅ **The entire application interface is in Arabic.**

---

## **🔹 Tech Stack 🛠️**
### **1️⃣ Backend & Frontend**
- **Laravel** with **Livewire** for an interactive experience.
- **MySQL** for the database.

### **2️⃣ UI Framework**
- **Tailwind CSS** for a responsive and clean design.

---

## **🔹 Database Schema 🗄**

### **🔹 Main Tables**
#### **1️⃣ Users Table**
| Column        | Type      | Details                  |
|--------------|----------|--------------------------|
| `id`         | UUID     | Primary Key              |
| `name`       | String   | User’s Name              |
| `email`      | String   | Unique Email             |
| `google_id`  | String   | Unique Google ID         |
| `created_at` | Timestamp | Creation Date           |

#### **2️⃣ Hospitals Table**
| Column       | Type      | Details                     |
|-------------|----------|-----------------------------|
| `id`        | UUID     | Primary Key                 |
| `name`      | String   | Hospital Name               |
| `user_id`   | UUID     | Foreign Key (Users Table)   |
| `created_at` | Timestamp | Creation Date             |

#### **3️⃣ Months Table**
| Column       | Type      | Details                     |
|-------------|----------|-----------------------------|
| `id`        | UUID     | Primary Key                 |
| `hospital_id` | UUID   | Foreign Key (Hospitals Table) |
| `month_year` | String  | Example: "5-2025"           |
| `created_at` | Timestamp | Creation Date             |

#### **4️⃣ Workdays Table**
| Column         | Type      | Details                                      |
|--------------|----------|----------------------------------------------|
| `id`         | UUID     | Primary Key                                  |
| `month_id`   | UUID     | Foreign Key (Months Table)                   |
| `date`       | Date     | Shift Date                                   |
| `work_type`  | Enum     | ("Night Shift" or "Long Shift")              |
| `status`     | Enum     | ("Attended", "Sold", "Exchanged", "Absent")  |
| `employee_name` | String | Nurse’s name (for Sold or Exchanged shifts) |
| `exchanged_date` | Date  | New date for exchanged shift                |
| `created_at` | Timestamp | Creation Date                               |

---

## **🔹 Laravel Folder Structure 📂**

```
my-app/
│── app/                        # Main Laravel Application Files
│── resources/views/            # Blade Templates & Livewire Components
│── routes/                     # Web & API Routes
│── database/migrations/        # Database Schema Management
│── public/                     # Public Assets (CSS, JS, Images)
│── config/                     # Configuration Files
│── storage/                    # Logs, Uploads, Cache
│── composer.json               # PHP Dependencies
│── package.json                # JavaScript Dependencies
│── .env                        # Environment Configurations
│── .gitignore                  # Git Ignore Rules

# **🏥 تطبيق إدارة شفتات الممرضات**

## **🔹 نظرة عامة**
هذا التطبيق مصمم لمساعدة الممرضات على إدارة جداول العمل الخاصة بهن في المستشفيات بكفاءة. يوفر ميزات لتسجيل الشفتات، إدارة حالتها، وتسجيل عمليات بيع الشفتات أو تبديلها مع ممرضات أخريات. يدعم التطبيق مستشفيات متعددة ويتكامل مع Firebase لتسجيل الدخول الآمن عبر Google. الواجهة بالكامل باللغة العربية.

---

## **🔹 تدفق التطبيق**

### **1️⃣ تسجيل الدخول**
- عند فتح التطبيق، تظهر **صفحة تسجيل الدخول عبر Google** باستخدام Firebase.
- لا يمكن للمستخدم الوصول إلى أي ميزات قبل تسجيل الدخول.

### **2️⃣ إدارة المستشفيات**
- بعد تسجيل الدخول، تظهر قائمة **بالمستشفيات التي يعمل بها المستخدم**.
- يمكنه:
  - ✅ **إضافة مستشفى جديد**
  - ✏️ **تعديل مستشفى موجود**
  - ❌ **حذف مستشفى**

### **3️⃣ إدارة الأشهر**
- عند النقر على مستشفى معين، يتم عرض **قائمة الأشهر المسجلة**.
- يمكن للمستخدم:
  - ✅ **تسجيل شهر جديد**
  - 🗓 **عرض وإدارة الأشهر السابقة**
- عند تسجيل شهر جديد، يحدد المستخدم **الأيام التي سيعمل بها** ونوع الشفت **(سهر أو لونج)**.

### **4️⃣ تسجيل الشفتات**
- بعد تسجيل الشهر، يقوم المستخدم **باختيار الأيام التي سيعمل بها خلال الشهر**.
- لكل يوم يتم تسجيل:
  - ✅ **تحديد التاريخ**
  - 🌙 **تحديد نوع الشفت (سهر أو لونج)**

### **5️⃣ إدارة الشفتات**
- بمجرد تسجيل الشفتات، يمكن تحديث حالتها إلى:
  - ✅ **حضور** – تم العمل في الشفت.
  - ❌ **غياب** – لم يتم الحضور.
  - 💰 **مباع** – تم بيع الشفت لممرضة أخرى.
    - 🔹 يجب إدخال **اسم الممرضة التي اشترت الشفت**.
  - 🔄 **مُستبدل** – تم استبدال الشفت مع ممرضة أخرى.
    - 🔹 يجب **تحديد اليوم البديل**.
    - 🔹 يتم **تسجيل الشفت الجديد تلقائيًا في اليوم البديل**.

---

## **🔹 دعم المستشفيات المتعددة**
✅ **يمكن للممرضات إدارة الشفتات عبر مستشفيات متعددة.**  
✅ **الخصوصية:** كل ممرضة ترى **فقط شفتاتها الخاصة**.  

---

## **🔹 تكامل Firebase 🔥**
- يتم تسجيل الدخول عبر **Google Authentication** باستخدام Firebase.

✅ **واجهة التطبيق بالكامل باللغة العربية.**

---

## **🔹 التقنيات المستخدمة 🛠️**
### **1️⃣ الواجهة الخلفية والواجهة الأمامية**
- **Laravel** مع **Livewire** لتجربة تفاعلية.
- **MySQL** كقاعدة بيانات.

### **2️⃣ إطار العمل للواجهة**
- **Tailwind CSS** لتوفير تصميم متجاوب وأنيق.

---

## **🔹 هيكلة قاعدة البيانات 🗄**

### **🔹 الجداول الأساسية**
#### **1️⃣ جدول المستخدمين**
| العمود       | النوع      | التفاصيل                  |
|--------------|----------|--------------------------|
| `id`         | UUID     | المفتاح الأساسي              |
| `name`       | String   | اسم المستخدم              |
| `email`      | String   | البريد الإلكتروني (فريد)     |
| `google_id`  | String   | معرف Google (فريد)        |
| `created_at` | Timestamp | تاريخ الإنشاء              |

#### **2️⃣ جدول المستشفيات**
| العمود       | النوع      | التفاصيل                     |
|-------------|----------|-----------------------------|
| `id`        | UUID     | المفتاح الأساسي                 |
| `name`      | String   | اسم المستشفى                   |
| `user_id`   | UUID     | مفتاح أجنبي (يشير إلى جدول المستخدمين) |
| `created_at` | Timestamp | تاريخ الإنشاء                 |

#### **3️⃣ جدول الأشهر**
| العمود       | النوع      | التفاصيل                     |
|-------------|----------|-----------------------------|
| `id`        | UUID     | المفتاح الأساسي                 |
| `hospital_id` | UUID   | مفتاح أجنبي (يشير إلى جدول المستشفيات) |
| `month_year` | String  | مثال: "5-2025"             |
| `created_at` | Timestamp | تاريخ الإنشاء                 |

#### **4️⃣ جدول أيام العمل**
| العمود         | النوع      | التفاصيل                                      |
|--------------|----------|----------------------------------------------|
| `id`         | UUID     | المفتاح الأساسي                                  |
| `month_id`   | UUID     | مفتاح أجنبي (يشير إلى جدول الأشهر)                   |
| `date`       | Date     | تاريخ الشفت                                   |
| `work_type`  | Enum     | ("شفت ليلي" أو "شفت طويل")                      |
| `status`     | Enum     | ("حضر", "مباع", "مُستبدل", "غياب")             |
| `employee_name` | String | اسم الممرضة (لحالات البيع أو التبديل)        |
| `exchanged_date` | Date  | التاريخ الجديد للشفت المستبدل                   |
| `created_at` | Timestamp | تاريخ الإنشاء                                  |

---

## **🔹 هيكلة مجلدات Laravel 📂**

```
my-app/
│── app/                        # ملفات التطبيق الرئيسية
│── resources/views/            # قوالب Blade ومكونات Livewire
│── routes/                     # التوجيهات (Routes)
│── database/migrations/        # إدارة قاعدة البيانات
│── public/                     # الملفات العامة (CSS, JS, صور)
│── config/                     # ملفات الإعدادات
│── storage/                    # التخزين (السجلات، الملفات المؤقتة)
│── composer.json               # تبعيات PHP
│── package.json                # تبعيات JavaScript
│── .env                        # إعدادات البيئة
│── .gitignore                  # استثناءات Git
```

