# Library ERP – Library Management System
LIve LINK -https://erplibarysystem.netlify.app/
## Overview
This project is a **Library Management System (LMS)** web application developed to simulate basic library operations such as searching books, issuing books, returning books, and managing memberships. The system supports role-based access so that different users have different permissions within the application.

The goal of the project is to implement a simple and functional system that follows the assignment requirements while demonstrating basic software design and validation logic.

---

## Tech Stack

- **Frontend:** React
- **Build Tool:** Vite
- **Language:** JavaScript
- **Routing:** React Router
- **Styling:** CSS
- **Package Manager:** npm

---

## Modules

### Authentication
The system provides a login page where users can log in using their credentials.

Two roles are supported:

**Admin**
- Access to Maintenance
- Access to Transactions
- Access to Reports

**User**
- Access to Transactions
- Access to Reports
- No access to Maintenance

---

### Maintenance Module (Admin Only)

This module allows administrators to manage library data.

Features include:

- Add new books
- Update book information
- Add memberships
- Update memberships
- Manage users

---

### Transactions Module

This module manages day-to-day library operations.

Features:

- Search available books
- Issue books
- Return books
- Handle fine payments

Important rules implemented in the system:

- A book must be selected before issuing.
- Issue date cannot be earlier than the current date.
- Return date is automatically generated.
- Fine must be confirmed before completing a return transaction.

---

### Reports Module

This module provides basic information about library activity.

Examples include:

- Available books
- Issued books
- Membership information

---

## Validation Rules

The system performs basic form validations:

- Required fields must not be empty
- At least one search field must be provided
- Issue date must not be earlier than the current date
- Book selection is mandatory before issuing
- Error messages appear on the same page when validation fails

---

## Development Approach

The project was developed using a simple modular approach.

1. Analyze the assignment requirements and identify key modules.
2. Divide the system into Maintenance, Transactions, and Reports sections.
3. Create separate components/pages for each feature.
4. Implement routing to navigate between pages.
5. Add validation rules to ensure correct user input.

The main focus was to build a **minimum working application** that demonstrates the required library workflow.

---

## Assumptions

1. Each book has a **unique serial number** used for identification.
2. A book can only be issued if it is marked as **available**.
3. A user must select a book from the search results before issuing it.
4. Membership information is assumed to exist for users who issue books.
5. The fine is calculated based on **late return days**.
6. Only administrators can modify library data such as books or memberships.
7. The system assumes the library database size is **small or medium scale**.
8. Authentication is simplified and does not include advanced security features.
9. The application is designed for **demonstration purposes** rather than production use.
10. Users follow the correct issue and return workflow through the application.

---

## Running the Project

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Build the project:

```bash
npm run build
```

---

## Future Improvements

- Add advanced book search filters
- Implement online fine payment
- Add email reminders for due dates
- Improve UI and accessibility
- Integrate a backend database
