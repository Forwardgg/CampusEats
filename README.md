# CampusEats

CampusEats is a Laravel-based campus food ordering system designed to connect students, vendors, and administrators on a single platform. The system allows students to order food from campus vendors, vendors to manage menus and orders, and administrators to control and monitor the platform.

---

## User Roles

The system supports three types of users:

- Students (Users)
- Vendors (Clients)
- Administrators (Admins)

Each role has its own authentication guard and dashboard.

---

## Student Features
Role: `users`  
Authentication: `web` guard

### Ordering and Wishlist
- Browse restaurants and food products
- Filter food products
- Add items to cart
- Place orders
- Apply coupons during checkout
- Add restaurants to wishlist

### Order Management
- View order list and order details
- Download invoice as PDF
- Track order status:
  - Pending
  - Confirmed
  - Processing
  - Delivered

### Profile Management
- Update name, email, password
- Upload profile photo
- Update phone and address
- View and edit profile

### Ratings and Reviews
- Submit ratings and feedback for vendors
- View vendor review breakdown

---

## Vendor Features
Role: `clients`  
Authentication: `client` guard

### Menu and Product Management
- Add, edit, and delete products
- Upload product images
- Set prices and discounts
- Organize products by category, menu, and city

### Gallery Management
- Add, edit, and delete restaurant gallery images

### Coupon Management
- Create and manage discount coupons
- Set coupon validity
- Target specific users

### Order Fulfillment
- View incoming orders grouped by Order ID
- Mark orders as Processing and Delivered
- View detailed order information per product

### Reports
- Filter order reports by date, month, and year

### Profile Management
- Update restaurant profile
- Manage cover photo, address, and phone
- Change vendor password

---

## Admin Features
Role: `admins`  
Authentication: `admin` guard

### Product and Category Management
- View, add, edit, and delete products
- Manage food categories
- Manage cities

### Order Control
- View and manage all orders
- Update order status:
  Pending → Confirm → Processing → Delivered

### Banner Management
- Upload and manage homepage banners

### Vendor Approval
- Approve or reject new vendors
- Change vendor status

### Reports
- View and filter reports by date, month, and year

### Review Moderation
- Approve or reject vendor reviews

### Admin Dashboard
- View key statistics
- Update admin profile and password

---

## Security and Access Control
- Role-based route protection using guards and middleware
- Separate login panels for Admin, Vendor, and Student
- Session-based authentication and access control

---

## Installation

Clone the repository:

```bash
git clone https://github.com/DBMSproj-ui/CampusEats.git
cd CampusEats
```

Install dependencies:

```bash
composer install
npm install
npm run dev
```

Environment setup:

```bash
cp .env.example .env
php artisan key:generate
```

Database setup:

```bash
php artisan migrate
```

Run the application:

```bash
php artisan serve
```

---

## Git Workflow

```bash
git add .
git commit -m "Added X feature"
git push
```

---

## Tech Stack

Backend:
- Laravel

Frontend:
- Blade / Laravel UI
- JavaScript
- CSS

Database:
- MySQL

Other Tools:
- Composer
- NPM
- PDF generation
