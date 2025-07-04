# Airbnb Clone Project

## Overview

The **Airbnb Clone Project** is a full-stack web application that replicates the core functionalities of the Airbnb platform. It allows users to register, list properties, make bookings, leave reviews, and handle payments. The project is built to simulate a real-world team development environment using modern web technologies and DevOps practices.

### Project Goals

- Build a scalable, maintainable clone of the Airbnb platform.
- Understand how to develop and consume RESTful APIs.
- Practice collaboration, CI/CD, and version control in a team setting.
- Apply backend and frontend technologies effectively.

---

## Team Roles

| Role | Description |
|------|-------------|
| **Backend Developer** | Builds and maintains the server-side logic, APIs, and business logic using Django and GraphQL. |
| **Frontend Developer** | Implements the UI components, connects to APIs, and ensures responsive design using React. |
| **Database Administrator (DBA)** | Designs and manages the PostgreSQL database schema, optimizes queries, and ensures data integrity. |
| **DevOps Engineer** | Sets up CI/CD pipelines, manages deployments, monitors application health, and handles Docker containers. |
| **QA Tester** | Writes and executes test cases, performs manual and automated testing, and ensures product quality. |
| **Product Manager** | Oversees project goals, deadlines, scope, and coordination between team members. |

---

## Technology Stack

| Technology | Purpose |
|------------|---------|
| **Django** | Backend framework used to build RESTful APIs and handle business logic. |
| **PostgreSQL** | Relational database system used to store and manage application data. |
| **GraphQL** | API query language used for efficient data fetching and manipulation. |
| **React** | Frontend JavaScript library for building dynamic user interfaces. |
| **Docker** | Containerization platform used for consistent development and deployment environments. |
| **GitHub Actions** | CI/CD tool used for automated testing, building, and deployment of the app. |

---

## Database Design

### Entities and Key Fields

- **Users**
  - `id`, `name`, `email`, `password`, `role`
  - A user can be a host or a guest.

- **Properties**
  - `id`, `title`, `location`, `price`, `host_id`
  - A property is listed by a user (host).

- **Bookings**
  - `id`, `user_id`, `property_id`, `start_date`, `end_date`
  - A booking is made by a guest for a specific property.

- **Reviews**
  - `id`, `booking_id`, `rating`, `comment`, `date`
  - Each review is linked to a booking and provides feedback.

- **Payments**
  - `id`, `booking_id`, `amount`, `payment_method`, `status`
  - Payments are tied to bookings and processed securely.

### Relationships

- A **user** can have multiple **properties**.
- A **booking** belongs to one **property** and one **user**.
- A **review** is given per **booking**.
- A **payment** is associated with one **booking**.

---

## Feature Breakdown

- **User Management**
  - Users can register, log in, and manage profiles. Role-based access controls are implemented.

- **Property Management**
  - Hosts can add, update, or remove property listings. Listings include photos, descriptions, and location data.

- **Booking System**
  - Guests can search for listings, check availability, and make bookings using a calendar interface.

- **Reviews & Ratings**
  - Users can leave reviews for properties they’ve stayed at, helping maintain transparency.

- **Payment Processing**
  - Integration with a payment gateway (e.g., Stripe) for secure transactions.

- **Admin Dashboard**
  - Admins can manage users, view site statistics, and handle reports or complaints.

---

## API Security

### Key Measures

- **Authentication**: JWT-based login system to ensure only verified users access protected routes.
- **Authorization**: Role-based permissions to differentiate between guests, hosts, and admins.
- **Rate Limiting**: Protects APIs from abuse and brute-force attacks by limiting the number of requests.
- **Data Validation**: Ensures data integrity and prevents malicious input.
- **HTTPS**: All data in transit is encrypted.

### Why Security is Crucial

- **User Data Protection**: Prevents data breaches and identity theft.
- **Payment Security**: Ensures financial transactions are safe and compliant.
- **System Integrity**: Protects against unauthorized access and system manipulation.

---

## CI/CD Pipeline

**CI/CD (Continuous Integration/Continuous Deployment)** is used to automate the testing and deployment process, ensuring faster and more reliable delivery.

### Tools Used:

- **GitHub Actions**: Automates testing and deployment workflows.
- **Docker**: Containers for consistent development and production environments.
- **Heroku / AWS / Vercel**: (or similar) for hosting and deployment.
- **Pre-commit Hooks**: For code linting and formatting before pushing.

### Why It Matters:

- Automates testing and deployment steps.
- Reduces the chance of human error.
- Ensures each commit maintains the stability of the application.
- Encourages rapid iteration and collaboration.

---

## License

This project is for educational purposes only.

---
