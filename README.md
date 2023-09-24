# Spring Boot Elasticsearch CRUD Application

This is a sample Spring Boot application that demonstrates performing CRUD (Create, Read, Update, Delete) operations on Elasticsearch. It serves as a basic example to help you get started with integrating Elasticsearch into your Spring Boot project.

## Features

- **Create**: Add new documents to Elasticsearch.
- **Read**: Retrieve documents from Elasticsearch.
- **Update**: Modify existing documents in Elasticsearch.
- **Delete**: Remove documents from Elasticsearch.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Java Development Kit (JDK) installed.
- Apache Maven installed.
- Elasticsearch instance running (you can use the [official Elasticsearch Docker image](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html)).
- Spring Boot development environment set up.

## Usage

To get started with this Spring Boot Elasticsearch CRUD application, follow these steps:

1. **Navigate to the project directory:**

    ```bash cd spring-boot-elasticsearch-crud```

2. **Build the project using Maven:**

    ```bash mvn clean install```

3. **Run the Spring Boot application:**

    ```bash java -jar target/spring-boot-elasticsearch-crud-1.0.0.jar```

4. **Usage:**

   Once the application is up and running, you can use the following endpoints to interact with Elasticsearch:

   - **Create a Product (POST)**
     - **Endpoint**: `/createProduct`
     - **Request Body** (JSON):
       ```json
       {
           "id": "BOOK-1",
           "name": "ElasticSearchBook",
           "description": "wonderful book",
           "price": 100.99
       }
       ```
     - Creates a new product document in Elasticsearch.

   - **Retrieve Products (GET)**
     - **Endpoint**: `/getProducts`
     - Retrieves a list of all products from Elasticsearch.

   - **Update a Product (PUT)**
     - **Endpoint**: `/updateProduct/{productId}`
     - **Request Body** (JSON):
       ```json
       {
           "name": "UpdatedBook",
           "description": "Updated description",
           "price": 150.99
       }
       ```
     - Updates an existing product document in Elasticsearch.

   - **Delete a Product (DELETE)**
     - **Endpoint**: `/deleteProduct/{productId}`
     - Deletes a product document from Elasticsearch by its ID.


