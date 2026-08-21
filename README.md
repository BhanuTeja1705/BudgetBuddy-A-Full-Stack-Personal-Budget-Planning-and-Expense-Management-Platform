# 💰 BudgetBuddy

### A Full-Stack Personal Budget Planning and Expense Management Platform

BudgetBuddy is a full-stack personal finance management platform designed to help students manage pocket money, track daily expenses, manage income, create budgets, set savings goals, monitor spending habits, receive budget alerts, and generate financial reports.

The application provides a centralized dashboard with financial analytics and notifications to help users develop better financial awareness and money-management habits.

---

## 🚀 Key Features

### 🔐 Authentication

- User registration and login
- JWT-based authentication
- Protected API endpoints
- User-specific financial data
- Secure user data isolation

### 💸 Expense Management

- Add expenses
- Edit expenses
- Delete expenses
- Expense categorization
- Daily transaction history
- Automatic budget utilization calculation

Supported categories include:

- Food
- Travel
- Shopping
- Education
- Entertainment
- Miscellaneous

### 💵 Income Management

- Add income
- Update income
- Delete income
- Pocket money tracking
- Scholarship income tracking
- Freelance income tracking
- Monthly income tracking

### 📊 Budget Planning

- Create monthly budgets
- Category-wise budget allocation
- Budget utilization tracking
- Remaining budget calculation
- Overspending detection
- Budget status monitoring

### 🚨 Budget Alerts & Notifications

BudgetBuddy provides threshold-based budget alerts.

| Threshold | Notification | Priority |
|-----------|--------------|----------|
| 80% | Budget Reached 80% | LOW |
| 90% | Budget Reached 90% | MEDIUM |
| 100%+ | Budget Exceeded Limit | HIGH |

Features include:

- In-app notifications
- Global notification bell
- Unread notification count
- Mark notification as read
- Mark all notifications as read
- Duplicate alert prevention
- Budget threshold detection
- SMTP email alerts
- Email alerts sent to the registered user's email address

### 🎯 Savings Goals

Users can create and track personal savings goals.

Features include:

- Create savings goals
- Set target amounts
- Track saved amount
- Progress visualization
- Target date management
- Goal completion tracking
- Goal milestone notifications

Example goals:

- New Laptop Fund
- Japan Trip Fund
- Emergency Savings

### 📈 Analytics Dashboard

The dashboard provides a financial overview including:

- Total Income
- Total Expenses
- Current Balance
- Total Savings
- Total Budget
- Remaining Budget
- Category-wise spending
- Monthly expense trends
- Recent transactions
- Active savings goals
- Latest notifications
- Financial summaries

### 🔔 Global Notification System

BudgetBuddy includes a global notification system available throughout the application.

The notification bell provides:

- Unread notification count
- Instant notification count updates
- Navigation to the Notifications page
- Budget alert visibility
- Priority-based notification display

### 📑 Reports & Export

BudgetBuddy supports multiple financial report formats:

- JSON
- PDF
- Excel

#### PDF Reports

PDF reports include:

- Financial Summary
- Expense History
- Savings Goal Progress
- Recent Transactions

#### Excel Reports

Excel reports contain six worksheets:

1. Financial Summary
2. Income
3. Expenses
4. Budgets
5. Savings Goals
6. Notifications

#### JSON Reports

JSON export is also available for structured financial data.

Example endpoint:

```text
GET /api/reports/export/?format=json
```

### 📧 Email Notifications

BudgetBuddy supports budget alert emails through Gmail SMTP.

Emails are triggered when:

- Budget reaches 80%
- Budget reaches 90%
- Budget reaches 100% or more

The recipient is dynamically taken from the email address provided during user registration.

---

## 🏗️ System Architecture

```text
┌──────────────────────────────┐
│       React Frontend         │
│                              │
│ Dashboard                    │
│ Expenses                     │
│ Income                       │
│ Budgets                      │
│ Savings Goals                │
│ Notifications                │
│ Analytics                    │
│ Reports                      │
└──────────────┬───────────────┘
               │
               │ REST API + JWT
               ▼
┌──────────────────────────────┐
│        Django Backend        │
│                              │
│ Authentication               │
│ Expense Management           │
│ Income Management            │
│ Budget Management            │
│ Savings Goals                │
│ Notifications                │
│ Analytics                    │
│ Reports & Export             │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│          Database            │
│                              │
│ SQLite - Development         │
│ PostgreSQL - Production      │
└──────────────────────────────┘
               │
               ▼
┌──────────────────────────────┐
│      External Services       │
│                              │
│ Gmail SMTP                   │
│ Budget Alert Emails          │
└──────────────────────────────┘
```

### Architecture Flow

**React Frontend → REST API + JWT → Django Backend → Database → Gmail SMTP**

---

## 🛠️ Technology Stack

### Frontend

- React.js
- JavaScript
- React Router
- Axios
- CSS
- Vite

### Backend

- Python
- Django
- Django REST Framework
- SimpleJWT

### Database

- SQLite for local development
- PostgreSQL for production

### Authentication

- JWT Authentication
- Django Authentication System

### Reporting

- ReportLab
- OpenPyXL
- JSON

### Email

- Gmail SMTP
- Django Email Backend

### Testing

- Django Test Client
- Python automated test scripts
- Frontend production build testing
- End-to-end testing

### Development Tools

- Visual Studio Code
- Git
- GitHub
- Postman
- Chrome

---

## 📁 Project Structure

```text
BudgetBuddy/
│
├── backend/
│   ├── config/
│   │   ├── settings.py
│   │   ├── urls.py
│   │   └── ...
│   │
│   ├── expenses/
│   │   ├── models.py
│   │   ├── serializers.py
│   │   ├── views.py
│   │   └── urls.py
│   │
│   ├── savings/
│   │   ├── models.py
│   │   ├── serializers.py
│   │   ├── views.py
│   │   ├── utils.py
│   │   └── urls.py
│   │
│   ├── reports/
│   │   ├── views.py
│   │   ├── utils.py
│   │   └── urls.py
│   │
│   ├── notifications/
│   │   ├── models.py
│   │   ├── serializers.py
│   │   ├── views.py
│   │   └── urls.py
│   │
│   ├── manage.py
│   └── requirements.txt
│
├── frontend/
│   ├── src/
│   │   ├── pages/
│   │   │   ├── Dashboard.jsx
│   │   │   ├── Expenses.jsx
│   │   │   ├── Income.jsx
│   │   │   ├── Budgets.jsx
│   │   │   ├── Savings.jsx
│   │   │   ├── Notifications.jsx
│   │   │   ├── Analytics.jsx
│   │   │   └── Reports.jsx
│   │   │
│   │   ├── layouts/
│   │   ├── services/
│   │   └── ...
│   │
│   ├── package.json
│   └── ...
│
├── screenshots/
├── .env.example
├── .gitignore
├── LICENSE
├── README.md
└── manage.py
```

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/BhanuTeja1705/BudgetBuddy-A-Full-Stack-Personal-Budget-Planning-and-Expense-Management-Platform.git
```

Move into the project directory:

```bash
cd BudgetBuddy-A-Full-Stack-Personal-Budget-Planning-and-Expense-Management-Platform
```

---

## 🐍 Backend Setup

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

### 3. Activate the Virtual Environment

#### Windows

```bash
venv\Scripts\activate
```

#### Linux / macOS

```bash
source venv/bin/activate
```

### 4. Install Backend Dependencies

```bash
pip install -r backend/requirements.txt
```

---

## 🗄️ Database Setup

Run migrations:

```bash
cd backend
python manage.py migrate
```

Run the Django development server:

```bash
python manage.py runserver
```

Backend will be available at:

```text
http://127.0.0.1:8000/
```

---

## ⚛️ Frontend Setup

Open another terminal.

Navigate to the frontend:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the frontend:

```bash
npm run dev
```

Frontend will normally be available at:

```text
http://localhost:5173/
```

---

## 🔑 Environment Variables

Create a `.env` file based on `.env.example`.

Example:

```env
SECRET_KEY=your-secret-key
DEBUG=True

ALLOWED_HOSTS=127.0.0.1,localhost

EMAIL_BACKEND=django.core.mail.backends.smtp.EmailBackend
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USE_TLS=True

EMAIL_HOST_USER=your-budgetbuddy-email@gmail.com
EMAIL_HOST_PASSWORD=your-16-character-google-app-password

DEFAULT_FROM_EMAIL=your-budgetbuddy-email@gmail.com
```

For Gmail SMTP, use a **Google App Password** rather than your normal Gmail password.

> Never commit `.env` or SMTP credentials to GitHub.

---

## 📧 SMTP Email Flow

BudgetBuddy uses the email address provided during registration as the notification recipient.

```text
User Registration
       ↓
User provides email address
       ↓
Email stored in Django User account
       ↓
User creates budget
       ↓
User adds expenses
       ↓
Budget utilization calculated
       ↓
80% / 90% / 100% threshold reached
       ↓
In-App Notification Created
       ↓
Budget Alert Email Generated
       ↓
Gmail SMTP
       ↓
Registered User's Email Inbox
```

---

## 🚨 Budget Alert Flow

```text
Expense Added
     ↓
Calculate Category Spending
     ↓
Compare Spending With Budget
     ↓
┌─────────────────────────┐
│ Less than 80%           │
│ No Budget Alert         │
└─────────────────────────┘
     ↓
┌─────────────────────────┐
│ 80% Reached             │
│ LOW Priority Alert      │
└─────────────────────────┘
     ↓
┌─────────────────────────┐
│ 90% Reached             │
│ MEDIUM Priority Alert   │
└─────────────────────────┘
     ↓
┌─────────────────────────┐
│ 100%+ Reached           │
│ HIGH Priority Alert     │
└─────────────────────────┘
     ↓
In-App Notification + Email
```

Budget alerts use deduplication logic so the same threshold does not repeatedly generate duplicate notifications or emails.

---

## 📊 Dashboard

The BudgetBuddy dashboard provides a centralized financial overview.

### Financial Summary

- Total Income
- Total Expenses
- Current Balance
- Total Budget
- Remaining Budget
- Total Savings

### Spending Analysis

- Category-wise spending
- Spending percentages
- Monthly expense trends

### Financial Activity

- Recent transactions
- Active savings goals
- Latest notifications

---

## 📈 Analytics

The Analytics section provides visual financial insights including:

- Category-wise spending analysis
- Monthly expense trends
- Income versus expenses
- Savings goal progress
- Budget utilization
- Financial summaries

---

## 📑 Reports

The Reports module provides different report views and export options.

### Available Reports

- Monthly reports
- Expense reports
- Savings reports
- Financial summaries

### Export Formats

```text
PDF
Excel
JSON
```

### PDF Export

```text
GET /api/reports/export/pdf/
```

### Excel Export

```text
GET /api/reports/export/excel/
```

### JSON Export

```text
GET /api/reports/export/?format=json
```

---

## 🔔 Notifications

Notifications are generated for important financial events.

Examples include:

- Budget created
- Budget updated
- Budget deleted
- Expense added
- Expense updated
- Expense deleted
- Budget reached 80%
- Budget reached 90%
- Budget exceeded
- Savings goal milestones
- Goal achievement

Notifications are displayed in the Notifications module and through the global notification bell.

---

## 🔒 User Data Isolation

Each user's financial information is isolated.

Users can only access their own:

- Expenses
- Income
- Budgets
- Savings Goals
- Notifications
- Reports
- Analytics

The backend validates the authenticated user before returning financial data.

---

## 🧪 Testing

The project includes automated testing for major application workflows.

### Django System Check

```bash
python manage.py check
```

### Database Migrations

```bash
python manage.py migrate
```

### Backend Tests

```bash
python manage.py test
```

### Frontend Build

```bash
cd frontend
npm run build
```

### End-to-End Testing

The project includes testing for:

- Registration
- Login
- JWT authentication
- Expense creation
- Expense update
- Expense deletion
- Income management
- Budget creation
- Budget calculations
- Savings goals
- Notifications
- Budget alerts
- Analytics
- Reports
- PDF export
- Excel export
- JSON export
- User data isolation
- Frontend-backend integration

---

## 🛡️ Validation & Error Handling

BudgetBuddy validates financial inputs to prevent invalid data.

Examples include:

- Negative expense amounts
- Negative income amounts
- Invalid budget values
- Invalid month/year values
- Invalid savings goal values
- Saved amount greater than target amount
- Unauthorized API access
- Missing required fields

The application provides meaningful error responses to help users correct invalid inputs.

---

## 🔄 Complete User Workflow

```text
Register
   ↓
Login
   ↓
Dashboard
   ↓
Add Income
   ↓
Create Budget
   ↓
Add Expenses
   ↓
Track Budget Utilization
   ↓
Receive Budget Alerts
   ↓
Receive Email Notifications
   ↓
Create Savings Goals
   ↓
Track Financial Progress
   ↓
View Analytics
   ↓
Generate Reports
   ↓
Export PDF / Excel / JSON
```

---

## 🎯 Project Objectives

BudgetBuddy aims to help students:

- Develop financial awareness
- Track daily spending
- Manage pocket money
- Plan monthly budgets
- Avoid overspending
- Track savings goals
- Understand spending patterns
- Receive timely budget alerts
- Generate financial reports
- Improve personal financial discipline

---

## 📌 Future Enhancements

Potential future improvements include:

- Google OAuth2 login
- GitHub OAuth2 login
- PostgreSQL production deployment
- Advanced financial analytics
- Interactive charts
- Mobile application
- Push notifications
- AI-powered financial recommendations
- Automated monthly financial summaries
- Advanced spending predictions

---

## 👨‍💻 Developer

### Bhanu Teja

Computer Science & Engineering Student

GitHub:  
https://github.com/BhanuTeja1705

LinkedIn:  
https://www.linkedin.com/in/bhanuteja-goriparthi

---

## 📄 License

This project is licensed under the MIT License.

See the `LICENSE` file for more information.

---

## ⭐ Acknowledgement

BudgetBuddy was developed as a full-stack personal finance management project with the goal of providing students with a simple and practical platform for managing income, expenses, budgets, savings goals, notifications, analytics, and financial reports.

---

# 💰 BudgetBuddy

**Track. Plan. Save. Spend Smart.**
