# Online Bus Booking System

## Overview
This project is an Online Bus Booking System built using **HTML**, **CSS**, **JavaScript**, **PHP**, and **MySQL**. It allows users to browse available bus routes, book tickets, and manage bookings. Admin users can manage buses, routes, and ticket bookings through the backend system.

## Features
- Browse available buses and routes
- Book bus tickets
- Manage bus categories, routes, and orders
- Admin panel for managing buses and viewing bookings

## Technologies Used
- Frontend: **HTML**, **CSS**, **JavaScript**
- Backend: **PHP**
- Database: **MySQL**

## Project Structure
The project contains the following main files and folders:
- `index.html`: Main landing page
- `booking.php`: Page for booking bus tickets
- `admin.php`: Admin panel for managing buses and bookings
- `db.php`: Database connection file
- `styles.css`: Styles for the frontend
- `scripts.js`: JavaScript for client-side interactions

## Database Setup
To set up the database, follow these steps:

1. Open **phpMyAdmin** (or any MySQL client).
2. Create a new database named `bus`.
3. Import the provided SQL file containing table structures and sample data:
   - **File**: `bus.sql` (The code provided in this README)
   - **Tables included**:
     - categories
     - cost
     - orders
     - posts
     - query
     - seats
     - users

## SQL for Database Tables

```sql
-- Database: `bus`

-- Table structure for table `categories`
CREATE TABLE `categories` (
  `cat_id` int(3) NOT NULL,
  `cat_title` varchar(255) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

-- Table structure for table `cost`
CREATE TABLE `cost` (
  `start` varchar(255) NOT NULL,
  `stopage` varchar(255) NOT NULL,
  `category` int(3) NOT NULL,
  `cost` int(3) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

-- Table structure for table `orders`
CREATE TABLE `orders` (
  `order_id` int(3) NOT NULL,
  `bus_id` int(3) NOT NULL,
  `user_id` int(3) NOT NULL,
  `user_name` varchar(255) NOT NULL,
  `user_age` int(3) NOT NULL,
  `source` varchar(255) NOT NULL,
  `destination` varchar(255) NOT NULL,
  `date` date NOT NULL,
  `cost` int(3) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

-- Table structure for table `posts`
CREATE TABLE `posts` (
  `post_id` int(3) NOT NULL,
  `post_category_id` int(3) NOT NULL,
  `post_title` varchar(255) NOT NULL,
  `post_author` varchar(255) NOT NULL,
  `post_date` date NOT NULL,
  `post_image` text NOT NULL,
  `post_content` text NOT NULL,
  `post_source` varchar(255) NOT NULL,
  `post_destination` varchar(255) NOT NULL,
  `post_via` varchar(255) NOT NULL,
  `post_via_time` varchar(255) NOT NULL,
  `post_query_count` int(3) NOT NULL,
  `max_seats` int(3) NOT NULL,
  `available_seats` int(3) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

-- Table structure for table `query`
CREATE TABLE `query` (
  `query_id` int(3) NOT NULL,
  `query_bus_id` int(3) NOT NULL,
  `query_user` varchar(255) NOT NULL,
  `query_email` varchar(255) NOT NULL,
  `query_date` date NOT NULL,
  `query_content` text NOT NULL,
  `query_replied` varchar(255) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

-- Table structure for table `seats`
CREATE TABLE `seats` (
  `bus_id` int(3) NOT NULL,
  `max_seats` int(3) NOT NULL,
  `available_seats` int(3) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

-- Table structure for table `users`
CREATE TABLE `users` (
  `user_id` int(3) NOT NULL,
  `username` varchar(255) NOT NULL,
  `user_password` varchar(255) NOT NULL,
  `user_firstname` varchar(255) NOT NULL,
  `user_lastname` varchar(255) NOT NULL,
  `user_email` varchar(255) NOT NULL,
  `user_phoneno` varchar(255) NOT NULL,
  `user_image` text NOT NULL,
  `user_role` varchar(255) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
```

## How to Run the Project Locally

### Prerequisites
- **XAMPP** or **WAMP** server installed on your machine.
- **phpMyAdmin** for database management.

### Steps
1. **Clone the repository to your local machine:**

   ```bash
   git clone https://github.com/your-username/online-bus-booking-system.git

2. **Move the project folder to the XAMPP/WAMP server's **`htdocs`** directory.**

3. **Start the **Apache** and **MySQL** services from the XAMPP/WAMP control panel.**

4. **Open a web browser and go to** `http://localhost/phpmyadmin`.

5. **Create a new database named** `bus`.

6. **Import the provided SQL file **(`bus.sql`) **into the** `bus` **database.**

7. **Open your browser and navigate to** `http://localhost/online-bus-booking-system` **to run the project.**

## Usage
- **User Side**: Browse available buses, view routes, and book tickets.
- **Admin Side**: Manage buses, routes, and view customer bookings.

## License
This project is licensed under the **MIT License**.

