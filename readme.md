# Hotel Booking System

A full-featured hotel and vacation rental booking platform built with PHP, MySQL, and Bootstrap. This application allows users to browse hotels, view rooms, and make bookings, while providing a comprehensive admin panel for hotel and property management.

## Features

### For Users

-   **Browse Hotels & Rooms** - View all available hotels and room listings
-   **Room Details** - Detailed information about each room with images and amenities
-   **Online Booking** - Reserve rooms directly through the platform
-   **Secure Payment** - Integrated payment processing for bookings
-   **User Registration & Login** - Create accounts and manage bookings
-   **Booking Management** - View and manage your reservations
-   **Contact & Support** - Get in touch with the booking team

### For Administrators

-   **Admin Dashboard** - Overview of hotels, rooms, admins, and bookings
-   **Hotel Management** - Create, update, and manage hotel properties
-   **Room Management** - Manage room listings and availability
-   **Booking Administration** - View and manage customer bookings
-   **Admin User Management** - Create and manage admin accounts
-   **Status Control** - Enable/disable hotels and rooms

## Project Structure

```
hotel-booking/
├── admin-panel/              # Admin dashboard and management
│   ├── admins/              # Admin authentication & user management
│   ├── hotels-admins/       # Hotel management pages
│   ├── rooms-admins/        # Room management pages
│   ├── bookings-admins/     # Booking management
│   ├── layouts/             # Admin header/footer templates
│   └── styles/              # Admin-specific styles
├── auth/                    # User authentication (login/register)
├── config/                  # Database configuration
├── css/                     # Frontend stylesheets
├── js/                      # JavaScript libraries & custom scripts
├── includes/                # Reusable components (header, footer)
├── rooms/                   # Room details & payment pages
├── users/                   # User booking management
├── scss/                    # SCSS source files
├── fonts/                   # Custom fonts (Flaticon)
├── images/                  # Image assets
├── index.php               # Homepage
├── rooms.php               # Rooms listing page
├── services.php            # Services page
├── about.php               # About page
├── contact.php             # Contact page
└── 404.php                # Error page
```

## Requirements

-   **PHP** 7.0+
-   **MySQL** 5.7+
-   **Web Server** (Apache with mod_rewrite)
-   **PHP PDO Extension** (for database operations)

## Installation

### 1. Clone or Download the Project

```bash
cd /var/www/html
# Download or clone the project into hotel-booking folder
```

### 2. Create Database

Create a MySQL database for the application:

```sql
CREATE DATABASE hotel_booking;
```

### 3. Configure Database Connection

1. Navigate to `config/` folder
2. Rename `config.example.php` to `config.php`
3. Update the configuration with your database credentials:

```php
define("HOST", "localhost");
define("DBNAME", "hotel_booking");
define("USER", "your_db_user");
define("PASS", "your_db_password");
```

### 4. Set Up Database Tables

Import the database schema (if a schema file exists) or create the required tables:

-   `hotels` - Hotel properties
-   `rooms` - Room listings
-   `admins` - Admin user accounts
-   `bookings` - User reservations
-   `users` - User accounts (if applicable)

### 5. Configure Web Server

Ensure your Apache configuration allows URL rewriting and the project is accessible via your web server.

### 6. Access the Application

-   **Frontend** - http://localhost/hotel-booking
-   **Admin Panel** - http://localhost/hotel-booking/admin-panel

## Usage

### For Users

1. Visit the homepage and browse available hotels and rooms
2. Click on a room to view details
3. Click "Book Now" or proceed to payment
4. Register or login to complete your booking
5. Manage your bookings in the user dashboard

### For Administrators

1. Access the admin panel at `/admin-panel/`
2. Login with admin credentials
3. From the dashboard, you can:
    - Manage hotels and their status
    - Manage room listings and availability
    - View and process bookings
    - Manage other admin users

## Key Files

-   **[config/config.php](config/config.php)** - Database configuration
-   **[index.php](index.php)** - Homepage with hotel and room listings
-   **[admin-panel/index.php](admin-panel/index.php)** - Admin dashboard
-   **[auth/login.php](auth/login.php)** - User login
-   **[auth/register.php](auth/register.php)** - User registration
-   **[rooms/pay.php](rooms/pay.php)** - Payment processing
-   **[includes/header.php](includes/header.php)** - Frontend header template
-   **[admin-panel/layouts/header.php](admin-panel/layouts/header.php)** - Admin header template

## Technologies Used

-   **Backend** - PHP with PDO
-   **Database** - MySQL
-   **Frontend** - HTML5, CSS3, Bootstrap
-   **Libraries** - jQuery, Owl Carousel, Magnific Popup, Bootstrap Datepicker
-   **Icons** - Flaticon

## Security Notes

-   Always use prepared statements and PDO for database queries (already implemented)
-   Keep `config.php` out of version control
-   Use HTTPS in production
-   Validate and sanitize all user inputs
-   Implement proper session management
-   Use password hashing for user accounts

## Future Enhancements

-   Email notifications for bookings
-   Payment gateway integration (Stripe, PayPal, etc.)
-   Advanced search and filtering
-   User reviews and ratings
-   Multi-language support
-   Mobile app
-   Analytics dashboard

## License

This project is provided as-is for educational and commercial purposes.

## Support

For issues or questions, please contact the development team or submit an issue through your project management system.

---

**Last Updated:** December 2025
