# Airbnb Clone Project

## Project Overview
This project is a full-stack Airbnb clone designed to simulate the development of a robust booking platform. It covers backend architecture, database design, API security, CI/CD, and team collaboration.

## Tech Stack
- Django
- MySQL / PostgreSQL
- GraphQL
- Docker
- GitHub Actions

## Team Roles

- **Backend Developer:** Implements core APIs, business logic, and integrates database.
- **Database Administrator (DBA):** Designs database schema, optimizes queries, ensures data consistency and backups.
- **DevOps Engineer:** Manages CI/CD pipeline, server infrastructure, Docker containers.
- **Project Manager:** Coordinates tasks, sets milestones, ensures timely delivery.
- **QA Engineer:** Tests functionality, handles bugs, validates feature requirements.

## Technology Stack

- **Django:** High-level Python web framework used to build robust REST and GraphQL APIs.
- **PostgreSQL/MySQL:** Relational databases to manage structured data like users, bookings, payments.
- **GraphQL:** Flexible query language for APIs to fetch precisely needed data.
- **Docker:** Containerization for consistent development and deployment environments.
- **GitHub Actions:** CI/CD pipeline tool used to automate testing and deployment processes.

## Database Design

**Entities:**
- **User:** `id`, `name`, `email`, `role`, `password`
- **Property:** `id`, `title`, `description`, `price`, `owner_id`
- **Booking:** `id`, `user_id`, `property_id`, `start_date`, `end_date`, `status`
- **Review:** `id`, `user_id`, `property_id`, `rating`, `comment`
- **Payment:** `id`, `booking_id`, `amount`, `method`, `timestamp`

**Relationships:**
- A **User** can own multiple **Properties**
- A **User** can make multiple **Bookings**
- Each **Booking** is tied to one **Property** and one **Payment**
- A **Review** links a User to a Property

## Feature Breakdown

- **User Management:** Handles registration, login, password encryption, and user roles (guest, host, admin).
- **Property Management:** Hosts can list, update, and delete properties they own.
- **Booking System:** Users can search for properties, book them for specific dates, and receive confirmation.
- **Review System:** After a stay, users can rate and review properties.
- **Payment Integration:** Secure payment processing for bookings via external payment services.
- **Admin Dashboard:** Admin can manage users, properties, and reviews (optional).

## API Security

**Key Security Measures:**
- **Authentication:** JWT-based user login system.
- **Authorization:** Role-based access control (e.g., only hosts can edit properties).
- **Rate Limiting:** Protects against brute-force and DoS attacks.
- **Input Validation:** Prevents SQL injection and data corruption.
- **HTTPS:** Ensures encrypted communication.

**Why It's Crucial:**
- Secures sensitive user data and credentials.
- Prevents abuse of booking and payment APIs.
- Ensures only authorized actions are allowed for users/roles.

## CI/CD Pipeline

**Overview:**
Continuous Integration and Continuous Deployment (CI/CD) automates testing and deployment, ensuring stability and faster releases.

**Tools:**
- **GitHub Actions:** Runs tests, builds, and deploys the app on every commit.
- **Docker:** Ensures consistent app behavior across environments (dev/stage/prod).
- **Optional Tools:** Travis CI, Jenkins, Heroku, or AWS/GCP for hosting.
