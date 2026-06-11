# EmailJS Contact Form - Quick Setup (5 Minutes)

## 🚀 Step-by-Step Setup

### Step 1: Create Free EmailJS Account (2 min)
```
1. Go to https://www.emailjs.com
2. Click "Sign Up" → "Free Plan"
3. Choose: Email/Password signup
4. Verify email in inbox
5. Login to dashboard
```

### Step 2: Connect Your Email (1 min)
```
1. Dashboard → "Email Services" → "Add Service"
2. Select Gmail (or your email provider)
3. Log in with your restaurant email
4. Allow EmailJS access
5. Copy the SERVICE ID shown
```

### Step 3: Create Email Template (1 min)
```
1. Dashboard → "Email Templates" → "Create New Template"
2. Name: "Al Qadri Contact Form"
3. Paste this as the email content:

---EMAIL CONTENT---
Subject: New Enquiry from {{from_name}}

From: {{from_name}} ({{from_phone}})
Inquiry Type: {{inquiry_type}}

Message:
{{message}}

Reply To: {{reply_to}}
---END---

4. Click "Save"
5. Copy the TEMPLATE ID (format: template_xxxxxx)
```

### Step 4: Get Your API Keys (1 min)
```
1. Dashboard → Settings ⚙️ → API Keys
2. Copy your PUBLIC KEY (format: xxxxxxxxxxxxxxxx)
```

### Step 5: Update Your Website (30 sec)
Open `index (1).html` and find this line (around line 13):
```javascript
emailjs.init('YOUR_EMAILJS_PUBLIC_KEY');
```
Replace with your actual key:
```javascript
emailjs.init('a1b2c3d4e5f6g7h8i9j0k1l2m3n4o5p6');
```

Then find this line (around line 42):
```javascript
emailjs.send('service_YOUR_SERVICE_ID', 'template_YOUR_TEMPLATE_ID', templateParams)
```
Replace with:
```javascript
emailjs.send('service_abc123def456', 'template_xyz789abc123', templateParams)
```

### Step 6: Test It! (30 sec)
```
1. Open your website
2. Scroll to Contact section
3. Fill form with test data
4. Click "Send Enquiry"
5. Check your email inbox
6. Should receive email in 5-10 seconds
```

---

## 📋 What to Copy/Paste

| What | Where to Find | Example |
|------|---------------|---------|
| **Public Key** | Settings → API Keys | a1b2c3d4e5f6g7h8i9j0k1l2m3n4o5p6 |
| **Service ID** | Email Services (after adding) | service_abc123def456 |
| **Template ID** | Email Templates (after creating) | template_xyz789abc123 |

---

## ✅ Verification Checklist

After setup, verify:
- [ ] Form validates name field (required)
- [ ] Form validates phone field (required)
- [ ] Submit button triggers email send
- [ ] Email arrives in 5-10 seconds
- [ ] Email contains all form data
- [ ] Success message shows after submission
- [ ] Form fields clear after submission

---

## 🆘 If It's Not Working

**Error: "Failed to send enquiry"**
- Check all 3 IDs are correctly copied (no extra spaces)
- Verify email service is active in EmailJS
- Check browser console for errors (F12)

**Email not arriving?**
- Check spam/junk folder
- Check EmailJS dashboard → Activity
- Verify email template is active

**Form still showing old message?**
- Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
- Clear browser cache

---

## 💡 Testing Template

Copy and paste into form to test:
- **Name:** Test Customer
- **Phone:** +91 9876543210
- **Type:** General Enquiry
- **Message:** This is a test message

---

**Estimated Time:** 5 minutes
**Cost:** Free forever (EmailJS free plan included)
**Result:** Working contact form! ✨
