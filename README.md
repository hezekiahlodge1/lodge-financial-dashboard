Lodge Financial Dashboard
Overview
This is a single-page web application designed to help lodge administrators track and manage member dues and lodge expenses in real-time. It provides a simple, three-view interface: a financial Dashboard for overall balance, a Dues Roster for member management, and an Expenses Log.
The application uses GitHub Pages for deployment and Google Cloud's Firestore (via the Canvas environment) for all persistent, real-time data storage, ensuring data integrity and instant updates.
🚀 Features
Real-Time Dashboard: Calculates and displays the Net Balance (Income minus Expenses) instantly.
Dues Roster Management:
Add new members to the roster.
Update member display names.
Record new payments and automatically update the Year-To-Date (YTD) Paid summary for each member.
Expense Logging:
Log new expenses with title, amount, category, and receipt metadata.
All expenses immediately impact the Dashboard's Net Balance.
Authentication: The application uses secure, environment-provided custom tokens for automatic authentication, ensuring that only authorized users can access and modify the financial data.
🛠️ Technology Stack
This is a complete, single-file application (index.html) utilizing modern web standards:
HTML5 / JavaScript: Core structure and logic.
CSS / Tailwind CSS: Used for a fully responsive and clean mobile-first design.
Firebase Firestore: Used as the back-end database for real-time data synchronization.
Firebase Authentication: Used to secure the connection and authorize data access.
📂 Data Structure (Firestore Collections)
All data is automatically stored under your unique application ID (__app_id).
View
Purpose
Collection Path (Public)
Dues Roster
Stores member names and summary totals (YTD Paid).
/artifacts/{appId}/public/data/lodge_members
Expenses Log
Stores individual expense records.
/artifacts/{appId}/public/data/lodge_expenses
Payments
Stores detailed, individual payment receipts for each member.
/artifacts/{appId}/users/{memberId}/dues_payments

💡 How to Get Started
Deployment: Ensure the provided index.html file is saved in the root of your GitHub repository.
Access: Once GitHub Pages is enabled, access the dashboard via your unique GitHub Pages URL.
Initial Data Entry:
Navigate to the Dues Roster tab.
Use the "+ Add New Member" button to begin building your member roster.
Click "Edit/Pay" on a member to record their first payment.
Navigate to the Expenses tab to log any initial starting expenses.

