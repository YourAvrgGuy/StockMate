
# StockMate — Inventory Management System
**Version:** `1.0.1`

---

## 📌 Project Description
**StockMate** is a basic, clean, and interactive mobile **Inventory Management System** developed for Android using **Kotlin**, **Jetpack Compose**, and **Room Database**. 

The application is designed to help small business owners, retail shopkeepers, and store managers keep track of their product stock, record customer purchases, calculate net profits automatically, and maintain real-time inventory records locally on their Android devices with seamless **Google Drive** cloud backup integration.

---

## ⚠️ Problem Addressed
Traditional manual stock tracking (using paper logbooks or spreadsheets) presents several challenges for small businesses:
1. **Human Error & Discrepancies**: Manual calculations often lead to incorrect stock counts, miscalculated prices, and inaccurate profit estimations.
2. **Lack of Real-Time Visibility**: Business owners struggle to quickly identify low stock or out-of-stock items, leading to lost sales opportunities.
3. **Accidental Clicks & Miscalculations**: When recording sales quickly, accidental duplicate entries or incorrect quantity inputs are difficult to track and correct without messing up stock ledgers.
4. **Data Loss Risks**: Physical notebooks or local desktop spreadsheets can be easily damaged, misplaced, or lost without an easy cloud backup mechanism.

**StockMate** addresses these problems by providing an automated, real-time mobile solution that tracks quantities, calculates profits automatically, offers an **Undo/Restock** feature for accidental entries, and enables direct backup to Google Drive.

---

## 🎯 Objectives
* To create an easy-to-use, beginner-friendly mobile inventory management system with a modern light-blue user interface.
* To automate stock level tracking and provide color-coded visual indicators for **In Stock**, **Low Stock**, and **Out of Stock** items.
* To prevent duplicate entry errors by strictly validating Product IDs and numerical inputs.
* To simplify point-of-sale customer purchases and calculate **Total Revenue** and **Net Profit** in real-time.
* To enable users to void/undo mistaken sales and restock items back into inventory automatically.
* To provide reliable data storage using Room SQLite Database and allow easy export/import backups to **Google Drive**.

---

## 🚀 Features

### 1. Welcome & Onboarding Screen
* **Create New Inventory**: Allows users to set up a new inventory name and select storage preferences (Local vs. Google Drive Backup).
* **Load Existing Inventory**: Instantly retrieves saved inventory settings from local storage (`SharedPreferences`).

### 2. Real-Time Interactive Dashboard
* **Overview Stats**: Live display of **Total Products**, **Total Item Quantity**, **Total Revenue ($)**, and **Net Net Profit ($)**.
* **Navigation Action Cards**: Direct buttons to *Add Product*, *Edit/Update Product*, *Check Stock*, and *Customer Sales & Profit History*.
* **Database Reset Safety**: A **Clear All Inventory Data** option protected by a confirmation alert dialog.

### 3. Add Product Form
* **Fields**: Product ID, Product Name, Category (with quick-select category chips), Quantity, Selling Price ($), Cost Price ($), Description, and Date Added.
* **Validation**: Rejects negative numbers for quantities/prices and blocks duplicate Product IDs.
* **High-Contrast Input**: Custom high-contrast text fields ensuring entered text is pitch-black and crystal clear in both Light and Dark phone themes.

### 4. Search & Edit / Update Product
* **Smart Search**: Search by Product ID or Name.
* **Error Handling**: Displays a **"Product Not Found"** red card with a **Retry Search** button if no matching item exists.
* **Edit & Update**: Pre-fills existing details for modification while keeping Product IDs read-only to preserve primary key database integrity.
* **Delete Product**: Includes a confirmation popup dialog before deleting a product.

### 5. Check Stock & Multi-Filter System
* **Real-time Search & Filter**: Filter items dynamically by keyword, Stock Status (*In Stock*, *Low Stock*, *Out of Stock*), and Product Category.
* **Visual Status Badges**:
  * 🟢 **In Stock**: Quantity > 10 units.
  * 🟠 **Low Stock**: Quantity between 1 and 10 units.
  * 🔴 **Out of Stock**: Quantity = 0 units.
* **Quick Purchase Button**: Includes a `🛒 Sell 1` button directly on each product card for quick processing.

### 6. Customer Sales & Net Profit Engine
* **Record Customer Purchase**: Dropdown selector to choose products and record quantity sold.
* **Automated Stock Decrement**: Automatically reduces inventory quantity upon sale.
* **Automated Profit Calculation**:
  $$\text{Net Profit} = (\text{Selling Price} - \text{Cost Price}) \times \text{Quantity Sold}$$
* **Undo / Restock Feature**: One-tap button to void miscalculated or accidental sales, refund revenue, and restock items back into inventory automatically.

### 7. Google Drive Cloud Backup & Restore
* **Upload to Google Drive**: Uses Android `FileProvider` to generate a formatted JSON file (`backup.json`) and opens the Google Drive app directly for 1-tap folder saving.
* **Restore from Drive**: Pick and import backup JSON files from Google Drive to restore products and sales logs on any phone.

---

## 🛠️ Technologies Used

* **Programming Language:** Kotlin (`2.1.10`)
* **Integrated Development Environment (IDE):** Android Studio (Ladybug / 2026.2.1+)
* **User Interface (UI):** Jetpack Compose with Material 3 Design System
* **Local Database:** Room SQLite Database (`2.8.5`)
* **Annotation Processing:** KSP (*Kotlin Symbol Processing*) (`2.1.10-1.0.30`)
* **Asynchronous Processing:** Kotlin Coroutines & `Flow`
* **File Sharing & Cloud Integration:** Android Storage Access Framework (SAF) & `FileProvider`
* **Build System:** Gradle (Kotlin DSL `build.gradle.kts`) with Version Catalog (`libs.versions.toml`)
* **Minimum Android Version:** Android 7.0 (API Level 24 - Nougat)
* **Target Android Version:** Android 15 (API Level 37)

---

## 💻 Installation and Setup

### Prerequisites
1. Install [Android Studio](https://developer.android.com/studio) (2024.1.1 or newer recommended).
2. Install JDK 11 or JDK 17 (configured in Android Studio).
3. An Android device running Android 7.0+ or an Android Emulator.

### Steps to Run the Application
1. **Clone or Download the Project**:
   Extract the `StockMate` project folder to your local computer directory.
2. **Open in Android Studio**:
   * Open Android Studio.
   * Click **File ➔ Open** and select the `StockMate` directory.
3. **Gradle Sync**:
   * Wait for Android Studio to index and download the dependencies automatically.
   * If prompted, click **Sync Project with Gradle Files**.
4. **Run the Project**:
   * Select an active Android Emulator or connect a physical Android device via USB Debugging.
   * Click the green **Run (`Shift + F10`)** button in Android Studio to build and install `app-debug.apk`.

---

## 📸 Screenshots


| 1. Start Screen | 2. Dashboard | 3. Add Product Form |
| :---: | :---: | :---: |
| ![Start Screen](/StockMateProject/screenshots/SMStartScreen.png) | ![Dashboard](StockMateProject/screenshots/SmDashboard.png) | ![Add Product](StockMateProject/screenshots/SMAddNewProduct.png) |

| 4. Check Stock & Filters | 5. Edit Product | 6. Sales & Profit History |
| :---: | :---: | :---: |
| ![Check Stock](StockMateProject/screenshots/SMCheckStock.png) | ![Edit Product](StockMateProject/screenshots/SMEditProduct.png) | ![Sales History](StockMateProject/screenshots/SMCustomerProfit.png) |

---

## 👥 Developers

* **Lead Developer / Contributor**: `"Prince Centeno",
"Mark Pedong",
"Dela Cruz Joshue",
`
* **Group Member**: `Johnrick Opena`
* **Group Member**: `Mark Jerome Valdez`
* **Group Member**: `Limuel Christian Santos`

**Course / Subject:** Mobile Application Development
**Project Version:** `1.0.1`


👉 Click here to read the full [Project Description](project-description.md).

`
