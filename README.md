# 🛒 MERN Stack E-Commerce Platform

A fully functional, high-performance E-commerce application built with the **MERN** (MongoDB, Express, React, Node.js) stack. This platform features a comprehensive Admin Dashboard, robust authentication system, real-time sales analytics, and a seamless shopping experience.

---

## 📋 Table of Contents
- [Overview](#overview)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Installation & Setup](#installation--setup)
- [Usage](#usage)
- [API Documentation](#api-documentation)
- [Contributing](#contributing)
- [License](#license)

---

## 📌 Overview

This MERN E-Commerce Platform is designed to provide both customers and administrators with an intuitive and powerful interface for online shopping and business management. The application emphasizes security, scalability, and user experience with modern web technologies.

**Key Highlights:**
- ✅ Full-stack JavaScript/TypeScript implementation
- ✅ Responsive and mobile-friendly UI
- ✅ Secure JWT-based authentication
- ✅ Real-time data visualization
- ✅ RESTful API architecture
- ✅ MongoDB for flexible data modeling

---

## 🌟 Key Features

### 👤 Customer Features

#### 🔐 **Authentication & Account Management**
- Secure user registration with email verification
- JWT token-based login with HTTP-only cookies for enhanced security
- Password hashing using industry-standard algorithms
- Session management and auto-logout functionality
- User profile management with editable information

#### 🛍️ **Shopping Experience**
- Browse products with advanced filtering (category, price range, ratings)
- Intuitive product search with real-time suggestions
- Detailed product pages with images, descriptions, and customer reviews
- Add/remove items from cart with instant quantity updates
- Persistent shopping cart (saved in localStorage and database)
- Wishlist functionality for saving favorite products

#### 💳 **Order Management**
- Seamless checkout process with payment integration
- Multiple payment method options
- Order history with detailed information (items, dates, amounts)
- Real-time order status tracking (Pending → Paid → Delivered)
- Order cancellation and return requests
- Invoice generation and download

#### ⭐ **Additional Features**
- Product ratings and reviews from verified buyers
- User dashboard for personal information and preferences
- Email notifications for order updates
- Address book for multiple shipping addresses

---

### 🛡️ Admin Features (Admin Dashboard)

#### 📊 **Sales Analytics & Reporting**
- Interactive sales dashboard with real-time data visualization using **ApexCharts**
- Sales charts: Revenue trends, daily/weekly/monthly analytics
- Customer acquisition metrics and user growth analysis
- Top-performing products and categories
- Profit margin analysis and financial reports
- Customizable date range filters for data analysis

#### 📦 **Product Management**
- Complete CRUD (Create, Read, Update, Delete) operations for products
- Bulk product import/export functionality
- Product categorization and subcategory management
- Inventory management with low-stock alerts
- Product images and gallery management
- SEO optimization fields (meta titles, descriptions, keywords)
- Product variants and specifications handling

#### 📋 **Order Management**
- View all customer orders with detailed information
- Filter and search orders by status, date, or customer
- Mark orders as "Paid" or "Delivered"
- Order fulfillment tracking
- Generate packing slips and shipping labels
- Handle order cancellations and refunds
- Export order data for accounting purposes

#### 👥 **User Management**
- View all registered users with account details
- User role assignment (Customer, Admin, Moderator)
- Block or deactivate user accounts
- View user activity and order history
- Manage user permissions and access levels

#### ⚙️ **System Settings**
- Admin account management
- Database backups and recovery options
- API key and payment gateway configuration
- Email template customization
- System configuration and preferences

---

## 🛠️ Tech Stack

### **Frontend Technologies**

| Technology | Purpose | Version |
|---|---|---|
| **React.js** | Library for building dynamic, interactive user interfaces | Latest |
| **Vite** | Modern, fast build tool and development server | Latest |
| **Redux Toolkit** | Centralized state management for complex application states | Latest |
| **RTK Query** | Efficient API caching, data fetching, and synchronization | Latest |
| **Tailwind CSS** | Utility-first CSS framework for responsive, modern styling | v3+ |
| **ApexCharts** | Interactive charts and graphs for data visualization | Latest |
| **Axios** | HTTP client for making API requests | Latest |
| **React Router** | Client-side routing for seamless navigation | v6+ |

### **Backend Technologies**

| Technology | Purpose | Version |
|---|---|---|
| **Node.js** | JavaScript runtime for server-side execution | v14+ |
| **Express.js** | Lightweight web framework for building RESTful APIs | v4+ |
| **MongoDB** | NoSQL database for flexible, scalable data storage | Latest |
| **Mongoose** | ODM (Object Document Mapper) for MongoDB | Latest |
| **JWT (JSON Web Tokens)** | Secure, stateless authentication mechanism | Industry Standard |
| **Bcryptjs** | Password hashing and encryption | Latest |
| **Dotenv** | Environment variable management | Latest |
| **Cors** | Cross-Origin Resource Sharing middleware | Latest |

### **Additional Tools & Libraries**

- **Git & GitHub**: Version control and collaboration
- **Postman**: API testing and documentation
- **ESLint & Prettier**: Code quality and formatting
- **Nodemon**: Development server with auto-reload

---

## 📁 Project Structure

```
EccomerceProject/
│
├── 📂 Backend/                          # Node.js & Express Backend
│   ├── 📂 config/                       # Database and environment configuration
│   │   └── db.js                        # MongoDB connection setup
│   ├── 📂 models/                       # Mongoose schemas and data models
│   │   ├── User.js                      # User schema (customers and admins)
│   │   ├── Product.js                   # Product schema with variants
│   │   ├── Order.js                     # Order and order items schema
│   │   ├── Category.js                  # Product categories
│   │   └── Review.js                    # Customer reviews and ratings
│   ├── 📂 controllers/                  # Business logic and route handlers
│   │   ├── authController.js            # Authentication logic
│   │   ├── productController.js         # Product CRUD operations
│   │   ├── orderController.js           # Order management
│   │   ├── userController.js            # User management
│   │   └── analyticsController.js       # Sales analytics
│   ├── 📂 routes/                       # API route definitions
│   │   ├── authRoutes.js                # Auth endpoints
│   │   ├── productRoutes.js             # Product endpoints
│   │   ├── orderRoutes.js               # Order endpoints
│   │   └── userRoutes.js                # User endpoints
│   ├── 📂 middlewares/                  # Custom middleware functions
│   │   ├── authMiddleware.js            # JWT verification
│   │   ├── errorHandler.js              # Global error handling
│   │   ├── validateInput.js             # Input validation
│   │   └── adminCheck.js                # Admin authorization
│   ├── 📂 data/                         # Seed data for initial database population
│   │   ├── products.json                # Sample products
│   │   └── categories.json              # Sample categories
│   ├── 📂 utils/                        # Helper functions and utilities
│   │   ├── emailService.js              # Email sending logic
│   │   ├── paymentService.js            # Payment gateway integration
│   │   └── validators.js                # Data validation utilities
│   ├── server.js                        # Express app initialization and server start
│   ├── .env                             # Environment variables (not committed)
│   └── package.json                     # Dependencies and scripts
│
├── 📂 Frontend-Ecommerce/                # React & Vite Frontend
│   ├── 📂 src/
│   │   ├── 📂 components/               # Reusable React components
│   │   │   ├── 📂 Header/               # Navigation bar, search, cart icon
│   │   │   ├── 📂 Footer/               # Footer component
│   │   │   ├── 📂 ProductCard/          # Product display card
│   │   │   ├── 📂 Cart/                 # Shopping cart components
│   │   │   ├── 📂 Checkout/             # Checkout form components
│   │   │   ├── 📂 Dashboard/            # Admin dashboard components
│   │   │   └── 📂 Common/               # Buttons, modals, spinners
│   │   │
│   │   ├── 📂 pages/                    # Full page components
│   │   │   ├── HomePage.jsx             # Landing/home page
│   │   │   ├── ShopPage.jsx             # Products listing page
│   │   │   ├── ProductDetail.jsx        # Individual product page
│   │   │   ├── CartPage.jsx             # Shopping cart page
│   │   │   ├── CheckoutPage.jsx         # Checkout page
│   │   │   ├── OrdersPage.jsx           # User orders history
│   │   │   ├── AdminDashboard.jsx       # Admin main dashboard
│   │   │   ├── ProductManagement.jsx    # Admin product management
│   │   │   ├── OrderManagement.jsx      # Admin order management
│   │   │   ├── UserManagement.jsx       # Admin user management
│   │   │   ├── LoginPage.jsx            # User login
│   │   │   ├── SignupPage.jsx           # User registration
│   │   │   └── NotFound.jsx             # 404 page
│   │   │
│   │   ├── 📂 redux/                    # Redux state management
│   │   │   ├── 📂 slices/               # Redux slices (features)
│   │   │   │   ├── authSlice.js         # Auth state (user, token)
│   │   │   │   ├── cartSlice.js         # Cart state management
│   │   │   │   ├── productSlice.js      # Products state
│   │   │   │   ├── orderSlice.js        # Orders state
│   │   │   │   └── filterSlice.js       # Filter state
│   │   │   │
│   │   │   ├── 📂 api/                  # RTK Query API slices
│   │   │   │   ├── authApi.js           # Auth API endpoints
│   │   │   │   ├── productApi.js        # Product API endpoints
│   │   │   │   ├── orderApi.js          # Order API endpoints
│   │   │   │   └── userApi.js           # User API endpoints
│   │   │   │
│   │   │   └── store.js                 # Redux store configuration
│   │   │
│   │   ├── 📂 hooks/                    # Custom React hooks
│   │   │   ├── useAuth.js               # Authentication hook
│   │   │   ├── useCart.js               # Cart management hook
│   │   │   └── useFilters.js            # Filtering logic hook
│   │   │
│   │   ├── 📂 styles/                   # Global CSS and Tailwind configuration
│   │   │   ├── index.css                # Global styles
│   │   │   └── tailwind.config.js       # Tailwind configuration
│   │   │
│   │   ├── 📂 utils/                    # Utility functions
│   │   │   ├── api.js                   # API configuration and interceptors
│   │   │   ├── helpers.js               # Helper functions
│   │   │   └── constants.js             # App constants and configurations
│   │   │
│   │   ├── App.jsx                      # Main app component
│   │   └── main.jsx                     # React DOM rendering
│   │
│   ├── vite.config.js                   # Vite configuration
│   ├── tailwind.config.js               # Tailwind CSS configuration
│   ├── .env                             # Environment variables (not committed)
│   └── package.json                     # Dependencies and scripts
│
├── 📂 .git/                             # Git repository (version control)
├── .gitignore                           # Files to exclude from git
├── README.md                            # Project documentation (this file)
└── LICENSE                              # License information

```

---

## 🚀 Installation & Setup

### Prerequisites
- **Node.js** (v14 or higher)
- **npm** or **yarn** package manager
- **MongoDB** (local or cloud instance)
- **Git** for version control

### Backend Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/shivam-pandey123-coder/EccomerceProject.git
   cd EccomerceProject/Backend
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Create `.env` file** and configure:
   ```env
   PORT=5000
   MONGODB_URI=mongodb://localhost:27017/ecommerce
   JWT_SECRET=your_jwt_secret_key
   NODE_ENV=development
   PAYMENT_GATEWAY_KEY=your_payment_key
   EMAIL_SERVICE_KEY=your_email_key
   ```

4. **Seed the database (optional)**
   ```bash
   npm run seed
   ```

5. **Start the server**
   ```bash
   npm start
   # or for development with auto-reload
   npm run dev
   ```

### Frontend Setup

1. **Navigate to frontend directory**
   ```bash
   cd ../Frontend-Ecommerce
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Create `.env` file**
   ```env
   VITE_API_URL=http://localhost:5000
   ```

4. **Start the development server**
   ```bash
   npm run dev
   ```

5. **Build for production**
   ```bash
   npm run build
   ```

---

## 📖 Usage

### For Customers
1. Navigate to the homepage
2. Browse products or use the search feature
3. Click on a product to view details
4. Add items to cart and proceed to checkout
5. Complete payment and track orders in your account

### For Admins
1. Login with admin credentials
2. Access the admin dashboard
3. Manage products, orders, and users
4. View sales analytics and generate reports
5. Configure system settings

---

## 📚 API Documentation

### Authentication Endpoints
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `GET /api/auth/profile` - Get user profile (protected)

### Product Endpoints
- `GET /api/products` - Get all products
- `GET /api/products/:id` - Get product details
- `POST /api/products` - Create product (admin only)
- `PUT /api/products/:id` - Update product (admin only)
- `DELETE /api/products/:id` - Delete product (admin only)

### Order Endpoints
- `POST /api/orders` - Create new order
- `GET /api/orders` - Get user orders
- `GET /api/orders/:id` - Get order details
- `PUT /api/orders/:id` - Update order (admin only)

### User Endpoints
- `GET /api/users` - Get all users (admin only)
- `GET /api/users/:id` - Get user details
- `PUT /api/users/:id` - Update user information
- `DELETE /api/users/:id` - Delete user (admin only)

---

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/YourFeature`)
3. Commit changes (`git commit -m 'Add YourFeature'`)
4. Push to branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

### Code Standards
- Follow ESLint and Prettier configurations
- Write meaningful commit messages
- Add tests for new features
- Update documentation as needed

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Shivam Pandey** - [GitHub Profile](https://github.com/shivam-pandey123-coder)

---

## 📞 Support & Contact

For questions, issues, or suggestions:
- Open an [GitHub Issue](https://github.com/shivam-pandey123-coder/EccomerceProject/issues)
- Create a [GitHub Discussion](https://github.com/shivam-pandey123-coder/EccomerceProject/discussions)

---

## 🎯 Future Enhancements

- [ ] Mobile app (React Native)
- [ ] Advanced recommendation engine
- [ ] Multi-vendor marketplace
- [ ] Live chat support
- [ ] Loyalty program system
- [ ] Enhanced security features (2FA, etc.)
- [ ] Performance optimization
- [ ] GraphQL API implementation

---

**Last Updated:** June 2026  
**Status:** ✅ Actively Maintained
