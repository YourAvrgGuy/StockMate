```
StockMate is a basic, interactive, and modern mobile Inventory Management System built for Android using Kotlin, Jetpack Compose, and Room Database.
The application provides an intuitive mobile platform for small business owners, retail managers, and storekeepers to create and manage local product inventories, track real-time stock levels, record customer sales transactions, automatically compute net profit margins, and perform seamless cloud backups directly to Google Drive.
The app is built following standard Android architecture principles, utilizing Kotlin Coroutines and Flows for reactive real-time database updates, custom high-contrast input fields for dark/light theme compatibility, and Storage Access Framework (FileProvider) for direct Google Drive JSON file backup and restore.

⚠️ Problem Addressed
Traditional manual inventory tracking (using paper ledgers, notebooks, or manual spreadsheet logging) faces critical operational problems:
1. Human Calculation Errors: Manual math often leads to inaccurate stock balances, incorrect pricing totals, and flawed profit accounting.
2. Delayed Stock Visibility: Store owners cannot instantly see which products are running low or out of stock, leading to delayed restocks and lost sales.
3. Accidental Clicks & Miscalculated Sales: Fast-paced customer checkout often leads to accidental duplicate entries or wrong quantities. Without a built-in undo/restock mechanism, correcting ledger mistakes is difficult and prone to errors.
4. Data Loss & Device Dependency: Paper notebooks can be lost or damaged, while local desktop spreadsheets are difficult to access on the go.
5. Legibility & Theme Issues: Many mobile apps suffer from low-contrast input fields where white text on light backgrounds becomes unreadable when device dark mode is toggled.
StockMate solves these issues by providing an automated, real-time mobile app with instant visual stock indicators, automated net profit tracking, an Undo / Restock feature for accidental sales, high-contrast inputs, and direct Google Drive JSON backups.

🎯 Objectives
• Objective 1: Simple & Interactive Mobile UI — Provide a clean, light-blue user interface tailored for first-year college project presentation and everyday mobile usability.
• Objective 2: Real-time Stock Monitoring — Automate inventory counts and display color-coded status badges (In Stock, Low Stock, Out of Stock).
• Objective 3: Robust Input Validation & Duplicate Prevention — Strictly validate user input (prevent negative numbers or empty fields) and block duplicate Product IDs in Room Database.
• Objective 4: Automated Point-of-Sale & Profit Tracking — Automatically decrease stock when customer purchases are recorded and compute net profits in real-time (Net Profit = (Selling Price - Cost Price) × Qty).
• Objective 5: Error Correction (Undo / Restock) — Provide an Undo / Restock mechanism to void miscalculated sales and return items to stock immediately.
• Objective 6: Google Drive Cloud Integration — Allow users to export and import complete JSON database backups directly to their phone's Google Drive app.

🚀 Features
1. Start Screen & Onboarding
• Create New Inventory: Input store name and choose between Local Storage or Google Drive Cloud Backup.
• Load Existing Inventory: Automatically retrieves saved inventory preferences from local SharedPreferences.
• Smart Navigation: Automatically routes returning users to their active Dashboard.
2. Real-Time Interactive Dashboard
•
Real-time Overview Cards: Displays live statistics observed directly from Room Database via Kotlin Flows:
◦ 📦 Total Products Count
◦ 🔢 Total Items Quantity
◦ 💵 Total Revenue ($)
◦ 📈 Total Net Profit ($)
• Main Action Cards: One-tap access to Add Product, Edit / Update Product, Check Stock, and Customer Sales & Profit History.
• Database Reset Safety: A Clear All Inventory Data button protected by an alert confirmation dialog.

# 3. Add Product Form
• Form Fields: Product ID, Product Name, Category (with quick-select category chips), Quantity, Selling Price (), Cost Price (), Description, and Date Added.
• Input Validation:
◦ Prevents negative values for quantities and prices.
◦ Disallows empty required fields.
◦ Rejects duplicate Product IDs in the Room Database.
• High-Contrast Styling: Custom StyledOutlinedTextField enforcing pitch-black/dark gray text for readability in both light and dark system themes.

# 4. Search & Edit / Update Product
• Smart Product Search: Search by Product ID or Name.
• Error Handling: Displays a "Product Not Found" red card with a Retry Search button if no match exists.
• Selection List: Shows a selectable list if multiple products match a search query.
• Editable Form: Populates existing details for editing while keeping Product ID in read-only mode to preserve primary key integrity.
• Delete Product: Dedicated button with a confirmation popup dialog to remove items safely.

# 5. Check Stock & Multi-Filter System
• Live Product List: Reactive display of all stored items.
• Multi-Level Filters:
◦ Real-time search bar (ID, Name, or Category).
◦ Stock Status Chips (All, In Stock, Low Stock, Out of Stock).
◦ Dynamic Category Filter Chips (generated automatically from stored database categories).
• Color-coded Stock Badges:
◦ 🟢 In Stock: Quantity > 10 units.
◦ 🟠 Low Stock: Quantity between 1 and 10 units.
◦ 🔴 Out of Stock: Quantity = 0 units.
• Quick Purchase Action: Includes a 🛒 Sell 1 button directly on each product card.

# 6. Customer Purchases & Automated Profit Engine
•Customer Purchase Dialog: Dropdown selector to choose items and enter quantity sold.
• Automated Stock Decrement: Automatically reduces stock upon purchase.
• Automated Profit Calculation: Net Profit = (Selling Price - Cost Price) × Quantity Sold
• Undo / Restock Feature: One-tap button on Recent Sales to void accidental sales, refund revenue, and restock items back into inventory.
7. Direct Google Drive Cloud Backup & Restore
• Direct Drive Upload: Packages all products, quantities, prices, sales, and profits into a formatted JSON backup file (stockmate_backup.json) and opens the Google Drive app (Save to Drive) via FileProvider.
• Cloud Restore: Pick and import backup JSON files from Google Drive to restore inventory records onto any Android device.



```
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
