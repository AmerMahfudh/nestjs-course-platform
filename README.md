# NestJS E-Learning Platform
![NestJS](https://img.shields.io/badge/NestJS-20232A?style=for-the-badge&logo=nestjs)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript)


A full-featured **NestJS** e-learning platform supporting courses, students, orders, payments via PayPal, email notifications, Cloudinary uploads, and multilingual support (English & Arabic).

---

## Features

- **Course Management**
  - Add, update, and delete courses
  - Add lectures to courses
  - Filter courses by category, level, and language
- **Student Management**
  - Track purchased courses
  - Monitor course progress per lecture
  - Reset course progress
- **Order & Payment**
  - Create and capture orders via PayPal
  - Track order status and payments
- **Email Notifications**
  - Verify user email
  - Password reset emails
- **File Uploads**
  - Upload files/images via Cloudinary
- **Multi-language Support**
  - English & Arabic support across the application

---

## Tech Stack

- **Backend:** [NestJS](https://nestjs.com/)
- **Database:** MongoDB (via Mongoose)
- **Authentication:** JWT + Role-based Guards
- **Payments:** PayPal SDK
- **Email:** Nodemailer + EJS templates
- **File Uploads:** Cloudinary
- **Others:** TypeScript, RxJS, Auto-Increment IDs

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>


```
# 2. Install dependencies
npm install

# 3. Create a .env file based on .env.example
# Example .env configuration:
PORT=3000
DataBase_URL=<your_mongodb_connection_string>
JWT_SECRET=<your_jwt_secret>
PAYPAL_CLIENT_ID=<your_paypal_client_id>
PAYPAL_CLIENT_SECRET=<your_paypal_client_secret>
PAYPAL_BASE_API=<sandbox_or_live_paypal_url>
CLOUDINARY_NAME=<your_cloud_name>
CLOUDINARY_API_KEY=<your_cloudinary_api_key>
CLOUDINARY_API_SECRET=<your_cloudinary_api_secret>
MAIL_USER=<your_email>
MAIL_PASS=<your_email_app_password>
DOMAIN=<your_frontend_domain>

# 4. Run the application
npm run start:dev




## API Documentation

Swagger API is available at:  
[http://localhost:3000/api](http://localhost:3000/api)

### Endpoints

- **GET /api/course** - List all courses
- **POST /student-course/check-purchase/:courseId** - Check if student purchased a course
- **POST /order/create-order** - Create PayPal order
- **POST /upload/upload** - Upload files to Cloudinary

Folder Structure
src/
├─ user/             # User management
├─ course/           # Course & lecture management
├─ student-course/   # Student courses & progress
├─ course-progress/  # Lecture and course progress tracking
├─ order/            # Orders & PayPal integration
├─ Paypal/           # PayPal service
├─ mail/             # Email notifications
├─ cloudinary/       # Cloudinary uploads
├─ db/               # Database connection
└─ main.ts           # Entry point


## License

This project is licensed under the MIT License.

## Author

Amer Mahfudh – amer3.mahfudh@gmail.com
