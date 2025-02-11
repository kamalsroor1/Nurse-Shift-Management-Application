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
