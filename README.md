BiblioBay 

Project Overview
-----------------
BiblioBay is a comprehensive, client-side rendered (HTML, CSS, and vanilla JavaScript) E-commerce application for books, complete with a full-featured User Interface and a robust Admin Management System.
The application uses Web Storage (localStorage) extensively for user authentication, session management, shopping cart persistence, and CRUD operations for administrative data (users, books).

Key Features
-------------
1. User Front-End (E-commerce)
- Book Browsing: Landing page (index.html) featuring book sections (e.g., featured, new releases) and a search bar.
- User Authentication: Complete Sign Up (register.html) and Sign In (login.html) functionality.
- Storage: User data is stored and managed using localStorage (auth.js).
- Session: Maintains a user session (currentUser in localStorage) and redirects unauthenticated users (user-common.js).
- User Dashboard (dashboard.html): A private area for logged-in users.
- Shopping Cart: Persistent, user-specific shopping cart (cart_[username]) managed in localStorage (user-common.js).
- Features include adding/removing items, updating quantities, and a mock Checkout process.

2. Admin Management System
- A separate, secure area for site administrators to manage all aspects of the platform.
- Admin Authentication (admin-login.html): Simple, hardcoded login logic.
- Username: admin
- Password: admin123
- Session: Saves state as adminLoggedIn: 'true' in localStorage.
- Dashboard (admin-dashboard.html): Overview of key metrics (Sales, Users, Orders) and recent activity.
- Book Management (admin-books.html): Full CRUD interface for managing the book inventory, including search and filter by category.
- User Management (admin-users.html): Full CRUD interface for managing registered customer accounts, including search and filter by role/status.
- Order Management (admin-orders.html): Allows administrators to view and manage customer orders.
- Includes logic for calculating financial details: Subtotal, 8% Tax, $5.00 Shipping, and Total.
- Review/Blog Management: Separate sections for controlling content (admin-reviews.html, admin-blogs.html) with search and filtering capabilities (e.g., filter reviews by star rating).
- System Settings (admin-settings.html): Allows customization of email templates (Welcome, Order Confirmation, Password Reset).

Technical Stack
----------------
- Front-End: HTML5
- Styling: CSS3, heavily utilizing Bootstrap v5.0.2 for layout and components, alongside custom CSS (style.css, loginReg.css, 404Style.css).
- Logic: Vanilla JavaScript (auth.js, user-common.js, script.js).
- Data: Sample book data defined in data.js.
- Dependencies (CDN): Font Awesome (icons), Swiper (sliders), Feather Icons (login/register).

Project Structure
------------------
- Directory/File	Type	Purpose
- index.html	HTML	Main E-commerce landing page.
- dashboard.html	HTML	User-specific dashboard and cart view.
- login.html, register.html	HTML	Customer authentication pages.
- admin-*.html	HTML	All Admin Management pages.
- auth.js	JavaScript	Handles customer login/register logic and localStorage persistence.
- user-common.js	JavaScript	Handles session check, logout, and persistent shopping cart operations.
- script.js	JavaScript	General UI/UX enhancements (sliders, search toggles, password visibility).
- data.js	JavaScript	Provides the static array of sample book data.
- style.css, loginReg.css, 404Style.css	CSS	Project styling and responsiveness.

Installation and Setup
-----------------------
- Since this is a client-side application, no backend server is required.
- Clone or Download: Get all files from the project repository.
- Open in Browser: Open the index.html file directly in your web browser.

Important Notes
----------------
- Data Persistence: All data (users, cart, admin login state) is stored locally in the browser's localStorage. Clearing your browser's data will reset the application's state.
- Admin Access: Use the hardcoded credentials (admin / admin123) in the admin-login.html file to access the administrative panel.
