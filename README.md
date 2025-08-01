# Coursecraft: A MERN Stack Course-Selling Platform

Welcome to Coursecraft, a full-stack application designed to be a modern and intuitive online learning platform. It allows users to browse and purchase courses, while leveraging Stripe for secure and seamless payment processing.

✨ **Features**
* **User Authentication:** Secure sign-up and log-in with role-based access control for users and administrators.
* **Course Catalog:** Browse a wide range of courses with detailed descriptions and lesson plans, fetched from a RESTful API.
* **Secure Payments:** Integrated with the Stripe API to handle all payment transactions safely in test mode.
* **Admin Panel:** A dedicated and protected section for administrators to manage courses (Create, Read, Update, Delete).
* **Responsive Design:** Optimized for both desktop and mobile devices using Tailwind CSS.
* **Modular Architecture:** A robust and scalable foundation using separate frontend and backend services.

---

🚀 **Technologies Used**
**Client (Frontend):**
* **React:** For building the dynamic user interface.
* **Vite:** A fast build tool for the development server.
* **Tailwind CSS:** A utility-first framework for responsive and attractive styling.
* **`@stripe/react-stripe-js`:** React components for secure payment forms.
* **`lucide-react`:** For clean and professional icons.

**Server (Backend):**
* **Node.js & Express.js:** A scalable and performant API layer.
* **MongoDB Atlas:** A cloud-hosted NoSQL database for data storage.
* **Mongoose:** An ODM library for data modeling and validation.
* **Stripe Node.js Library:** For communicating with the Stripe API and processing payments.
* **`jsonwebtoken`:** For secure, stateless user authentication with JWTs.
* **`bcryptjs`:** For secure password hashing.
* **Firebase Admin SDK:** For file storage integration (e.g., course thumbnails, future content).

---

⚙️ **Prerequisites**
Before you begin, ensure you have the following installed on your machine:

* **Node.js** (v14.x or later)
* **npm** (usually comes with Node.js)
* **MongoDB** (via MongoDB Atlas)
* A **Stripe Account** to get your API keys.
* A **Firebase Project** for file storage and a `serviceAccountKey.json`.

---

📦 **Installation & Setup**
1.  **Clone the repository** to your local machine:
    ```bash
    git clone [https://github.com/rushikeshxdev/your-project-repo.git](https://github.com/rushikeshxdev/your-project-repo.git)
    cd your-project-repo
    ```

2.  **Backend Setup**
    Navigate to the `server` directory and install dependencies:
    ```bash
    cd server
    npm install
    ```
    Create a `.env` file in the `server` directory with the following variables:
    ```
    PORT=5000
    MONGO_URI=your_mongodb_connection_string
    STRIPE_SECRET_KEY=your_stripe_secret_key
    JWT_SECRET=your_jwt_secret_key
    FIREBASE_STORAGE_BUCKET=your-project-id.appspot.com
    ```
    *Note: For `MONGO_URI`, use your connection string from MongoDB Atlas. For Stripe, get your **secret key** from the Stripe Dashboard. Choose a strong, random string for `JWT_SECRET`. The `FIREBASE_STORAGE_BUCKET` URL can be found in your Firebase Storage dashboard.*
    *Run the backend server:*
    ```bash
    npm start
    ```

3.  **Frontend Setup**
    Navigate to the `my-coursera-app` directory and install dependencies:
    ```bash
    cd ../my-coursera-app
    npm install
    ```
    Create a `.env` file in the `my-coursera-app` directory with the following variables:
    ```
    VITE_API_BASE_URL=http://localhost:5000/api/auth
    VITE_API_BASE_URL_COURSES=http://localhost:5000/api/courses
    VITE_API_BASE_URL_ORDERS=http://localhost:5000/api/orders
    VITE_STRIPE_PUBLISHABLE_KEY=your_stripe_publishable_key
    ```
    *Note: For `VITE_STRIPE_PUBLISHABLE_KEY`, use your **publishable key** from the Stripe Dashboard. The API URLs point to your backend server.*
    *Run the frontend development server:*
    ```bash
    npm run dev
    ```

---

🖥️ **Usage**
1.  Open your browser and navigate to `http://localhost:5173/`.
2.  Sign up or log in to access the platform.
3.  Browse the courses and view detailed information.
4.  (Admin Only): Access the Admin Panel from the Dashboard to add, edit, or delete courses.
5.  Proceed to checkout and complete the payment using Stripe's test card data.

---

📂 **Project Structure**

.
├── my-coursera-app/
│   ├── src/
│   │   ├── pages/
│   │   ├── components/
│   │   ├── services/
│   │   └── App.jsx
│   ├── .env
│   └── package.json
└── server/
├── config/
│   ├── db.js
│   └── firebaseAdmin.js
├── controllers/
│   ├── authController.js
│   ├── courseController.js
│   └── orderController.js
├── middleware/
│   ├── authMiddleware.js
│   └── errorHandler.js
├── models/
│   ├── Course.js
│   ├── Order.js
│   └── User.js
├── routes/
│   ├── authRoutes.js
│   ├── courseRoutes.js
│   └── orderRoutes.js
├── .env
└── package.json


---

🤝 **Contributing**
Contributions are always welcome! If you have suggestions for features or improvements, please create an issue or submit a pull request.

---

📄 **License**
This project is licensed under the MIT License.
