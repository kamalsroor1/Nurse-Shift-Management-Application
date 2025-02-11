# **🏥 تطبيق إدارة مناوبات التمريض**

## **🔹 نظرة عامة**
هذا التطبيق مصمم لمساعدة الممرضين في إدارة جداول عملهم في المستشفى بكفاءة. يوفر ميزات لتسجيل المناوبات، وإدارة الحالة، وتسجيل مبيعات أو تبادل المناوبات مع الممرضين الآخرين. يدعم التطبيق العديد من المستشفيات ويتكامل مع Firebase لتسجيل الدخول الآمن عبر Google.

---

## **🔹 تدفق التطبيق**

### **1️⃣ تسجيل الدخول**
- يرى المستخدم أولاً **صفحة تسجيل الدخول عبر Google** من خلال Firebase.
- لا يمكن للمستخدمين **الوصول** إلى أي ميزة قبل تسجيل الدخول.

### **2️⃣ إدارة المستشفيات**
- بعد تسجيل الدخول، يرى المستخدم **قائمة المستشفيات** التي يعمل بها.
- يمكنهم:
  - ✅ **إضافة مستشفى جديد**
  - ✏️ **تعديل مستشفى موجود**
  - ❌ **حذف مستشفى**

### **3️⃣ إدارة الأشهر**
- النقر على مستشفى يفتح **قائمة الأشهر المسجلة.**
- يمكن للمستخدم:
  - ✅ **تسجيل شهر جديد**
  - 🗓 **عرض وإدارة الأشهر السابقة**
- عند تسجيل شهر جديد، يقوم المستخدم **باختيار الأيام التي سيعمل فيها** ويحدد **نوع المناوبة (ليلية أو طويلة).**

### **4️⃣ تسجيل المناوبات**
- بعد تسجيل الشهر، يختار المستخدم **الأيام التي سيعمل فيها في ذلك الشهر.**
- يتضمن كل إدخال يومي:
  - ✅ **اختيار التاريخ**
  - 🌙 **نوع المناوبة (ليلية أو طويلة)**

### **5️⃣ إدارة المناوبات**
- بمجرد تسجيل المناوبات، يمكن للمستخدمين تحديث حالتها إلى:
  - ✅ **حضور** – تم إكمال المناوبة.
  - ❌ **غياب** – تم تفويت المناوبة.
  - 💰 **بيع** – تم بيع المناوبة لممرض آخر.
    - 🔹 يجب على المستخدم **إدخال اسم الممرض** الذي اشتراها.
  - 🔄 **تبادل** – تم تبادل المناوبة مع ممرض آخر.
    - 🔹 يجب على المستخدم **اختيار تاريخ المناوبة الجديد**.
    - 🔹 يتم **تسجيل المناوبة المتبادلة تلقائياً في التاريخ الجديد.**

---

## **🔹 الميزات الجديدة والتحسينات 🚀**

### **1️⃣ عرض المناوبات على الجدول الزمني (على غرار تقويم Google) 📅**
✅ **جدول زمني مرئي للمناوبات لسهولة الجدولة**  
✅ **حالات المناوبات مرمزة بالألوان**  
✅ **السحب والإفلات لتعديلات المناوبات بسهولة**

### **2️⃣ تحسينات واجهة المستخدم 🎨**
✅ **حركات وانتقالات سلسة للتنقل**  
✅ **شريط تنقل سفلي للأجهزة المحمولة**  
✅ **خيارات عرض الشبكة والقائمة لتصور أفضل للبيانات**  
✅ **عرض المناوبات المتبقية للشهر الحالي في لمحة**

### **3️⃣ بحث وتصفية متقدم 🔎**
✅ **البحث عن المناوبات حسب:**
   - **التاريخ** 📅
   - **المستشفى** 🏥
   - **نوع المناوبة** 🌙☀️
   - **حالة المناوبة** ✅❌💰🔄
✅ **تصفية ديناميكية للنتائج الفورية**

### **4️⃣ الإشعارات والتذكيرات 🔔**
✅ **تذكيرات قبل 24 ساعة من بدء المناوبة**  
✅ **إشعارات لتحديثات المناوبات والمبيعات أو التبادلات**  
✅ **إشعارات داخل التطبيق تظهر مباشرة في لوحة التحكم**

### **5️⃣ مشاركة الجدول عبر واتساب 📤**
✅ **مشاركة جدول المناوبات بنقرة واحدة**  
✅ **تصدير المناوبات بصيغة PDF أو Excel**

### **6️⃣ تحسينات الأداء ⚡**
✅ **تخزين مؤقت Redis لتقليل استعلامات MySQL**  
✅ **التحميل الكسول في Vue 3 لأداء أسرع**  
✅ **عرض مادي للجداول الزمنية الثقيلة**

### **7️⃣ دعم تطبيق الويب التقدمي (PWA) 📱**
✅ **وضع عدم الاتصال للوصول إلى المناوبات بدون إنترنت**  
✅ **قابل للتثبيت على الأجهزة المحمولة**  
✅ **مزامنة في الخلفية عند إعادة الاتصال بالإنترنت**

---

## **🔹 المميزات التقنية 🛠️**

### **1️⃣ الواجهة الخلفية (Laravel 11 وتحسين جانب الخادم) 🔧**
- **نمط المستودعات والخدمات**
- **نظام الطوابير (المهام والعمال)**
- **هندسة مدفوعة بالأحداث**
- **فئات موارد API**

### **2️⃣ قاعدة البيانات والتخزين المؤقت 🔍**
- **MySQL 8 / PostgreSQL** مع **فهرسة متقدمة**
- **تخزين مؤقت Redis لتحسين الاستعلامات**
- **Eloquent ORM مع التحميل الحريص والكسول**

### **3️⃣ الواجهة الأمامية (Vue 3 وأطر واجهة المستخدم) 🎨**
- **Vue 3 + Vite لأداء أسرع**
- **Pinia لإدارة الحالة**
- **Tailwind CSS + DaisyUI/Flowbite لواجهة مستخدم عصرية**
- **Vue Router 4 للتنقل**

### **4️⃣ النشر والتطوير 🚀**
- **Docker + Laravel Sail للحاويات**
- **GitHub Actions للأتمتة المستمرة**
- **PM2 + Nginx لإدارة الخادم**

---

## **🔹 هيكل قاعدة البيانات 🗄**

### **🔹 الجداول الرئيسية**
#### **1️⃣ جدول المستخدمين**
| العمود | النوع | التفاصيل |
|--------|------|-----------|
| `id` | UUID | المفتاح الرئيسي |
| `name` | String | اسم المستخدم |
| `email` | String | البريد الإلكتروني الفريد |
| `google_id` | String | معرف Google الفريد |
| `created_at` | Timestamp | تاريخ الإنشاء |

#### **2️⃣ جدول المستشفيات**
| العمود | النوع | التفاصيل |
|--------|------|-----------|
| `id` | UUID | المفتاح الرئيسي |
| `name` | String | اسم المستشفى |
| `user_id` | UUID | مفتاح خارجي (جدول المستخدمين) |
| `created_at` | Timestamp | تاريخ الإنشاء |

#### **3️⃣ جدول الأشهر**
| العمود | النوع | التفاصيل |
|--------|------|-----------|
| `id` | UUID | المفتاح الرئيسي |
| `hospital_id` | UUID | مفتاح خارجي (جدول المستشفيات) |
| `month_year` | String | مثال: "5-2025" |
| `created_at` | Timestamp | تاريخ الإنشاء |

#### **4️⃣ جدول أيام العمل**
| العمود | النوع | التفاصيل |
|--------|------|-----------|
| `id` | UUID | المفتاح الرئيسي |
| `month_id` | UUID | مفتاح خارجي (جدول الأشهر) |
| `date` | Date | تاريخ المناوبة |
| `work_type` | Enum | ("مناوبة ليلية" أو "مناوبة طويلة") |
| `status` | Enum | ("حضور", "بيع", "تبادل", "غياب") |
| `employee_name` | String | اسم الممرض (للمناوبات المباعة أو المتبادلة) |
| `exchanged_date` | Date | تاريخ المناوبة المتبادلة |
| `created_at` | Timestamp | تاريخ الإنشاء |

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
- **Laravel** for backend.
- **Vue 3** for frontend.
- **MySQL** for the database.

### **2️⃣ UI Framework**
- **Tailwind CSS** for a responsive and clean design.
- **DaisyUI or Flowbite** for improved UI components.
- **Dark Mode support.**

---

## **🔹 New Features & Enhancements 🚀**

### **1️⃣ Timeline View for Shifts (Google Calendar Style) 📅**
✅ **Visual timeline of shifts for easy scheduling**  
✅ **Color-coded shift statuses**  
✅ **Drag & Drop for easy shift modifications**

### **2️⃣ Enhanced UI/UX Improvements 🎨**
✅ **Animations & Transitions for smoother navigation**  
✅ **Bottom Navigation Bar for mobile devices**  
✅ **Grid View and List View options for better data visualization**  
✅ **Display the remaining shifts for the current month at a glance**  

### **3️⃣ Advanced Search & Filtering 🔎**
✅ **Search shifts by:**  
   - **Date** 📅  
   - **Hospital** 🏥  
   - **Shift Type** 🌙☀️  
   - **Shift Status** ✅❌💰🔄  
✅ **Dynamic filtering for real-time results**

### **4️⃣ Notifications & Reminders 🔔**
✅ **Reminders for upcoming shifts sent a day before**  
✅ **Push notifications for shift updates, sales, or exchanges**

### **5️⃣ Direct Sharing of Schedule via WhatsApp 📤**
✅ **One-click WhatsApp sharing of the shift schedule**  
✅ **Export shifts as PDF or Excel for easy sharing**

### **6️⃣ Performance Optimizations ⚡**
✅ **Redis Caching to reduce MySQL queries**  
✅ **Lazy Loading in Vue 3 for faster performance**  

### **7️⃣ Progressive Web App (PWA) Support 📱**
✅ **Offline mode for accessing shifts without internet**  
✅ **Installable on mobile devices**  
✅ **Background sync when reconnected to the internet**

---

## **🔹 Enhanced Features & Optimizations 🚀**

### **📅 Advanced Timeline & Calendar View**
- **Improved horizontal timeline display:**
  - 🗓 **Google Calendar-style** interface
  - 📊 **Week/Month grid views** for better clarity
  - 🌓 **Auto Dark Mode** based on system settings
  - 🎨 **Color-coded shifts** for better visibility
  - 🔄 **Drag-and-drop** shift management

### **🔔 Enhanced Notification System**
- **Multi-channel notifications:**
  - ⏰ **24-hour advance** shift reminders
  - 📊 **Monthly remaining shifts** summary
  - 📱 **In-app dashboard notifications**
  - 🔄 **Automatic status updates** after shift day
  - 📲 **PWA push notifications** (Firebase-independent)

### **⚡ Performance & Database Optimizations**
- **Advanced query optimization:**
  - 📊 **Materialized Views** for faster schedule display
  - 🔄 **Smart Cache Invalidation** in Redis
  - 🚀 **Lazy Loading** for external libraries:
    - 📈 Chart.js
    - 📅 FullCalendar.js
    - 📑 PDF Export module
  - 📱 **PWA enhancements:**
    - 💾 **Offline support**
    - 📲 **One-click installation**
    - 🔄 **Background sync**

---

## **🔹 Technical Stack 🛠️**

### **1️⃣ Backend (Laravel 11 & Server-Side Optimization) 🔧**
- **Repositories + Services Pattern**
- **Queue System (Jobs & Workers)**
- **Event-Driven Architecture**
- **API Resource Classes**

### **2️⃣ Database & Caching 🔍**
- **MySQL 8 / PostgreSQL** with **Advanced Indexing**
- **Redis Caching for query optimization**
- **Eloquent ORM with Eager Loading & Lazy Loading**

### **3️⃣ Frontend (Vue 3 & UI Frameworks) 🎨**
- **Vue 3 + Vite for faster performance**
- **Pinia for state management**
- **Tailwind CSS + DaisyUI/Flowbite for a modern UI**
- **Vue Router 4 for navigation**

### **4️⃣ DevOps & Deployment 🚀**
- **Docker + Laravel Sail for containerization**
- **GitHub Actions for CI/CD automation**
- **PM2 + Nginx for server management**

---

## **🔹 Additional Features & Enhancements**

### **📊 Enhanced Shift Audit Log**
- **Comprehensive tracking system:**
  - 📝 Record **all shift status changes** with timestamps
  - 👤 Track **who made each modification**
  - 📅 Maintain **long-term shift history**
  - 🔄 **Automatic date forwarding** for consecutive shifts
  - 📋 **Detailed audit trail** of all actions

### **📱 Advanced Mobile Experience**
- **Fully responsive design optimized for mobile:**
  - 📲 **Touch-friendly** interface
  - 📊 **Mobile-optimized** data views
  - 🔄 **Swipe gestures** for common actions
  - 📱 **Bottom navigation** for easier thumb access
  - 💫 **Smooth animations** for better UX

### **📤 Enhanced Export & Calendar Features**
- **Multiple export options:**
  - 📑 **PDF export** with customizable layouts
  - 📅 **Google Calendar integration:**
    - 🔄 **Automatic sync** of new shifts
    - 🔔 **Calendar reminders**
    - 📲 **Mobile calendar** support
  - 📊 **Excel export** for data analysis

### **✅ Improved Data Validation**
- **Robust validation system:**
  - 🚫 **Prevent duplicate shifts** on same day
  - ⚠️ **Smart conflict detection**
  - 🔍 **Real-time validation** checks
  - 📋 **Custom validation rules** per hospital

---

## **🔹 Database Schema 🗄**

### **🔹 Main Tables**
#### **1️⃣ Users Table**
| Column        | Type      | Details                  |
|--------------|----------|--------------------------|
| `id`         | UUID     | Primary Key              |
| `name`       | String   | User's Name              |
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
| `employee_name` | String | Nurse's name (for Sold or Exchanged shifts) |
| `exchanged_date` | Date  | New date for exchanged shift                |
| `created_at` | Timestamp | Creation Date                               |

---

## **🔹 Laravel Folder Structure 📂**

```
my-app/
│── app/
│── resources/views/
│── routes/
│── database/migrations/
│── public/
│── config/
│── storage/
│── composer.json
│── package.json
│── .env
│── .gitignore
```
