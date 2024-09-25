# Simple Inventory Management System

## Overview
This is a Simple Inventory Management System built using Django and Django Rest Framework (DRF). The application allows users to manage inventory items, including creating, reading, updating, and deleting items. It also includes user authentication and JWT token management for secure access.

## Features
- User registration and authentication (using JWT)
- CRUD operations for inventory items
- Soft delete functionality for items
- Caching of item data using Redis for improved performance
- Swagger documentation for easy API exploration

## Technologies Used
- **Django**: A high-level Python web framework.
- **Django Rest Framework (DRF)**: A powerful toolkit for building Web APIs.
- **PostgreSQL**: An open-source relational database.
- **Redis**: An in-memory data structure store used for caching.
- **Swagger**: API documentation and testing tool.

## Installation

### Prerequisites
- Python 3.x
- Docker (for Docker-based setup)
- PostgreSQL
- Redis

## Running the Application Locally

### Method 1: Using Docker

#### Steps
1. Clone the repository:
    ```bash
    git clone <repository-url>
    cd inventory_system
    ```
2. Build and Run the Docker Containers: Ensure Docker is installed and running on your system.
    ```bash
    docker-compose up --build
    ```
3. Access the Application:
    - API: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
    - Swagger documentation: [http://127.0.0.1:8000/swagger/](http://127.0.0.1:8000/swagger/)

### Method 2: Manual Setup

#### Steps
1. Clone the repository:
    ```bash
    git clone <repository-url>
    cd inventory_system
    ```
2. Create and activate a virtual environment:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```
3. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
4. Configure PostgreSQL:
    - Create a new PostgreSQL database.
    - Update the `DATABASES` setting in `settings.py` with your database credentials.
    
5. Configure Redis:
    - Install Redis on your machine and ensure the Redis server is running.

6. Run migrations:
    ```bash
    python manage.py migrate
    ```

7. Create a superuser (optional):
    ```bash
    python manage.py createsuperuser
    ```

8. Run the development server:
    ```bash
    python manage.py runserver
    ```

9. Access the Application:
    - API: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
    - Swagger documentation: [http://127.0.0.1:8000/swagger/](http://127.0.0.1:8000/swagger/)

## API Endpoints
- **User Registration**: `POST /register/`
- **User Login**: `POST /login/`
- **Create Item**: `POST /items/`
- **Get Item Details**: `GET /items/<item_id>/`
- **Update Item**: `PUT /items/<item_id>/`
- **Delete Item**: `DELETE /items/<item_id>/`

## Running Tests
To run tests, use the following command:
```bash
python manage.py test

