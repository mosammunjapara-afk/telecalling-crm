# 📞 Telecaller CRM — Complete Setup Guide

## 🚀 Quick Start (3 Steps)

### Step 1 — Install Python & Flask
```bash
pip install flask
```

### Step 2 — Run the App
```bash
cd crm
python app.py
```

### Step 3 — Open in Browser
```
http://localhost:5000
```

---

## 🔗 Important URLs

| Page | URL |
|------|-----|
| 🔐 Login | http://localhost:5000/login |
| 📋 Lead Form (Customer) | http://localhost:5000/form |
| 📊 Admin Dashboard | http://localhost:5000/admin |
| 👥 All Leads | http://localhost:5000/admin/leads |
| 🧑‍💼 Telecallers | http://localhost:5000/admin/telecallers |
| 📈 Reports | http://localhost:5000/admin/reports |

---

## 👤 Default Login

| Role | Username | Password |
|------|----------|----------|
| Admin | `admin` | `admin123` |
| Telecallers | Admin se add karein | — |

---

## 📋 Workflow (Poora Process)

```
1. Customer → /form pe jaata hai → Lead fill karta hai
           ↓
2. Admin ko notification aata hai (bell icon)
           ↓
3. Admin → /admin/leads mein lead dikhti hai (Pending status)
           ↓
4. Admin → Lead open karta hai → Approve karta hai + Telecaller assign karta hai
           ↓
5. Telecaller ko notification aata hai
           ↓
6. Telecaller → /tc mein lead dikhti hai
           ↓
7. Telecaller → Click-to-Call karta hai (📞 button → seedha phone dial)
            → Ya WhatsApp button → pre-written message ke saath WA khulta hai
           ↓
8. Telecaller → Call Log karta hai → Status update karta hai
           ↓
9. Admin → Reports mein sab track kar sakta hai
```

---

## ✨ Features

### 🌐 Public Lead Form (/form)
- Naam, Phone, WhatsApp, Email, City, Product, Budget — sab collect karta hai
- Submit hone pe Admin ko notification

### 🔐 Admin Panel
- **Telecaller Management** — Dynamically add, edit, delete telecallers
- **Lead Approval** — Pending leads approve/reject/hold kar sakte ho
- **Bulk Actions** — Ek saath kai leads approve/assign kar sakte ho
- **Lead Assignment** — Kisi bhi telecaller ko assign karo
- **Reports** — Source, status, daily count, telecaller performance
- **CSV Export** — Saari leads download karo

### 📞 Telecaller Panel
- **Click-to-Call** — Phone number pe click karo, seedha dial hoga
- **WhatsApp** — Pre-written message ke saath WhatsApp directly khulega
- **Call Log** — Har call ka record rakho
- **Quick Status** — Ek click mein status update karo
- **Documents** — Aadhar, PAN, Bank Statement etc. track karo
- **Follow-ups** — Aaj ke follow-ups highlighted dikhenge

---

## 🌐 Website mein Form Embed karna (Caryanams ya koi bhi)

Apni website pe yeh code add karo:
```html
<!-- Option 1: Direct Link -->
<a href="http://your-crm-server.com/form" target="_blank">Enquiry Bhejein</a>

<!-- Option 2: iFrame Embed -->
<iframe src="http://your-crm-server.com/form" 
        width="100%" height="700px" 
        frameborder="0" 
        style="border-radius:16px">
</iframe>
```

---

## 📁 Project Structure
```
crm/
├── app.py                    # Main Flask application
├── crm.db                    # SQLite database (auto-create hoga)
├── requirements.txt          # Dependencies
├── templates/
│   ├── base.html            # Common layout (sidebar, navbar)
│   ├── login.html           # Login page
│   ├── public_form.html     # Customer lead form
│   ├── form_success.html    # Form submit success
│   ├── admin_dashboard.html # Admin home
│   ├── admin_leads.html     # All leads list
│   ├── admin_telecallers.html # Telecaller management
│   ├── admin_reports.html   # Reports
│   ├── lead_detail.html     # Lead detail + call log + docs
│   ├── lead_form.html       # Add/Edit lead form
│   ├── tc_dashboard.html    # Telecaller dashboard
│   └── tc_leads.html        # Telecaller leads list
└── static/                  # CSS/JS/Images (optional)
```
