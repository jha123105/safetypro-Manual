
# SafetyPro Rescue - Inventory Management System

## User Manual

---

## Table of Contents
1. [Getting Started](#getting-started)
2. [Login](#login)
3. [Dashboard](#dashboard)
4. [Stock In](#stock-in)
5. [Stock Out](#stock-out)
6. [Physical Count](#physical-count)
7. [Products](#products)
8. [Transactions](#transactions)
9. [Reports](#reports)
10. [Settings](#settings)
11. [Backup System](#backup-system)
12. [Notifications](#notifications)
13. [User Roles](#user-roles)
14. [Remote Access (Tailscale)](#remote-access-tailscale)

---

## Getting Started

### System Requirements
- Windows 10/11
- Node.js LTS
- Any modern browser (Chrome recommended)

### Installation
1. Extract the ZIP folder
2. Run `setup-windows.bat` (one-time)
3. Run `setup-autostart.bat` (optional - auto start with Windows)

### Accessing the System
- **Local:** `http://localhost:3000`
- **Network:** Settings → Network Access

---

## Login

### Default Credentials
| Role | Username | Password |
|------|----------|----------|
| Admin | admin | admin123 |
| Staff | staff | staff123 |

### Features
- Remember Me — Saves username
- Password show/hide toggle
- Session timeout — Auto-logout after 30 min inactive
- Change Password — Via user menu dropdown

---

## Dashboard

### Statistics Cards
- **Total Products** — All products in system
- **In Stock** — Above reorder level
- **Low Stock** — Below reorder level
- **Out of Stock** — Zero quantity

### Inventory Value
- Total value of all stock (quantity × price)

### Widgets
- **Category Summary** — Products per category
- **Low Stock Alerts** — Scrollable list
- **Recent Transactions** — Last 10 movements

### Inventory Table
- Search by name, code, or category
- Color-coded stock status
- Auto-refresh every 5 seconds

---

## Stock In

### Adding Stock
1. Go to **Stock In** tab
2. Search for product
3. Click product from results
4. Enter quantity
5. Click **Add Stock**
6. Confirm in modal

---

## Stock Out

### Removing Stock
1. Go to **Stock Out** tab
2. Search for product
3. Click product from results
4. Enter quantity
5. Select reason:
   - Sold
   - Used
   - Damaged
   - Expired
   - Other
6. Click **Remove Stock**
7. Confirm in modal

---

## Physical Count

### Monthly Inventory
1. Go to **Physical Count** tab
2. Count actual items on shelf
3. Enter actual quantity
4. Click Update (per item) or Update All
5. Confirm in modal

### Difference Colors
- 🟢 Green (+) = More than system
- 🔴 Red (-) = Less than system

---

## Products

### Viewing
- Search by name, code, category
- Sort by name, code, quantity, price
- Filter by status

### Stock Status Colors
- 🟢 Green = Above reorder
- 🟡 Yellow = Below reorder
- 🔴 Red = Out of stock

### Adding (Admin only)
1. Click **Add Product**
2. Item Code auto-generated
3. Enter name, category, quantity, unit, cost price, selling price, reorder level
4. Click Save

### Editing (Admin only)
1. Click 3-dot menu → Edit
2. Modify fields
3. Save Changes

### Deleting (Admin only)
1. Click 3-dot menu → Delete
2. Confirm

---

## Transactions

- Search by name, code, reason
- Filter by type (IN/OUT)
- Filter by date range
- Shows who performed each transaction

---

## Reports

### Types
1. **Inventory Report** — Stock levels and values
2. **Low Stock Report** — Items below reorder
3. **Transactions Report** — Stock movements
4. **Stock Movement Report** — Per-product summary
5. **Category Summary** — By category
6. **Profit Report** — Cost vs Revenue analysis

### Export
- **PDF** — With logo and business info
- **Excel** — Editable spreadsheet
- **CSV** — Simple format

### Filters
- Date range
- Type filter
- Sort options
- Category filter
- Search

---

## Settings

### Business Information
- Business name, address, phone, email
- Receipt footer message

### User Management (Admin only)
- Add users
- Edit users
- Delete staff users
- Deactivate/Activate staff

### Data Management
- Export/Import JSON
- Create backup
- View/restore backups
- Reset to sample data
- Clear all data

### Network Access
- View local and network IPs
- Tailscale IP for remote access
- Copy buttons

### Activity Log (Admin only)
- See all user actions
- Login/logout tracking
- Stock operations

---

## Backup System

### Automatic
- Every server start
- Keeps last 14 backups

### Manual
- Settings → Data Management → Create Backup

### Restore
1. View Backups
2. Select backup
3. Type "RESTORE"
4. Confirm

---

## Notifications

### Bell Icon (Top Bar)
- Low stock alerts
- Stock out notifications
- Staff login alerts
- Backup created
- Product deleted

### Features
- Badge with unread count
- Click to mark as read
- Clear all
- Shows who performed action

---

## User Roles

### Admin
- Full access
- User management
- Product management
- Physical count
- All reports
- Data management
- Activity log

### Staff
- Dashboard
- Stock In/Out
- Products (view)
- Transactions (view)
- Reports (view)

**Staff cannot:**
- Access Settings
- Access Physical Count
- Add/Edit/Delete products
- Clear transactions

---

## Remote Access (Tailscale)

### Setup
1. Install Tailscale on shop PC
2. Install Tailscale on phone/laptop
3. Sign in with same account
4. Use Tailscale IP to access

### Steps
1. Download: https://tailscale.com/download
2. Install and sign in
3. Check Settings → Network Access for Tailscale IP
4. Access from anywhere!

---

## Troubleshooting

### Server won't start
- Check Node.js installed
- Port 3000 free
- Run `npm install`

### Can't login
- Check username/password
- User might be deactivated

### Data lost
- Restore from backup

### Browser error
- Hard refresh (Ctrl+Shift+R)

---

## Support

**Developer:** Josh Hakkem Allawan
- Facebook: Josh Hakkem Allawan
- Telegram: @Joshie31 / 09946937855
- Email: joshhakkemallawan@gmail.com

---

*Version 1.0 - August 2026*
