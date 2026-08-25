cat > USER-MANUAL.md << 'EOF'
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
12. [User Roles](#user-roles)

---

## Getting Started

### System Requirements
- Windows 10/11
- Node.js LTS (for setup)
- Any modern browser (Chrome recommended)

### Installation
1. Extract the project folder
2. Run `setup-windows.bat` (one-time)
3. Run `start-safetypro.bat` (every time)

### Accessing the System
- **Local:** `http://localhost:3000`
- **Network:** Check Settings → Network Access for IP

---

## Login

### Default Credentials
| Role | Username | Password |
|------|----------|----------|
| Admin | admin | admin123 |
| Staff | staff | staff123 |

### Features
- Remember Me checkbox saves username
- Password show/hide toggle
- Forgot password contact admin

---

## Dashboard

The dashboard shows:

### Statistics Cards
- **Total Products** - Number of products in system
- **In Stock** - Products above reorder level
- **Low Stock** - Products below reorder level
- **Out of Stock** - Products with zero quantity

### Inventory Value
- Total value of all stock (quantity × price)

### Widgets
- **Category Summary** - Top 6 categories by quantity
- **Low Stock Alerts** - Products needing reorder
- **Recent Transactions** - Last 5 stock movements

### Inventory Overview Table
- Search products by name, code, or category
- Color-coded status badges

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
5. Select reason (Sold, Used, Damaged, Expired, Other)
6. Click **Remove Stock**
7. Confirm in modal

---

## Physical Count

### Monthly Inventory Count
1. Go to **Physical Count** tab
2. Search products
3. Count actual items on shelf
4. Enter actual quantity
5. Click Update button or Update All

### Difference Display
- **Green (+)** = More than system
- **Red (-)** = Less than system

---

## Products

### Viewing Products
- Search by name, code, or category
- Sort by name, code, quantity, price
- Filter by status (In Stock, Low Stock, Out of Stock)

### Adding Products
1. Click **Add Product**
2. Item Code auto-generated
3. Enter product name
4. Select category (or add new)
5. Enter quantity
6. Select unit (or add new)
7. Enter price
8. Enter reorder level
9. Click Save

### Editing Products (Admin only)
1. Click three-dot menu
2. Select Edit
3. Modify fields
4. Click Save Changes

### Deleting Products (Admin only)
1. Click three-dot menu
2. Select Delete
3. Confirm in modal

### Stock Quantity Colors
- 🟢 Green = Above reorder level
- 🟡 Yellow = Below reorder level
- 🔴 Red = Out of stock

---

## Transactions

### Viewing History
- Search by name, code, or reason
- Filter by type (Stock In/Out)
- Filter by date range

### Transaction Types
- **IN** - Stock added
- **OUT** - Stock removed

---

## Reports

### Report Types
1. **Inventory Report** - All products with values
2. **Low Stock Report** - Products below reorder
3. **Transactions Report** - Stock movements
4. **Stock Movement Report** - Per-product summary
5. **Category Summary** - By category

### Export Options
- **PDF** - With company logo and info
- **Excel** - With company header
- **CSV** - Simple format

### Filters
- Date range
- Type filter
- Sort options
- Search within report

---

## Settings

### Business Information
- Business name
- Address
- Phone number
- Email
- Receipt footer message

### Network Access
- View local and network IPs
- Copy button for easy sharing

### User Management (Admin only)
- Add users
- Edit users (username, name, role, password)
- Delete staff users
- Deactivate/Activate staff

### Data Management
- Export data (JSON)
- Import data (Replace or Merge)
- Create manual backup
- View backups
- Reset to sample data
- Clear all data

---

## Backup System

### Automatic Backup
- Created every time server starts
- Keeps last 14 backups

### Manual Backup
1. Go to Settings → Data Management
2. Click **Create Backup**

### Restoring Backup
1. Click **View Backups**
2. Find backup to restore
3. Click restore icon
4. Type "RESTORE" to confirm
5. Database restored instantly

---

## User Roles

### Admin
- Full access to all features
- Manage users
- Manage products (add/edit/delete)
- Physical count
- All reports
- Data management

### Staff
- Dashboard (view)
- Stock In
- Stock Out
- Products (view only)
- Transactions (view)
- Reports (view)

**Staff cannot:**
- Access Settings
- Access Physical Count
- Add/Edit/Delete products
- Clear transactions

---

## Troubleshooting

### Server won't start
- Make sure Node.js is installed
- Check if port 3000 is free
- Run `npm install` again

### Can't login
- Check username and password
- Make sure user is active

### Browser shows error
- Hard refresh (Ctrl+Shift+R)
- Clear browser cache

### Data lost
- Restore from backup
- Check backups folder

---

## Support

**Developer:** Josh Hakkem Allawan
- Facebook: Josh Hakkem Allawan
- Telegram: @Joshie31 / 09946937855
- Email: joshhakkemallawan@gmail.com

---

*Version 1.0 - August 2026*
EOF
