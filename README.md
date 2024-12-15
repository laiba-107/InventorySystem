# InventoryManagementSystem

A software developed using Java SE which provides an easy way to track products, suppliers, customers, as well as purchase and sales information. It also records the stock currently available in the store. The system is connected to a **MySQL** database to store and manage inventory data.

There are basically two users: **Administrator** and **Normal User**. Both users can manage suppliers, products, customers, and purchase and sell products. The only difference between the two users is that the **administrator** can also view sales reports and manage other users.

## Features:
| Feature                        | Administrator                    | Normal User                       |
|---------------------------------|-----------------------------------|-----------------------------------|
| **Manage Suppliers**            | Add, edit, delete, view suppliers | Add, edit, delete, view suppliers |
| **Manage Products**             | Add, edit, delete, view products  | Add, edit, delete, view products  |
| **Manage Customers**            | Add, edit, delete, view customers | Add, edit, delete, view customers |
| **Manage Purchases and Sales**  | Add, edit, delete, view purchases and sales | Add, edit, delete, view purchases and sales |
| **View Sales Reports**          | View total sales, top-selling products, supplier reports | - |
| **Manage Users**                | Add, delete, and manage other users | - |

## Setup and Installation

1. **Download the .sql file for this application**:  
   [Google Drive Link](https://drive.google.com/file/d/0Bw-qNYNSGhdCN09YZDV6SmtRN00/view?usp=sharing&resourcekey=0-g98Gi5ErSgzV-Jit-4Ow6Q)

2. **Download required third-party plugins (includes JCalendar, JTattoo, and SQLConnector)**:  
   [Google Drive Link](https://drive.google.com/file/d/0Bw-qNYNSGhdCMU1mekN4SmRCb1E/view?usp=sharing&resourcekey=0-mynFCWwHM0l7oUuBwDIVbw)

3. **Download the software only**:  
   [Google Drive Link](https://drive.google.com/file/d/0Bw-qNYNSGhdCbVdSdzZHX0pZOFE/view?usp=sharing&resourcekey=0-mynFCWwHM0l7oUuBwDIVbw)

## Requirements:
- Java SE (Java Development Kit)
- MySQL Database (for storing and managing data)
- Required third-party plugins as mentioned above

## MySQL Database Setup:
The application uses a **MySQL** database to store and manage data. To set up the MySQL database:

1. **Create a database** in MySQL:
   - Run the `.sql` file provided to set up the required tables and relationships.

2. **Configure the connection**:
   - Update the database connection details in the configuration file (e.g., `application.properties` or `application.yml`) to match your MySQL setup.
   - Example configuration:
     ```properties
     spring.datasource.url=jdbc:mysql://localhost:3306/inventory_db
     spring.datasource.username=root
     spring.datasource.password=password
     spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
     spring.jpa.hibernate.ddl-auto=update
     spring.jpa.database-platform=org.hibernate.dialect.MySQL8Dialect
     ```

## Usage
1. Set up the database using the `.sql` file.
2. Install the required third-party plugins.
3. Run the Java application, and use it to manage your inventory, suppliers, customers, and sales.

## Expected Output

| Action                               | Expected Output |
|--------------------------------------|-----------------|
| **Login (Administrator)**            | Successful login, admin dashboard with full features (Manage Suppliers, Products, Sales, etc.) |
| **Login (Normal User)**              | Successful login, user dashboard with limited features (Manage Suppliers, Products, Sales) |
| **Add Product**                      | "Product 'Laptop' added successfully." |
| **View Product List**                | Displays a list of all products: name, price, quantity, etc. |
| **Edit Product**                     | "Product updated successfully." |
| **Delete Product**                   | "Product 'Laptop' deleted successfully." |
| **Make Purchase**                    | "Purchase of 'Laptop' completed. Stock updated." |
| **Make Sale**                        | "Sale completed: 2 x Laptops for $2000." |
| **Generate Sales Report (Admin)**    | Displays total sales, top-selling products, supplier performance, etc. |
| **Invalid Login**                    | "Invalid username or password." |
| **Out of Stock Error**               | "Product 'Laptop' is out of stock." |
| **Missing Field Error**              | "All fields are required." |
| **Database Connection Error**        | "Database connection error. Please try again later." |

## License
[Add license information here if applicable]
