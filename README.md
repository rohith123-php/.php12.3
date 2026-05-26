1. Overview
Bibliotech is a self-contained, premium administration portal designed for librarians to manage books, student records, and borrow/return cycles. It is built as an intermediate PHP web application utilizing a fast, lightweight SQLite database file—meaning it runs out-of-the-box using standard PHP runners (like XAMPP) without requiring configuration of separate database services.

2. Core Modules & Features
📊 Admin Panel Dashboard (dashboard.php)
Overview KPI Cards: Real-time metrics counting total book copies, active checkout counts, registered library memberships, and overdue warnings.
Circulation Metrics Visualizer: A custom, dynamic SVG Donut Chart rendering the ratio of issued vs. available book stock.
Alert System: Critical overdue checkout alerts showing days late and student names.
Recent Activities Log: Audit list showing the last 5 transactions.
📚 Book Catalog (books.php)
Catalog Registry: Grid containing title, author, category, ISBN, and stock indicators (In Stock, Issued, Out of Stock).
Live Dynamic Search: Client-side search field filtering matches across title, author, category, or ISBN instantly as you type.
CRUD Operations: Register new book stocks or adjust total copies with edit modals.
Integrity Guard: The system automatically checks references; it blocks the deletion of any books currently checked out by a student to prevent database errors.
🎓 Student Directory & Profiles (students.php)
Member Ledger: Database listing student names, roll card IDs, departments, and active checkout counters.
Detailed Profile Views: A separate page (?profile=ID) for each student listing their complete card info, total fines assessed, and historical checkout logs.
🔄 Circulation desk / Transactions (transactions.php)
Borrowing Flow: Dual-tab workspace split into "Active Checkouts" and "Returned History Logs."
Auto-complete Search: Autocomplete drop-downs for student and book selection.
Fine Calculation Engine: Automated logic assessing fine amounts at $0.50 per day past the return due date when returned.
⚙️ Database Admin Control Panel (db_manage.php)
Status Check: Reviews driver status and database file size.
Schema Migration: Allows initializing/dropping SQLite tables cleanly.
Demo Data Seeding: A single-button seeder populated with 10 classic books (e.g., 1984, Clean Code, Gatsby), 5 students, and simulated checkout logs (returned, active, and overdue entries).
3. Design Aesthetics & Visuals
UI Palette: Sleek modern space-dark palette incorporating a indigo and purple gradient layout, matching emerald success states, and rose danger highlights.
Layout Structure: Persistent responsive sidebar navigation with glassmorphism blurring effects (backdrop-filter) and smooth sliding animations.
Micro-interactions: Interactive buttons, autocomplete listings, card elevations, and self-closing error alert banners.
4. Technical Specifications
Server-side Logic: PHP 8.2 (Modular files, session management, transaction logic).
Database Driver: SQLite 3 via PDO driver (including PRAGMA foreign_keys = ON for referential safety).
Frontend: Responsive HTML5 templates, Vanilla CSS, and Native JS.
12:20 PM



# .php12.3
its some source code about the function
