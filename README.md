# **🏥 Nurse Shift Management Application**

## **🔹 Overview**
This application is designed to help nurses efficiently manage their hospital work schedules. It provides features for shift registration, status management, and recording shift sales or exchanges with other nurses. The application supports multiple hospitals and integrates with Firebase for secure Google login.

---

## **🔹 Application Flow**

### **1️⃣ Login**
- Users first see the **Google Login Page** via Firebase.
- Users **cannot access** any feature before logging in.

### **2️⃣ Hospital Management**
- After login, users see a **list of hospitals** they work at.
- They can:
  - ✅ **Add a new hospital**
  - ✏️ **Edit an existing hospital**
  - ❌ **Delete a hospital**

### **3️⃣ Managing Months**
- Clicking on a hospital opens a **list of registered months.**
- Users can:
  - ✅ **Register a new month**
  - 🗓 **View and manage previous months**
- When registering a new month, users **select the days they will work** and set the **shift type (Night or Long).**

### **4️⃣ Shift Registration**
- After registering the month, users **choose the days they will work in that month.**
- Each day entry includes:
  - ✅ **Date selection**
  - 🌙 **Shift type (Night or Long)**

### **5️⃣ Shift Management**
- Once shifts are registered, users can update their status to:
  - ✅ **Attended** – The shift was completed.
  - ❌ **Absent** – The shift was missed.
  - 💰 **Sold** – The shift was sold to another nurse.
    - 🔹 Users **must enter the nurse's name** who purchased it.
  - 🔄 **Exchanged** – The shift was exchanged with another nurse.
    - 🔹 Users **must select the new shift date**.
    - 🔹 The exchanged shift **is automatically recorded in the new date.**

---

## **🔹 New Features & Enhancements 🚀**

### **1️⃣ Timeline View for Shifts (Google Calendar Style) 📅**
✅ **Visual timeline of shifts for easy scheduling**  
✅ **Color-coded shift statuses**  
✅ **Drag & Drop for easy shift modifications**

### **2️⃣ Enhanced UI/UX Improvements 🎨**
✅ **Modern & Dynamic Design:**
  - 🎯 **Simple & attractive interface** with 3D animations
  - 🌈 **Cohesive color scheme** with calming greens and blues
  - 🌙 **Auto Dark Mode** synced with system settings

✅ **Enhanced User Experience:**
  - 📱 **Bottom navigation bar** for quick access to main tasks
  - 🔄 **Smooth transitions** between screens
  - ➕ **Floating action button** for quick shift registration
  - 🎨 **Expressive icons** for each shift type and status

✅ **Improved Information Organization:**
  - 📊 **Modern cards** for shift details
  - 📅 **Advanced calendar view** similar to Google Calendar
  - 📌 **Upcoming tasks list** on home screen
  - 🔍 **Quick search & filtering** for shifts

✅ **Interface Customization:**
  - 🎛️ **Customizable dashboard**
  - 📱 **Grid or list view** based on user preference
  - 🔔 **Custom notification settings**
  - 📊 **Visual statistics** for monthly shifts

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
✅ **Redis Caching for query optimization**

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
