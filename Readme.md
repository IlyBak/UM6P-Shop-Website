# 🛍️ UM6P Shop Website

A dynamic and responsive **e-commerce shopping platform** designed for the UM6P university shop.  
This project includes full shopping functionality such as product browsing, authentication, cart management, and admin controls.

---

## 🚀 Features

### 👤 User Features
- **User Authentication** — Secure registration & login system  
- **Product Catalog** — Browse products by category with filters  
- **Search System** — Quickly find products  
- **Shopping Cart** — Add/remove items and manage quantities  
- **Wishlist** — Save favorite products  
- **Quick View** — Preview products without leaving the page  
- **Order Management** — Track orders and view history  
- **Responsive Design** — Works on desktop, tablet, and mobile  

### 🛠️ Admin Features
- **Admin Dashboard**
- Manage products (Add / Edit / Delete)
- View customer orders
- Update inventory and pricing  

---

## 📋 Tech Stack

| Technology | Usage |
|----------|------|
| **PHP** | Backend logic (73.3%) |
| **CSS** | Styling & responsiveness (25.3%) |
| **JavaScript** | Interactivity (1.4%) |
| **MySQL** | Database |
| **Swiper JS** | Product sliders |
| **Font Awesome** | Icons |

---

## 📁 Project Structure

```
UM6P-Shop-Website/
├── home.php                # Homepage
├── shop.php                # Shop page
├── category.php            # Category filtering
├── product details & cart/
│   ├── quick_view.php
│   ├── cart.php
│   ├── checkout.php
│   └── wishlist.php
├── user management/
│   ├── user_register.php
│   ├── user_login.php
│   ├── update_user.php
│   └── orders.php
├── search_page.php
├── about.php
├── contact.php
├── admin/
├── components/
│   ├── connect.php
│   ├── user_header.php
│   ├── footer.php
│   └── wishlist_cart.php
├── css/
│   └── style.css
├── js/
│   └── script.js
├── images/
├── uploaded_img/
└── shop_db.sql
```

---

## 🛠️ Installation & Setup

### 📌 Prerequisites
- PHP 7.0+
- MySQL 5.7+
- Apache/Nginx
- Composer (optional)

---

### ⚙️ Step 1: Clone Repository
```bash
git clone https://github.com/IlyBak/UM6P-Shop-Website.git
cd UM6P-Shop-Website
```

---

### 🗄️ Step 2: Database Setup
```sql
CREATE DATABASE um6p_shop;
```

```bash
mysql -u root -p um6p_shop < shop_db.sql
```

---

### 🔧 Step 3: Configure Database

Edit `components/connect.php`:

```php
<?php
$db_name = 'um6p_shop';
$db_user = 'root';
$db_pass = '';
$db_host = 'localhost';

$conn = new PDO("mysql:host=$db_host;dbname=$db_name", $db_user, $db_pass);
?>
```

---

### 🌐 Step 4: Apache Configuration (.htaccess)

```apache
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule ^(.*)$ index.php?path=$1 [NC,L,QSA]
```

---

### 🔐 Step 5: File Permissions

```bash
chmod 755 uploaded_img/
chmod 755 images/
```

---

### ▶️ Step 6: Run the App

Start your server and open:

```
http://localhost/UM6P-Shop-Website/home.php
```

---

## 📖 Usage Guide

### 👤 Users
- Register or login
- Browse products via homepage or categories
- Search for items
- Add to cart & checkout
- Save items to wishlist
- View order history
- Update account info  

---

### 🛠️ Admin
- Access: `/admin/`
- Manage products
- View orders
- Update stock & prices  

---

## 🎨 Key Pages

| Page | Purpose |
|------|--------|
| `home.php` | Landing page |
| `shop.php` | Full catalog |
| `category.php` | Filter by category |
| `quick_view.php` | Product preview |
| `cart.php` | Cart management |
| `checkout.php` | Order processing |
| `user_login.php` | Login |
| `user_register.php` | Registration |
| `orders.php` | Order history |

---

## 🗄️ Database Schema

Main tables:
- `users`
- `products`
- `categories`
- `cart`
- `wishlist`
- `orders`
- `order_items`

---

## 🎯 Dependencies

- Swiper JS v8
- Font Awesome 6.1.1
- Bootstrap (optional)

---

## 🤝 Contributing

1. Fork the repo  
2. Create branch:
```bash
git checkout -b feature/amazing-feature
```
3. Commit:
```bash
git commit -m "Add amazing feature"
```
4. Push:
```bash
git push origin feature/amazing-feature
```
5. Open Pull Request  

---

## 🐛 Known Issues

| Issue | Solution |
|------|--------|
| 404 errors | Check `.htaccess` |
| DB connection fails | Verify credentials |
| Images not loading | Check folder permissions |
| Sessions issues | Ensure `session_start()` |

---

## 🔐 Security Notes

- Use HTTPS in production  
- Store credentials in environment variables  
- Validate all inputs  
- Use prepared statements (✔ already done)  
- Add CSRF protection  
- Secure admin panel  

---

## 📚 Resources

- PHP Documentation  
- MySQL Documentation  
- PDO Tutorial  
- Swiper JS Docs  

---

## 📝 License

This project is part of the **UM6P university shop initiative**.

---

## 👨‍💻 Author

**Ilyas Bakri**  
GitHub: https://github.com/IlyBak 
Email : bilyas12345@gmail.com
Linkedin : linkedin.com/in/ilyas-bakri-1b1162304 

---

## 📧 Support

- Use the contact form (`contact.php`)
- Open a GitHub issue  
- Contact the dev team  

---

### 📌 Version Info
- **Version:** 1.0.0  
- **Last Updated:** April 2026  