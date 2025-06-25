Fruit E-Commerce App
This is a full-stack e-commerce application for fruits and vegetables, built with:
Django & Django REST Framework (backend API)
React.js (frontend)
JWT-based authentication
Cart, Checkout, and Order history
Admin dashboard for product & order management

Features
User signup/login using JWT
Browse and filter products
Add to cart with quantity and size
Checkout with payment method
Order confirmation and order history
Admin can add/edit/delete products and view orders

Tech Stack
Frontend =>	React + Axios + React Router
Backend => Django + Django REST Framework
Auth => JWT (using djangorestframework-simplejwt)
Database => SQLite (default for dev)
CORS => django-cors-headers

Setup Instructions

Backend Setup (Django):
1. Clone the repo and navigate to backend folder:
   git clone <your-repo-url>
   cd fruits_backend
2. Create virtual environment:
   python -m venv venv
   source venv/bin/activate
3. Install dependencies:
   pip install -r requirements.txt
4. Run migrations:
   python manage.py makemigrations
   python manage.py migrate
5. Create admin user:
   python manage.py createsuperuser
6. Run the server:
   python manage.py runserver
   Django runs on http://localhost:8000/

Frontend Setup (React):
1. Navigate to frontend:
   cd frontend
2. Install dependencies:
   npm install
3. Start the development server:
   npm run dev
   React app runs on http://localhost:5173/

JWT Authentication:
Login: POST /api/users/token/
Add Authorization: Bearer <access_token> to all protected requests
Tokens are stored in localStorage in the browser

API Endpoints Summary:
| Endpoint                    | Method | Description              |
| --------------------------- | ------ | ------------------------ |
| `/api/products/`            | GET    | List all products        |
| `/api/orders/add/`          | POST   | Add to cart              |
| `/api/orders/list/`         | GET    | View cart                |
| `/api/orders/clear/`        | DELETE | Clear user cart          |
| `/api/orders/place/`        | POST   | Place order              |
| `/api/orders/history/`      | GET    | View order history       |
| `/api/users/token/`         | POST   | Get access/refresh token |
| `/api/users/token/refresh/` | POST   | Refresh access token     |

Admin Panel:
Visit: http://localhost:8000/admin/
Login with your superuser credentials
Manage Products and Orders
