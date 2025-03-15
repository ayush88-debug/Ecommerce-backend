
# 🛒 Ecommerce Backend

A robust **Node.js & Express** backend for an eCommerce platform, featuring **secure authentication, product management, and wishlist handling**. Built with **MongoDB, Mongoose, JWT, and Cloudinary**, it ensures seamless scalability and optimized performance.


## 🚀 Features

- **User Authentication** – Secure login, registration, and password hashing with bcrypt.
- **Product Management** – CRUD operations for products with Cloudinary image storage.
- **Wishlist Handling** – Users can add/remove products to their wishlist.
- **Secure API** – Protected routes with role-based access control.
- **Efficient Database Operations** – MongoDB aggregation, pagination, and indexing.


## 🛠️ Tech Stack

```json
["Node.js", "Express", "MongoDB", "Mongoose", "JWT", "Bcrypt", "Cloudinary", "Multer", "Cookie-Parser", "Cors", "Dotenv", "Nodemon"]
```

---

## 📂 Project Structure

```
Ecommerce-backend/
│── public/                # Static files
│── src/
│   ├── controllers/       # Business logic (User, Product)
│   ├── db/                # Database connection
│   ├── middlewares/       # Authentication & file handling
│   ├── models/            # Mongoose models (User, Product)
│   ├── routes/            # API routes (User, Product)
│   ├── utils/             # Helper functions (Cloudinary, Responses)
│── .env.sample            # Environment variable example
│── package.json           # Project dependencies
│── README.md              # Project documentation
```

---

## 🔧 Installation & Setup

### 1️⃣ Clone the repository
```sh
git clone https://github.com/ayush88-debug/Ecommerce-backend.git
cd Ecommerce-backend
```

### 2️⃣ Install dependencies
```sh
npm install
```

### 3️⃣ Set up environment variables  
Create a `.env` file and configure:
```env
PORT=4000
MONGODB_URL="your_mongodb_connection_string"
CORS_ORIGIN="your_frontend_url"
ACCESS_TOKEN_SECRET="your_secret"
REFRESH_TOKEN_SECRET="your_secret"
CLOUDINARY_CLOUD_NAME="your_cloud_name"
CLOUDINARY_API_KEY="your_api_key"
CLOUDINARY_API_SECRET="your_api_secret"
```

### 4️⃣ Run the project
```sh
npm run dev
```

---

## 📌 API Endpoints

### **User API Endpoints**
| Method  | Endpoint                         | Description                                   | Authentication Required |
|---------|---------------------------------|-----------------------------------------------|-------------------------|
| `POST`  | `/api/v1/user/register`         | Register a new user                          | ❌ No                   |
| `POST`  | `/api/v1/user/login`            | User login                                   | ❌ No                   |
| `POST`  | `/api/v1/user/refresh-access-token` | Refresh access token                     | ❌ No                   |
| `POST`  | `/api/v1/user/logout`           | User logout                                  | ✅ Yes                  |
| `PATCH` | `/api/v1/user/change-password`  | Change current password                      | ✅ Yes                  |
| `GET`   | `/api/v1/user/current-user`     | Get currently logged-in user                 | ✅ Yes                  |
| `PATCH` | `/api/v1/user/update-account-details` | Update user account details            | ✅ Yes                  |
| `PATCH` | `/api/v1/user/update-avatar`    | Update user avatar image                     | ✅ Yes                  |
| `PATCH` | `/api/v1/user/update-coverImage` | Update user cover image                     | ✅ Yes                  |
| `GET`   | `/api/v1/user/u/:username`      | Get user profile by username                 | ❌ No                   |
| `GET`   | `/api/v1/user/wishlist`         | Get user's wishlist                          | ✅ Yes                  |



## 🛡️ Security Features

- **JWT Authentication** – Secure login & token refresh.
- **Bcrypt Password Hashing** – Encrypts user passwords before storage.
- **Role-Based Access Control** – Restricts access to protected routes.


## 🤝 Contributing

1. **Fork the repository**  
2. **Create a new branch** (`feature-branch`)  
3. **Commit your changes**  
4. **Push the branch & submit a PR**  
