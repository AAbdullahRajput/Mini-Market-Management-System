# 🛒 Mini Market Management System

> A fully-featured desktop application built with C# WinForms for managing a mini market's daily operations — including login, product management, category management, seller management, and a complete billing/selling system.

---

## ✨ Features

| Module | Description |
|--------|-------------|
| 🔐 Login System | Secure seller authentication with username & password |
| 📦 Product Management | Add, update, delete and view products |
| 🗂️ Category Management | Organize products into categories |
| 👤 Seller Management | Manage seller accounts with name, age, phone & password |
| 🧾 Selling / Billing | Generate bills, select products by category, print receipts |
| 🖨️ Print Support | Built-in DataGridView printer for billing |
| 💅 Modern UI | Styled with Guna UI2 WinForms library |

---

## 🛠️ Tech Stack

| Technology | Details |
|-----------|---------|
| Language | C# |
| Framework | .NET Framework 4.7.2 |
| UI Library | Guna.UI2.WinForms |
| Database | SQL Server LocalDB (.mdf) |
| IDE | Visual Studio |

---

## 🗄️ Database Tables

| Table | Fields |
|-------|--------|
| `Seller` | SellerId, SellerName, Age, Phone, Password |
| `Category` | CatId, CatName, CatDes |
| `Product` | ProdId, ProdName, ProdPrice, Category |
| `Bill` | Billing records with product and seller info |

---

## 📦 Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/AAbdullahRajput/Mini-Market-Management-System.git
```

### 2. Requirements
- Visual Studio 2019 or later
- .NET Framework 4.7.2
- SQL Server LocalDB
- Guna UI2 NuGet package

### 3. Setup the Database
- Create a new database named `minimarketdb` in SQL Server
- Create the required tables (`Seller`, `Category`, `Product`, `Bill`)
- Update the connection string in `DBConnect.cs`:
```csharp
Data Source=(LocalDB)\MSSQLLocalDB;
AttachDbFilename=YOUR_PATH\minimarketdb.mdf;
Integrated Security=True;
```

### 4. Restore NuGet Packages
In Visual Studio:
```
Tools → NuGet Package Manager → Package Manager Console
```
```
Update-Package -reinstall
```

### 5. Run the Project
- Press `F5` in Visual Studio to build and run

---

## 📁 Project Structure

```
Mini_Market Management System/
│
├── LoginForm.cs              # Login & authentication
├── SpalshForm.cs             # Splash screen
├── CategoryForm.cs           # Category CRUD operations
├── ProductForm.cs            # Product CRUD operations
├── SellerForm.cs             # Seller CRUD operations
├── SellingForm.cs            # Billing & selling module
├── DBConnect.cs              # Database connection helper
├── DGVPrinter.cs             # DataGridView print helper
└── App.config                # App configuration
```

---

## 🚀 How to Use

1. Launch the application — splash screen loads first
2. **Login** with seller credentials
3. Navigate to any module:
   - Manage **Categories** → add/edit/delete product categories
   - Manage **Products** → add/edit/delete products with pricing
   - Manage **Sellers** → add/edit/delete seller accounts
   - Go to **Selling** → select category, choose products, generate & print bill

---

## 👨‍💻 Author

**Abdullah Rajput**  
GitHub: [@AAbdullahRajput](https://github.com/AAbdullahRajput)  
Made with ❤️   
© 2026 — All rights reserved
