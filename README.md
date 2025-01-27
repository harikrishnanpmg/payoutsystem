# payoutsystem
This project is a PHP-based multi-level user commission management system. It allows administrators and regular users to manage users, sales, and commissions within a hierarchical structure.

**Features**
User registration and login functionality.
Role-based access: Separate dashboards for admins and regular users.
Multi-level commission system: Commissions are distributed up to 5 levels.
Admin dashboard: View all users, sales, and commission details.
Secure password storage with password_hash for encryption.
AJAX-based dynamic parent user selection during registration.

**Setup Instructions**
__Prerequisites__
A web server with PHP support (e.g., XAMPP, WAMP, or LAMP).
MySQL database.
Git for version control.

**How It Works**
**User Registration**
New users can register through the Register page.
During registration, the parent user dropdown is dynamically populated using AJAX.
**Login**
Users can log in with their email and password.
After successful login:
Admin users are redirected to the admindashboard.php page.
Regular users are redirected to the dashboard.php page.
__Admin Dashboard__
Accessible only to admin users.
Admins can:
View all users in the system.
View sales records and their details.
View commissions distributed across levels.
__Regular User Dashboard__
Accessible to non-admin users.
Users can:
Add sales.
View their commissions.
__Commission Distribution__
When a sale is recorded, the commission is distributed up to 5 levels in the hierarchy.
Beyond the 5th level, no commissions are distributed.
When a user at the 6th level (or below) makes a sale, the system
should distribute a5iliate commissions as follows:
- Level 1 (Direct Parent): 10%
- Level 2: 5%
- Level 3: 3%
- Level 4: 2%
- Level 5: 1%


project-root/
│
├── db.php              # Database connection file
├── login.php           # User login handling
├── logout.php          # User logout handling
├── register.html       # User registration page
├── register.php        # Backend logic for registration
├── dashboard.php       # Regular user dashboard
├── admindashboard.php  # Admin dashboard
├── add_sale.html       # Add sale page
├── add_sale.php        # Backend logic for adding sales
├── styles.css          # Stylesheet for the application
├── affiliate_system.sql        # SQL script for database setup
└── index.html          # Initial page
