# Capstone-Shopkart
`FYND Captsone Project`

## Ecommerce Website Using React

The project requires creating a fully functional, responsive frontend using React and integrating with a backend for product and cart management.

**Project Overview**

E-commerce website using MERN. The project requires creating a fully functional, responsive frontend using React and integrating with a backend for product and cart management. 
Core features include product browsing, cart management, and order placement. The website will be evaluated based on UI design, functionality, and code structure.


### Overall Breakdown

1. Project Setup and Initial Frontend Development

  Set up the project repository on GitHub.
  Create the basic project structure using React.
  Design main pages Home, Product, and Cart, using HTML and CSS.
  Ensure responsiveness using CSS or Bootstrap.
  Implement navigation components (e.g., Home, Products, Cart).

2. Backend Setup and API Integration

Set up a backend (optional or using a third-party API like Fakestore API).
Create mock data for products using JSON or connect to an external API.
Implement product fetching from the API.
Display the fetched products on the frontend with dynamic rendering.

3. Cart Management System

Implement add-to-cart functionality.
Display selected items in the cart with quantities.
Allow users to modify cart items (update quantity, remove items).
Calculate and display total price dynamically.

4. Order Placement and User Interaction

Implement an order form where users enter details (e.g., name, address, phone number).
Handle form validation and ensure all required fields are filled.
Display a success message upon order completion.
Clear the cart after a successful order.

5. Project Testing, Debugging, and Deployment

Test the entire workflow (product listing, cart, and order placement).
Fix any issues and optimize performance.
Write documentation with setup instructions.
Deploy the app on GitHub Pages, Netlify, or a similar platform.

Key Functionalities

1. Product Management :
Browse products with a dynamic listing.
Add products to the cart and adjust quantities.
2. Cart Management :
Display cart details with total price calculations.
Remove items and proceed to checkout.
3. Order Placement :
Order form with validation.
Show success messages and clear the cart.



---

## 🛒 Project: E-commerce Website using React

**Goal:** Build a responsive, real-world e-commerce site with cart, checkout, and order flow.
**Stack:** React, Context/Redux (optional), CSS/Bootstrap, Fakestore API or mock JSON.

---

## ✅ High-Level Phases (Production Workflow)

| Phase                | Days    | Goal                                      |
| -------------------- | ------- | ----------------------------------------- |
| 1. Planning & Setup  | Day 1   | Define features, project structure, tools |
| 2. UI & Layout       | Day 2–3 | Build component-based frontend UI         |
| 3. API & State Logic | Day 4–5 | Connect APIs, handle cart & state         |
| 4. Checkout Flow     | Day 6   | Form, validation, success page            |
| 5. Testing & Polish  | Day 7   | UX fixes, test flows                      |
| 6. Deployment & Docs | Day 8   | Hosting, README, polish                   |

---

## 📅 8-Day Breakdown

### **🔹 Day 1: Planning, Setup & Boilerplate**

**Goal:** Get environment ready, define structure

* [ ] Set up GitHub repo (private or public)
* [ ] Initialize project using `create-react-app` or Vite
* [ ] Create folder structure:

  ```
  /src
    /components
    /pages
    /assets
    /services
    /context (optional)
  ```
* [ ] Install dependencies:

  * `react-router-dom`, `axios`, `bootstrap`
* [ ] Setup routes: `/`, `/products`, `/cart`, `/checkout`
* [ ] Make a Figma/mockup sketch (even hand-drawn is okay)

**Deliverable:** Skeleton app running with routing, folder structure, clean commit pushed.

---

### **🔹 Day 2: Build Homepage & Product Listing UI**

**Goal:** Build UI components with mock data

* [ ] Design homepage with banner + categories section
* [ ] Create product card component (image, title, price, button)
* [ ] Setup `/products` page showing a list of products (grid)
* [ ] Use mock data or Fakestore API initially
* [ ] Add Navbar with links to Home, Products, Cart

**Deliverable:** Navigable UI with product list, responsive layout.

---

### **🔹 Day 3: Cart Page UI + Add-to-Cart Logic**

**Goal:** Implement cart visuals and core logic

* [ ] Setup global state using Context API or local state (React basics)
* [ ] Add "Add to Cart" button to product cards
* [ ] Show item count on cart icon in Navbar
* [ ] Create Cart page: show item, quantity, total price
* [ ] Enable remove item, update quantity buttons

**Deliverable:** Fully working cart page with real-time updates

---

### **🔹 Day 4: Product Details & API Integration**

**Goal:** Connect to Fakestore API or JSON file

* [ ] Set up a service in `/services/api.js` for product fetching
* [ ] Fetch and display real product data
* [ ] Create `/products/:id` route for Product Details page
* [ ] Show product image, description, price, add to cart button

**Deliverable:** API-based product list + detail view with add-to-cart working

---

### **🔹 Day 5: Checkout Form + Order Flow**

**Goal:** Add form for user details & checkout

* [ ] Create `/checkout` page
* [ ] Build form: name, email, address, phone
* [ ] Validate fields using simple JS or libraries like `yup`
* [ ] On submit: clear cart, show confirmation message

**Deliverable:** User can successfully "place an order"

---

### **🔹 Day 6: UX Polish + Error Handling**

**Goal:** Handle edge cases, polish UI/UX

* [ ] Add loader states (optional)
* [ ] Handle empty cart, invalid product ID, form errors
* [ ] Add toast or alert for “item added” or “order placed”
* [ ] Fine-tune layout, spacing, colors

**Deliverable:** Smooth user experience with all flows tested

---

### **🔹 Day 7: Testing, Cleanup, Optimization**

**Goal:** Clean and verify all logic

* [ ] Test all user flows: product → cart → checkout
* [ ] Ensure mobile responsiveness
* [ ] Clean up unused files, optimize images
* [ ] Add helpful comments

**Deliverable:** Ready-to-deploy, clean and tested application

---

### **🔹 Day 8: Deployment & Final Touch**

**Goal:** Host app & write documentation

* [ ] Deploy to Netlify or Vercel
* [ ] Add favicon, title, meta tags
* [ ] Write a solid `README.md`:

  * Features
  * Tech stack
  * Setup steps
  * Live demo link
* [ ] Submit or present your project

**Deliverable:** Deployed link + repo ready to showcase

---

## 📦 Bonus (Optional but Impressive)

* Add search/filter (price range, category)
* Pagination or infinite scroll
* Use Redux Toolkit instead of Context API
* Admin panel (mock only, no login needed)

---

## ⏳ Time Budget (per day with job)

| Time Slot         | Suggested Use          |
| ----------------- | ---------------------- |
| 1.5 hrs morning   | UI tasks or debugging  |
| 1 hr lunch        | Small coding, testing  |
| 1.5–2 hrs evening | Main development chunk |

---
