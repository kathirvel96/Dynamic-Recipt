# 🧾 Dynamic Invoice & Receipt Builder

A modern, responsive, browser-based **Invoice, Receipt & Quotation Builder** built using **HTML5, CSS3, JavaScript and Bootstrap 5**.

Create professional invoices dynamically, calculate totals automatically, save invoice data locally, generate printable PDFs, and share invoice information through email or WhatsApp.

---

## ✨ Features

### 📄 Invoice Management

* Create **Invoices**
* Create **Receipts**
* Create **Quotations**
* Automatic invoice/document numbering
* Invoice date and due date
* Paid / Unpaid / Partially Paid status
* Multiple currency support:

  * ₹ INR
  * $ USD
  * € EUR
  * £ GBP

### 🏢 Business Details

Add your business information:

* Business name
* Address
* Phone number
* Email
* GSTIN / Tax ID

### 👤 Customer Details

Add complete customer information:

* Customer name
* Phone number
* Email
* Address

### 🛒 Dynamic Items

* Add unlimited products/services
* Remove individual items
* Item description
* Quantity
* Unit price
* Automatic line-item calculation

### 💰 Automatic Calculations

The application automatically calculates:

```text
Subtotal
    ↓
Discount
    ↓
Tax
    ↓
Shipping
    ↓
Grand Total
    ↓
Amount Paid
    ↓
Balance Due
```

Supports:

* Discount percentage
* Tax percentage
* Shipping charges
* Amount paid
* Balance due

### 💳 Payment Methods

Supported payment methods:

* Cash
* UPI
* Card
* Bank Transfer
* Cheque
* Other

### 👀 Live Invoice Preview

The invoice preview updates automatically whenever the user changes:

* Customer information
* Business information
* Products
* Quantity
* Price
* Discount
* Tax
* Shipping
* Payment details
* Invoice status

---

## 📑 PDF Export

Generate a professional **A4 PDF invoice** directly from the browser.

PDF export uses:

* `html2canvas`
* `jsPDF`

Features include:

* A4 page formatting
* High-resolution invoice rendering
* Multi-page PDF support
* Automatic filename generation
* Browser-based PDF generation
* No backend required

Example filename:

```text
INV-0001-Customer-Name.pdf
```

---

## 📧 Email Sharing

The **Email Invoice** button creates a pre-filled email using the browser's `mailto:` functionality.

The generated email can include:

* Customer name
* Invoice number
* Invoice date
* Total amount
* Paid amount
* Balance due
* Payment method
* Business details
* Notes

The customer email address is automatically used when available.

> Note: The browser opens the user's default email application. Sending the actual PDF attachment still depends on the email application being used.

---

## 💬 WhatsApp Sharing

The project is designed to support WhatsApp invoice sharing.

On supported mobile browsers, the native sharing system can be used to share the generated PDF.

On desktop or browsers without file-sharing support, WhatsApp can be opened with the invoice summary.

Example message:

```text
Hello Customer,

INVOICE INV-0001

From: ABC Business
Date: 2026-10-07

Total: ₹1,180.00
Paid: ₹1,000.00
Balance Due: ₹180.00

Payment: UPI

Thank you for your business!
```

> Important: A browser-only application cannot automatically create a public downloadable URL for a locally generated PDF. For true "PDF link" sharing, the PDF needs to be uploaded to a server/cloud storage service first.

---

## 💾 Local Storage

Invoices can be saved directly inside the browser using **LocalStorage**.

This allows users to:

* Save the current invoice
* Reload saved invoice data
* Continue editing later
* Work without a database

No account or backend is required.

---

## 🖨️ Printing

The invoice includes a print-optimized layout.

Users can:

```text
Print → Save as PDF
```

from the browser's native print dialog.

The print stylesheet automatically hides the application controls and displays only the invoice.

---

# 🛠️ Technology Stack

| Technology      | Purpose                       |
| --------------- | ----------------------------- |
| HTML5           | Application structure         |
| CSS3            | Custom styling                |
| JavaScript      | Dynamic functionality         |
| Bootstrap 5     | Responsive UI                 |
| Bootstrap Icons | Interface icons               |
| html2canvas     | Invoice rendering             |
| jsPDF           | PDF generation                |
| LocalStorage    | Browser-based invoice storage |

---

# 📁 Project Structure

The project is intentionally lightweight and can run as a standalone HTML application.

```text
Dynamic-Invoice-Receipt-Builder/
│
├── Dynamic_Invoice_Receipt_Builder.html
└── README.md
```

The main application contains:

```text
HTML
 ├── Header
 ├── Invoice Builder
 │    ├── Invoice Details
 │    ├── Business Details
 │    ├── Customer Details
 │    ├── Item Management
 │    ├── Tax & Discount
 │    └── Payment Details
 │
 └── Live Invoice Preview
      ├── Business Information
      ├── Customer Information
      ├── Item Table
      ├── Calculations
      └── Payment Summary
```

---

# 🚀 Getting Started

## 1. Download the Project

Download:

```text
Dynamic_Invoice_Receipt_Builder.html
```

## 2. Open the File

Simply double-click the HTML file.

Recommended browsers:

* Google Chrome
* Microsoft Edge
* Mozilla Firefox
* Safari

## 3. Start Creating an Invoice

Enter:

1. Business information
2. Customer information
3. Invoice details
4. Products/services
5. Quantity
6. Price
7. Discount
8. Tax
9. Payment information

The invoice preview updates automatically.

---

# 📦 Running Locally

No Node.js, PHP, Python or database is required.

Simply open:

```text
Dynamic_Invoice_Receipt_Builder.html
```

in a modern browser.

For development, you can also use **VS Code + Live Server**.

Example:

```text
VS Code
   ↓
Install Live Server
   ↓
Right Click HTML
   ↓
Open with Live Server
```

---

# 🎨 UI Design

The interface follows a modern dashboard-style design.

### Design characteristics

* Bootstrap 5 responsive grid
* Rounded cards
* Soft shadows
* Modern form controls
* Responsive invoice preview
* Mobile-friendly layout
* Professional A4 invoice design
* Status badges
* Action buttons
* Clean typography

---

# 📱 Responsive Design

The application is designed for:

* 💻 Desktop
* 🖥️ Laptop
* 📱 Mobile
* 📱 Tablet

On smaller screens, the invoice builder and preview automatically stack vertically.

---

# 🔢 Calculation Logic

The application uses the following calculation flow:

### Subtotal

```text
Subtotal = Σ (Quantity × Unit Price)
```

### Discount

```text
Discount = Subtotal × Discount %
```

### Taxable Amount

```text
Taxable Amount = Subtotal - Discount
```

### Tax

```text
Tax = Taxable Amount × Tax %
```

### Grand Total

```text
Grand Total = Taxable Amount + Tax + Shipping
```

### Balance

```text
Balance Due = Grand Total - Amount Paid
```

---

# 🔐 Privacy

This application is primarily client-side.

Invoice information is not automatically sent to a server.

Saved invoice data is stored using:

```javascript
localStorage
```

Therefore:

* No database is required
* No user account is required
* No backend is required
* Invoice data remains in the browser

> Users should avoid storing highly sensitive information on shared/public computers.

---

# ⚙️ Customization

Developers can easily customize:

### Company Branding

Modify:

```javascript
businessName
businessAddress
businessPhone
businessEmail
taxNo
```

### Currency

Add additional currencies to:

```html
<select id="currency">
```

### Invoice Status

Modify:

```javascript
statusBadge()
```

### Payment Methods

Modify:

```html
<select id="paymentMethod">
```

### Invoice Styling

Customize the CSS variables:

```css
:root {
    --primary: #4f46e5;
    --dark: #111827;
    --muted: #6b7280;
    --border: #e5e7eb;
}
```

---

# 🔮 Future Enhancements

Possible future improvements include:

* [ ] Multiple invoice templates
* [ ] Company logo upload
* [ ] Drag-and-drop invoice items
* [ ] Product database
* [ ] Customer database
* [ ] Invoice history
* [ ] Multiple saved invoices
* [ ] Invoice search
* [ ] Invoice editing
* [ ] Delete invoice
* [ ] Dashboard with sales statistics
* [ ] Monthly sales reports
* [ ] GST calculation
* [ ] CGST / SGST / IGST
* [ ] HSN/SAC codes
* [ ] Automatic GST invoice generation
* [ ] QR code for UPI payments
* [ ] Payment link generation
* [ ] Direct WhatsApp PDF attachment
* [ ] Cloud PDF hosting
* [ ] Firebase integration
* [ ] ASP.NET Core backend
* [ ] SQL Server database
* [ ] User authentication
* [ ] Admin dashboard
* [ ] Invoice numbering system
* [ ] Customer ledger
* [ ] Product inventory
* [ ] Stock management

---

# 🌐 Backend Upgrade

For a production business application, this frontend can later be connected to an API.

A possible architecture:

```text
                ┌─────────────────────┐
                │      Frontend       │
                │ HTML + Bootstrap +  │
                │    JavaScript       │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │     ASP.NET Core    │
                │       Web API       │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │     SQL Server      │
                └─────────────────────┘
```

This would allow:

* Multi-user access
* Permanent invoice storage
* Customer management
* Product management
* Invoice history
* Authentication
* Reports
* Cloud deployment

---

# 📄 Example Use Cases

This application can be adapted for:

* 🏪 Retail shops
* 🍽️ Restaurants
* ☕ Tea shops
* 💻 Software companies
* 🔧 Service centers
* 🏨 Hotels
* 🧑‍💼 Freelancers
* 📦 Small businesses
* 🏋️ Gyms
* 🛠️ Repair shops
* 🧾 Billing counters

---

# 🤝 Contributing

Contributions are welcome.

### Basic workflow

```bash
git clone <repository-url>
cd Dynamic-Invoice-Receipt-Builder
```

Make your changes and test them in a modern browser.

Then:

```bash
git add .
git commit -m "Improve invoice builder"
git push
```

---

# 🐛 Bug Reports

If you find a bug, please provide:

* Browser name and version
* Operating system
* Steps to reproduce
* Expected behavior
* Actual behavior
* Screenshot if possible

---

# 📜 License

This project can be used and modified according to the license included with the repository.

If no license has been added yet, consider adding an **MIT License** for an open-source project.

---

# 👨‍💻 Author

**Kathirvel Chinnasamy**

Full Stack .NET Developer

### Technologies

```text
C#
ASP.NET Core
ASP.NET Web API
SQL Server
JavaScript
HTML
CSS
Bootstrap
ERP Solutions
```

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.

**Built with HTML, CSS, JavaScript & Bootstrap ❤️**

