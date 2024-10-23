# Product Management System (React, Spring Boot & MySQL)

This project is a **Product Management System** that allows users to **add**, **view**, **edit**, and **delete** product details. It uses **ReactJS** for the front-end, **Spring Boot** for the back-end, and **MySQL** as the database.

## Features

1. **Add Product**: Users can add new products by providing product details like product ID, name, image URL, cost price, quantity, and origin.
2. **View Products**: Users can view a list of all products, including their profit, sell price, GST, and amount.
3. **Edit Product**: Users can edit existing product details.
4. **Delete Product**: Users can delete products from the list.
5. **Integration**: The front-end and back-end are connected using REST APIs. The back-end uses MySQL to store product data.

## Technologies Used

- **Frontend**: ReactJS, Axios
- **Backend**: Spring Boot (Java)
- **Database**: MySQL
- **Routing**: React Router

## Setup and Installation

### Backend (Spring Boot)

1. Clone the repository:
   ```bash
   git clone https://github.com/chandrika-2112/Product-Management.git
   ```

2. Configure the `application.properties` file in your **Spring Boot** project to connect to your **MySQL** database.

   Example:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/product_db
   spring.datasource.username=root
   spring.datasource.password=password
   spring.jpa.hibernate.ddl-auto=update
   spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
   spring.jpa.show-sql=true
   ```

3. Create the necessary database tables. The application will create the `product` table on startup if `spring.jpa.hibernate.ddl-auto=update` is set in the properties file.

4. Run the Spring Boot application:
   ```bash
   mvn spring-boot:run
   ```

### Frontend (ReactJS)

1. Navigate to the `Product-Management-Using-ReactJs` directory.

2. Install the dependencies:
   ```bash
   npm install
   ```

3. Start the React app:
   ```bash
   npm start
   ```

4. The application will be available at `http://localhost:3000`.

## Project Structure

### Frontend (ReactJS)

The main files for the React app are located in the `/components` folder:

1. **`AddProduct.jsx`**: Form to add a new product.
2. **`EditProduct.jsx`**: Form to edit an existing product.
3. **`ViewProduct.jsx`**: Page to view the list of all products.
4. **`Home.jsx`**: Home page of the product management system.
5. **`Master.jsx`**: Defines the routing for the React app.

### Backend (Spring Boot)

1. **`ProductController.java`**: Handles the REST API endpoints.
2. **`ProductServices.java`**: Implements the business logic for managing products.
3. **`ProductRepository.java`**: Manages the interaction with the database.
4. **`Product.java`**: Entity class representing the `Product` model.

#### API Endpoints

1. **GET `/allProducts`**: Retrieve a list of all products.
2. **POST `/save`**: Add a new product.
3. **PUT `/update/{pid}`**: Update an existing product.
4. **DELETE `/delete/{pid}`**: Delete a product by its ID.

### Database (MySQL)

The application connects to a **MySQL** database to store product data. Ensure that the database is running and the `product_db` is created.

### Example Product Schema

```sql
CREATE TABLE product (
    pid INT PRIMARY KEY,
    name VARCHAR(255),
    image VARCHAR(255),
    costPrice INT,
    quantity INT,
    origin VARCHAR(255),
    profit FLOAT,
    sellPrice INT,
    gst FLOAT,
    amount INT
);
```

## Running the Application

1. Ensure **MySQL**, **Spring Boot**, and **ReactJS** are set up and running.
2. Navigate to `http://localhost:3000` to interact with the product management system.

## Additional Information

- **Repository**: Refer to the [Product-Management](https://github.com/chandrika-2112/Product-Management) repository for the Back End(SpringBoot, Mysql, Java, Postman APi) implementation of this project.

