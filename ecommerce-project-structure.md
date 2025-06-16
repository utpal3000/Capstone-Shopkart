# MERN E-commerce Project Structure Setup

## 1. Create Root Directory Structure

```bash
mkdir mern-ecommerce-capstone
cd mern-ecommerce-capstone
mkdir frontend backend
```

## 2. Frontend Setup (React + Vite + Tailwind)

### Navigate to frontend directory:
```bash
cd frontend
```

### Initialize React with Vite:
```bash
npm create vite@latest . -- --template react
npm install
```

### Install additional dependencies:
```bash
npm install react-router-dom axios lucide-react
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

### Configure Tailwind CSS:

**tailwind.config.js:**
```javascript
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {
      colors: {
        primary: {
          50: '#eff6ff',
          500: '#3b82f6',
          600: '#2563eb',
          700: '#1d4ed8',
        }
      }
    },
  },
  plugins: [],
}
```

**src/index.css:**
```css
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer base {
  body {
    font-family: 'Inter', system-ui, sans-serif;
  }
}

@layer components {
  .btn-primary {
    @apply bg-primary-600 hover:bg-primary-700 text-white font-medium py-2 px-4 rounded-lg transition-colors duration-200;
  }
  
  .btn-secondary {
    @apply bg-gray-200 hover:bg-gray-300 text-gray-800 font-medium py-2 px-4 rounded-lg transition-colors duration-200;
  }
  
  .input-field {
    @apply w-full px-3 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-primary-500 focus:border-transparent;
  }
}
```

### Create Frontend Folder Structure:
```
frontend/
├── public/
├── src/
│   ├── components/
│   │   ├── common/
│   │   │   ├── Header.jsx
│   │   │   ├── Footer.jsx
│   │   │   ├── LoadingSpinner.jsx
│   │   │   └── ErrorBoundary.jsx
│   │   ├── product/
│   │   │   ├── ProductCard.jsx
│   │   │   ├── ProductGrid.jsx
│   │   │   └── ProductFilter.jsx
│   │   ├── cart/
│   │   │   ├── CartItem.jsx
│   │   │   └── CartSummary.jsx
│   │   └── auth/
│   │       ├── LoginForm.jsx
│   │       └── RegisterForm.jsx
│   ├── pages/
│   │   ├── Home.jsx
│   │   ├── Products.jsx
│   │   ├── ProductDetail.jsx
│   │   ├── Cart.jsx
│   │   ├── Checkout.jsx
│   │   ├── Login.jsx
│   │   ├── Register.jsx
│   │   └── NotFound.jsx
│   ├── context/
│   │   ├── AuthContext.jsx
│   │   ├── CartContext.jsx
│   │   └── ProductContext.jsx
│   ├── hooks/
│   │   ├── useAuth.js
│   │   ├── useCart.js
│   │   └── useApi.js
│   ├── services/
│   │   ├── api.js
│   │   ├── authService.js
│   │   └── productService.js
│   ├── utils/
│   │   ├── constants.js
│   │   ├── helpers.js
│   │   └── validators.js
│   ├── assets/
│   │   └── images/
│   ├── App.jsx
│   ├── main.jsx
│   └── index.css
├── package.json
├── vite.config.js
└── tailwind.config.js
```

## 3. Backend Setup (Node.js + Express + MongoDB)

### Navigate to backend directory:
```bash
cd ../backend
```

### Initialize Node.js project:
```bash
npm init -y
```

### Install dependencies:
```bash
npm install express mongoose dotenv cors bcryptjs jsonwebtoken
npm install -D nodemon concurrently
```

### Create Backend Folder Structure:
```
backend/
├── config/
│   └── database.js
├── controllers/
│   ├── authController.js
│   ├── productController.js
│   └── orderController.js
├── middleware/
│   ├── auth.js
│   ├── errorHandler.js
│   └── validation.js
├── models/
│   ├── User.js
│   ├── Product.js
│   └── Order.js
├── routes/
│   ├── auth.js
│   ├── products.js
│   └── orders.js
├── utils/
│   ├── generateToken.js
│   └── seedData.js
├── .env
├── .gitignore
├── package.json
└── server.js
```

### Update package.json scripts:
```json
{
  "scripts": {
    "start": "node server.js",
    "dev": "nodemon server.js",
    "seed": "node utils/seedData.js"
  }
}
```

### Create .env file:
```env
NODE_ENV=development
PORT=5000
MONGO_URI=mongodb://localhost:27017/ecommerce
JWT_SECRET=your_jwt_secret_key_here
JWT_EXPIRE=30d
```

### Create .gitignore:
```gitignore
node_modules/
.env
.env.local
.env.development.local
.env.test.local
.env.production.local
npm-debug.log*
yarn-debug.log*
yarn-error.log*
.DS_Store
*.log
dist/
build/
```

## 4. Root Level Configuration

### Create root package.json for concurrent development:
```json
{
  "name": "mern-ecommerce-capstone",
  "version": "1.0.0",
  "scripts": {
    "dev": "concurrently \"npm run server\" \"npm run client\"",
    "server": "cd backend && npm run dev",
    "client": "cd frontend && npm run dev",
    "build": "cd frontend && npm run build",
    "install-server": "cd backend && npm install",
    "install-client": "cd frontend && npm install",
    "install-all": "npm run install-server && npm run install-client"
  },
  "devDependencies": {
    "concurrently": "^8.2.0"
  }
}
```

## 5. Initial Setup Commands

### From the root directory, run:
```bash
# Install all dependencies
npm install
npm run install-all

# Start both frontend and backend
npm run dev
```

## 6. VSCode Configuration (Optional)

### Create .vscode/settings.json:
```json
{
  "emmet.includeLanguages": {
    "javascript": "javascriptreact"
  },
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode"
}
```

### Create .vscode/extensions.json:
```json
{
  "recommendations": [
    "esbenp.prettier-vscode",
    "ms-vscode.vscode-json",
    "bradlc.vscode-tailwindcss",
    "ms-vscode.vscode-typescript-next"
  ]
}
```

## 7. Git Setup

```bash
git init
git add .
git commit -m "Initial project setup with MERN stack structure"
git branch -M main
# Add your remote repository
# git remote add origin https://github.com/yourusername/mern-ecommerce-capstone.git
# git push -u origin main
```

## 8. Environment Verification

### Test Frontend (should run on http://localhost:5173):
```bash
cd frontend
npm run dev
```

### Test Backend (should run on http://localhost:5000):
```bash
cd backend
npm run dev
```

## Next Steps for Day 1

1. **Frontend**: Modify `src/App.jsx` to include basic routing
2. **Backend**: Set up `server.js` with basic Express configuration
3. **Database**: Connect to MongoDB and test connection
4. **API**: Create first test endpoint
5. **Integration**: Test API call from frontend

This structure follows the 8-day plan and gives you a solid foundation to start building your e-commerce application immediately!