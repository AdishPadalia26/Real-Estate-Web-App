# DreamDwellings — Real Estate Web Application

![MIT License](https://img.shields.io/badge/license-MIT-green)
![React](https://img.shields.io/badge/frontend-React-blue)
![Node.js](https://img.shields.io/badge/backend-Node.js-green)

---

DreamDwellings is a full-stack real estate web application designed for buyers and sellers to explore property listings, contact agents, and manage listings with ease. Built with modern web technologies, it offers responsive user interfaces and a scalable backend API.

---

## Table of Contents
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Code Examples](#code-examples)
- [Getting Started](#getting-started)
- [API Endpoints](#api-endpoints)
- [Roadmap](#roadmap--potential-enhancements)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

---

## Key Features
- Browse Properties: Advanced filtering by location, price, type, features
- Property Details: Rich pages with images, descriptions, amenities
- User Accounts: Register, log in, manage profiles (Redux + Firebase)
- Contact Agents: Send inquiries from property pages
- Admin Panel: Manage listings, users (optional)
- Responsive UI: Optimized for desktop & mobile (Tailwind + Vite)
- Image uploads: Firebase Storage for property images
- Secure Auth: JWT & Firebase integration

---

## Tech Stack

| Layer         | Technologies                                  |
|---------------|-----------------------------------------------|
| Frontend      | React.js, Vite, Tailwind CSS, Redux Toolkit   |
| Backend       | Node.js, Express.js                           |
| Database      | MongoDB (Mongoose) or PostgreSQL (optional)   |
| APIs          | RESTful endpoints                             |
| Auth/Storage  | Firebase (Auth, Storage)                      |
| Deployment    | Vercel / Netlify (frontend), Heroku / Render  |

---

## Code Examples

**React: PropertyCard Component**
```jsx
// src/components/PropertyCard.js
import React from 'react';
const PropertyCard = ({ property }) => (
  <div className="card">
    <img src={property.image} alt={property.title} />
    <h3>{property.title}</h3>
    <p>{property.location} • ${property.price}</p>
  </div>
);
export default PropertyCard;
```

**Express: Listings Route**
```js
// api/routes/listings.js
const express = require('express');
const router = express.Router();
const { getListings } = require('../controllers/listings');
router.get('/', getListings);
module.exports = router;
```

---

## Getting Started

### Prerequisites
- Node.js (v16+)
- npm or Yarn
- MongoDB Atlas / Local MongoDB

### 1. Clone the repository

```bash
git clone https://github.com/AdishPadalia26/Real-Estate-Web-App.git
cd Real-Estate-Web-App
```

### 2. Setup the Backend
```bash
cd api
cp .env.example .env
# Edit .env with PORT, MONGO_URI, etc.
npm install
npm run dev
```

### 3. Setup the Frontend (Vite + React)
```bash
cd ../client
npm install
npm start
```

---

## API Endpoints

```
GET    /api/listings
GET    /api/listings/:id
POST   /api/inquiries
POST   /api/listings          # For admin
PUT    /api/listings/:id      # For admin updates
DELETE /api/listings/:id      # For admin deletion
```

---

## Roadmap & Potential Enhancements

- User Authentication (JWT/Firebase)
- Role-based Access (Admin vs User)
- Image uploads for property listings
- Email notifications for inquiries
- Map integration (Google Maps)
- Pagination & price sliders
- Deployment automation (CI/CD)

---

## Contributing

1. Fork the repo
2. Create a feature branch: `git checkout -b feat/add-filter-component`
3. Commit your changes: `git commit -m "Add price filter component"`
4. Push and open a PR

---

## License

Released under the MIT License.

---

## Author

👤 **Adish Padalia**  
🌐 [LinkedIn](https://www.linkedin.com/in/adish-padalia/)  
💻 [GitHub](https://github.com/AdishPadalia26)  
📧 padaliaadish@gmail.com

---
