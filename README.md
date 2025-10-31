# VAPTIC - Deployment Guide & Roadmap

## 📋 What You Have Now

**Stage 1: Landing Page (COMPLETED)** ✅
- Modern dark-themed cybersecurity website
- Responsive design
- Animated effects and smooth scrolling
- Course showcase
- Features section
- Call-to-action sections

---

## 🚀 How to Deploy to GitHub Pages

### Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com) and log in
2. Click the **"+"** icon (top right) → **"New repository"**
3. Repository name: `vaptic` (or your GitHub username)
4. Make it **Public**
5. Click **"Create repository"**

### Step 2: Upload Your Website

**Option A: Via GitHub Web Interface (Easiest)**
1. In your new repository, click **"Add file"** → **"Upload files"**
2. Upload the `index.html` file
3. Scroll down and click **"Commit changes"**

**Option B: Via Git Command Line**
```bash
git clone https://github.com/YOUR-USERNAME/vaptic.git
cd vaptic
# Copy your index.html here
git add index.html
git commit -m "Initial VAPTIC landing page"
git push origin main
```

### Step 3: Enable GitHub Pages

1. In your repository, go to **Settings** → **Pages** (left sidebar)
2. Under "Source", select **"Deploy from a branch"**
3. Select branch: **main** and folder: **/ (root)**
4. Click **"Save"**
5. Wait 2-3 minutes

### Step 4: Access Your Website

Your site will be live at:
- **Format 1:** `https://YOUR-USERNAME.github.io/vaptic/`
- **Format 2 (if repo name = username):** `https://YOUR-USERNAME.github.io/`

⚠️ **Important:** GitHub Pages URLs are `username.github.io/repo-name`, not `vaptic.github.com`

### Custom Domain (Optional)
If you want `www.vaptic.com`:
1. Purchase domain from Namecheap/GoDaddy
2. Add CNAME record pointing to `YOUR-USERNAME.github.io`
3. In GitHub Settings → Pages, add custom domain
4. Follow [GitHub's custom domain guide](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)

---

## 🎨 Customization Guide

### Change Colors
Edit these CSS variables in the `<style>` section:
```css
:root {
    --primary-color: #00ff88;      /* Main accent color */
    --secondary-color: #00d4ff;    /* Secondary accent */
    --accent-color: #ff0066;       /* Highlight color */
    --dark-bg: #0a0e27;            /* Main background */
    --card-bg: #151932;            /* Card background */
}
```

### Add Your Email
Replace `contact@vaptic.com` with your actual email in:
- Line 503: Enroll button
- Line 515: Footer email link

### Update Social Links
Replace `#` with your actual social media URLs in the footer (around line 518)

### Modify Course Details
Edit the course cards section (around line 350) to update:
- Course names
- Descriptions
- Pricing
- Module details

---

## 📊 Next Steps: Stage 2 - LMS Backend

### Recommended Stack

**Backend:** Firebase (Google)
- ✅ **FREE tier:** 50K reads, 20K writes per day
- ✅ **No coding required** for basic features
- ✅ Perfect for 20 students (2 batches × 10 students)

**Features to Build:**
1. **Authentication** (Firebase Auth)
   - Email/password login
   - Student registration approval system
   
2. **Database** (Firestore)
   - User profiles
   - Course enrollment
   - Progress tracking (unlocked modules)
   - 20 modules × 2 courses
   
3. **File Storage** (Firebase Storage)
   - Videos (.mp4)
   - PDFs
   - ePub files
   
4. **Payment Integration** (Razorpay)
   - Accepts UK debit/credit cards
   - Deposits in INR to Indian bank account
   - ~2% transaction fee

### Estimated Timeline
- **Week 1-2:** Firebase setup, authentication, database structure
- **Week 3:** Student dashboard (show enrolled courses)
- **Week 4:** Course roadmap with locked/unlocked modules
- **Week 5:** File upload and delivery system
- **Week 6:** Manual approval workflow
- **Week 7:** Payment gateway integration
- **Week 8:** Testing and refinement

### Alternative: Low-Code Solutions
If you want even faster development:
- **Teachable** (hosted LMS, $39-119/month)
- **Thinkific** (hosted LMS, free tier available)
- **Podia** (all-in-one, $39/month)

But these won't give you custom `github.io` hosting.

---

## 💰 Payment Gateway Setup (Razorpay)

### Why Razorpay for UK → India?
- Accepts international cards (Visa, Mastercard, Amex)
- Settles in INR to Indian bank accounts
- Pricing: 2% + GST per transaction
- Easy integration with Firebase

### Setup Steps:
1. Sign up at [razorpay.com](https://razorpay.com)
2. Complete KYC verification
3. Enable international payments in dashboard
4. Get API keys (Test & Live)
5. Integrate via Firebase Cloud Functions

### Alternative: Stripe
- Also accepts UK cards
- Lower fees in some cases
- Can transfer to Indian accounts via Payoneer/Wise

---

## 🗺️ Roadmap Summary

### ✅ Stage 1: Landing Page (DONE)
- Professional website
- Course showcase
- GitHub Pages ready

### 🔄 Stage 2: Backend Setup (NEXT)
- Firebase project creation
- Authentication system
- Database structure

### 📝 Stage 3: Student Dashboard
- Login/signup pages
- Course enrollment view
- Progress tracking

### 🔓 Stage 4: Progressive Unlocking
- Module roadmap
- Lock/unlock logic based on class completion
- Resource delivery

### 💳 Stage 5: Payment Integration
- Razorpay/Stripe setup
- Payment confirmation
- Enrollment after payment

### 🎓 Stage 6: Admin Panel
- Approve students manually
- Unlock modules for batches
- View student progress

---

## 📞 Support & Next Actions

### What to do RIGHT NOW:
1. ✅ Download the `index.html` file
2. ✅ Create GitHub account (if you don't have one)
3. ✅ Create repository and upload the file
4. ✅ Enable GitHub Pages
5. ✅ Test your live website!

### When ready for Stage 2:
Let me know and I'll help you:
- Set up Firebase
- Create the database structure
- Build the login system
- Design the student dashboard

### Questions to Consider:
1. What's your expected pricing per course?
2. Do you have hosting for videos? (Vimeo/YouTube/Firebase)
3. Will courses run simultaneously or one after another?
4. Do you need a blog/news section?

---

## 🛠️ Technical Support

If you run into issues:
1. GitHub Pages not loading? Wait 5 minutes, then hard refresh (Ctrl+Shift+R)
2. Layout broken? Ensure you uploaded the complete `index.html` file
3. Want to edit? Any text editor works (Notepad++, VS Code, Sublime)

Ready to proceed to Stage 2? Just say the word! 🚀

---

**Created for:** VAPTIC Cybersecurity Training  
**Version:** 1.0  
**Last Updated:** October 2025
