# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh



---
# 🎯  Restaurant Management Website 🍽️

## 📌 Project Overview
A full-stack **Restaurant Management Website** built with the **MERN Stack** (MongoDB, Express.js, React.js, Node.js).  
The platform is designed to enhance the restaurant’s online presence, improve customer interaction, and streamline internal management processes.

---
# 🚀 Live Website showcase
# 🌐 live link:https://resturentmanagement-website.web.app/

### 🔗 Clint site : https://github.com/mdtahsinislam/Resturent-management-clint-site
### 🔗 Server site: https://github.com/mdtahsinislam/Resturent_management-server-site

## ✨ Features

- **Authentication System**
  - Email/Password login & register
  - Google/GitHub OAuth (choose one)
  - Conditional Navbar (Login/Logout/Profile image)
  - Password validation (Uppercase, Lowercase, Min length 6)
  - Toast/SweetAlert for login/register success/errors

- **Navbar**
  - Logo / Website Name
  - Home, All Foods, Gallery
  - Login/Logout (conditional)
  - Profile image + dropdown (My Foods, Add Food, My Orders)

- **Home Page (Public)**
  - Banner/Slider with title, description, and button (redirect to All Foods)
  - Top Foods section (6 top-selling foods by purchase count)
  - Extra Sections (2 creative, food/restaurant related)
  - “See All” button → All Foods page

- **All Foods Page (Public)**
  - Title with background banner
  - Show all food items (cards/grid)
  - Search functionality
  - Each card shows food info, quantity, and Details button

- **Single Food Page (Public)**
  - Detailed food information
  - Purchase count (default 0)
  - Purchase button → redirects to Food Purchase page

- **Food Purchase Page (Private)**
  - Form with:
    - Food name
    - Price
    - Quantity
    - Buyer name & email (auto-filled from user)
    - Buying date (auto-added with Date.now())
  - On purchase: data stored in DB + success toast/alert

- **Gallery Page (Public)**
  - Page title
  - Gallery with at least 10 static images
  - Click image → enlarged (lightbox effect with `yet-another-react-lightbox` or similar)

- **My Foods Page (Private)**
  - Shows all foods added by the logged-in user
  - Display in table or cards
  - Update button (edit food info via form/modal)
  - Restriction: Only owner can update their own foods

- **Add Food Page (Private)**
  - Form with:
    - Food name
    - Food image
    - Category
    - Quantity
    - Price
    - Added by (user name & email)
    - Origin (country)
    - Short description
  - On success → save to DB + toast/alert

- **My Orders Page (Private)**
  - Shows foods ordered by logged-in user
  - Info includes:
    - Food image, name, price, owner
    - Purchase date (formatted with `moment`)
    - Delete button to remove an order

- **Footer**
  - Restaurant info
  - Contact details
  - Eye-catching design

---

## ✨ Technology Stack

* Frontend: React.js / Tailwind CSS / daisyui
* Backend: Node.js + Express.js
* Database: MongoDB
* Authentication: Firebase Authentication / JWT
* Hosting: Frontend (Client site): Firebase Hosting | Backend (Server site): Vercel Hosting
* Toaster/Alerts: react-toastify or SweetAlert2
* Slider: Swiper.js or DaisyUI Carousel
* Version Control: GitHub
---

## 🔐 Authentication Flow

- Login with Email/Password or Google/GitHub
- Register with Name, Email, PhotoURL, Password
- Validation:
  - Password must have **uppercase, lowercase, min 6 chars**
- Navbar changes based on login state
- Profile dropdown → My Foods, Add Food, My Orders

---

## 🧾 Data Model Example

```json
{
  "_id": "123abc",
  "foodName": "Grilled Chicken",
  "image": "https://.../food.jpg",
  "category": "Main Course",
  "quantity": 10,
  "price": 12.99,
  "addedBy": {
    "name": "John Doe",
    "email": "john@example.com"
  },
  "origin": "USA",
  "description": "Delicious grilled chicken with spices",
  "purchaseCount": 5,
  "createdAt": "2025-10-01T10:30:00Z"
}
```

---
## 🗺 Pages & Routes

**Public**

* `/` → Home
* `/all-foods` → All Foods
* `/gallery` → Gallery
* `/foods/:id` → Single Food Details
* `/login` → Login
* `/register` → Register
* `/*` → 404 Page

**Private**

* `/purchase/:id` → Food Purchase
* `/my-foods` → My Foods
* `/add-food` → Add Food
* `/my-orders` → My Orders

---

## ⚙️ Installation & Setup
```
# install dependencies
npm install

# run client
npm run dev

# run server
cd server
npm install
npm start
```
## 🛠️ Deployment
* Hosting: Frontend (Client site): Firebase Hosting | Backend (Server site): Vercel Hosting
* Database: MongoDB Atlas
---
## 📝  Happy coding 🚀


