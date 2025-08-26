# Notion-P: Service Request Management System

A professional web application that helps businesses manage customer service requests using Notion as a database. This system automatically saves customer requests to your Notion workspace, handles file uploads, and sends email notifications when request statuses change.

## 🎥 **WATCH THE SETUP VIDEO**

**📺 Complete Setup Tutorial** - Follow along with step-by-step video instructions for the easiest setup experience!

<a href="https://youtu.be/wOrA6n0GLow" target="_blank">
  <img src="https://img.youtube.com/vi/wOrA6n0GLow/maxresdefault.jpg" alt="Setup Tutorial Video" style="width: 100%; height: auto; border-radius: 8px; box-shadow: 0 4px 12px rgba(0,0,0,0.15); cursor: pointer;" />
</a>

**Click the image above to watch the full video tutorial**

You are getting this for free. You will save bellow cost and effort.

### For Service Businesses ($500-$2,000 value)
- Immediate ROI: Saves 5-10 hours/week on manual data entry
- Professional Image: Clean, modern customer experience
- Cost Effective: Replaces expensive CRM systems
- Easy Setup: 15-30 minute deployment vs months of custom development

### For Agencies ($2,000-$10,000 value)
- White-Label Opportunity: Rebrand and resell to clients
- Recurring Revenue: Monthly maintenance and customization services
- Client Retention: Valuable service that keeps clients engaged
- Scalable Solution: Deploy for multiple clients quickly

## ⚠️ **IMPORTANT: This is NOT a 5-minute setup**

**Realistic Setup Time: 15-30 minutes** for first-time users using the template. The demo script claims "15 minutes" for users who follow the steps exactly.

## 🎯 What This System Does

**For Your Customers:**

- Fill out a professional web form with service request details
- Upload photos of broken items or issues (up to 5MB each)
- Receive automatic email updates when their request status changes
- Get a professional, trustworthy experience

**For Your Business:**

- All customer requests automatically appear in your Notion database
- No more manual data entry or lost paperwork
- Automatic email notifications keep customers informed
- Everything is organized and searchable in Notion
- File uploads are securely stored and linked to requests

## 📋 **PREREQUISITES - You Need These BEFORE Starting**

### Required Accounts & Access

- ✅ **GitHub account** (free)
- ✅ **Netlify account** (free)
- ✅ **Notion account** (free)
- ✅ **Gmail account** (free)

### Required Knowledge

- ✅ **Basic computer skills** (copy/paste, following step-by-step instructions)
- ✅ **Ability to create accounts** on websites
- ✅ **Patience** - this takes time to set up correctly

### What You DON'T Need

- ❌ **Coding knowledge** (everything is pre-built)
- ❌ **Server management** (Netlify handles this)
- ❌ **Database expertise** (Notion is user-friendly)

## 🚀 **DETAILED SETUP GUIDE**

### Step 1: Set Up Your Notion Database & Integration

#### 1.1 Create the Database First

**Duplicate the Template (RECOMMENDED)**

1. Click this link: [Database Template](https://www.notion.so/stackseekers/24a30c0a61cd80869243f2beb52b019c?v=24a30c0a61cd8018bb86000ce5206b10&source=copy_link)
2. Click **"Duplicate"** in the top right corner
3. Choose your workspace and location
4. **Rename it** to something like "Service Requests" or "Customer Support"

**⚠️ CRITICAL**: The template must have these exact column names for the form to work:

- `Full Name` (Title)
- `Email` (Email)
- `Product` (Text)
- `Serial Number` (Text)
- `Purchase Date` (Date)
- `Issue Details` (Text)
- `Issue Type` (Select) ← **This is critical for the dropdown**
- `Status` (Status)
- `Received Date` (Date)
- `Schedule Date` (Date) - Optional
- `Image Upload` (Files) - Optional

#### 1.2 Get Database ID

1. Look at your database URL: `https://notion.so/workspace-name/database-id-here`
2. **Copy the last part** (the database ID) - it's a long string of letters/numbers
3. **Save this somewhere safe** - you'll need it for the next steps

#### 1.3 Create Notion Integration

1. Go to your duplicated database in Notion
2. Click the **triple dot menu** (⋮) in the top right
3. Go to **"Connections"** → **"Develop integration"**
4. It will open another tab asking to add new integration
5. Click **"Add new integration"**
6. Give it a name like "Service Request Manager"
7. Choose associated workspace and type as **"Internal"**
8. Logo is optional, then hit **"Save"**
9. Click **"Configure integration settings"**
10. **Copy the value "Internal Integration Secret"** - this is your Notion API key
11. **Save this somewhere safe** - you'll need it for the next steps

#### 1.4 Share Database with Integration (CRITICAL STEP!)

1. Go back to your duplicated database in Notion
2. Go to **"Access"** tab
3. Select **"Pages"**
4. Choose **"Teamspace"** then **"Service Request"** (or you can select entire teamspace)
5. Hit **"Update access"**
6. This gives your integration permission to access the database

### Step 2: Set Up Gmail App Password

#### 2.1 Enable 2-Factor Authentication

1. Go to [myaccount.google.com/security](https://myaccount.google.com/security)
2. Enable **"2-Step Verification"** if not already enabled

#### 2.2 Create App Password

1. In the same security page, find **"App passwords"**
2. Click **"App passwords"**
3. Select **"Mail"** and **"Other (Custom name)"**
4. Name it "Service Request Manager"
5. Click **"Generate"**
6. **Copy the 16-character password** (save this safely!)

### Step 3: Deploy to Netlify

#### 3.1 Create GitHub Repository

1. Create a new **private repository** in your GitHub account
2. Click **"New"** then give repo name and description
3. Toggle **"Add README"** on then hit **"Create repository"**
4. Click **"Add file"** followed by **"Upload files"**
5. Use the drag-and-drop option to upload all the code files (download from the link in the description)
6. This gives you complete control and privacy over your code

#### 3.2 Connect to Netlify

1. Go to [netlify.com](https://netlify.com) and sign up/login
2. Click **"New site from Git"**
3. Choose **"GitHub"**
4. Select your **private repository** (not forked)
5. Click **"Deploy site"**

#### 3.3 Set Environment Variables (CRITICAL!)

1. In your Netlify dashboard, go to **"Site settings"**
2. Click **"Environment variables"**
3. Add these **exactly as shown**:

```
NOTION_API_KEY = secret_your_actual_api_key_here
NOTION_DATABASE_ID = your_actual_database_id_here
SMTP_USER = your_email@gmail.com
SMTP_PASS = your_16_character_app_password_here
```

4. **Click "Save"** after each one

**🚨 SECURITY WARNING**: Never add these environment variables to your Git repository! They contain sensitive information like API keys and passwords. Always set them in Netlify's dashboard only.

#### 3.4 Enable Netlify Blobs (REQUIRED for file uploads)

1. In your Netlify dashboard, go to **"Functions"**
2. Look for **"Netlify Blobs"** section
3. If it shows "Not enabled", click **"Enable"**
4. If you don't see this option, wait a few minutes and refresh

#### 3.5 Redeploy

1. Go to **"Deploys"** in your Netlify dashboard
2. Click **"Trigger deploy"** → **"Deploy site"**
3. Wait for deployment to complete

### Step 4: Test Your System

#### 4.1 Basic Form Test

1. Visit your Netlify site URL
2. Fill out the form with **test data**:
   - Product: "Test Product"
   - Serial Number: "TEST123"
   - Purchase Date: Today's date
   - Issue Type: Any option from your dropdown
   - Description: "This is a test request"
   - Client Name: "Test User"
   - Client Email: "your-email@gmail.com"
   - Phone: "123-456-7890"
3. **Don't upload files yet** - test the basic form first
4. Click Submit
5. Check your Notion database - the request should appear automatically

#### 4.2 File Upload Test

1. Go back to your form
2. Upload a small image file (under 1MB)
3. Submit the form
4. Check if the image appears in your Notion database

#### 4.3 Email Test

1. In your Notion database, change the Status to "Completed"
2. Wait a few minutes
3. Check your email for a notification

## 🚨 **COMMON FAILURE POINTS & SOLUTIONS**

### ❌ **"Notion API key missing" Error**

**What you'll see**: Error message or blank page
**Solution**:

1. Check your Netlify environment variables
2. Make sure `NOTION_API_KEY` starts with `secret_`
3. Copy/paste the key exactly - no extra spaces

### ❌ **"Database ID missing" Error**

**What you'll see**: Error message or blank page
**Solution**:

1. Check your Netlify environment variables
2. Make sure `NOTION_DATABASE_ID` is the long string from your URL
3. No extra spaces or characters

### ❌ **"Unauthorized" or "Forbidden" Error**

**What you'll see**: Error when trying to submit form
**Solution**:

1. **You forgot to share the database with your integration!**
2. Go back to Step 1.3 and share the database
3. Wait a few minutes, then try again

### ❌ **Photos not uploading**

**What you'll see**: Form submits but no images in Notion
**Solution**:

1. Check if Netlify Blobs is enabled in your dashboard
2. Wait a few minutes after first deployment
3. Try uploading a smaller file (under 1MB)
4. Check Netlify function logs for errors

### ❌ **Emails not sending**

**What you'll see**: Status changes but no email notifications
**Solution**:

1. Verify your Gmail app password is correct
2. Check that `SMTP_USER` is your full Gmail address
3. Make sure `SMTP_PASS` is the 16-character app password
4. Check Netlify function logs for SMTP errors

### ❌ **Form loads but dropdown is empty**

**What you'll see**: "Loading issue types..." never changes
**Solution**:

1. **Check your Netlify function logs** for errors in the `get-issue-types` function
2. **Verify your Notion API key has access** to the database
3. **Make sure the "Issue Type" column exists** in your database with exactly this name (case-sensitive)
4. **Ensure the "Issue Type" column is a Select field** (not Text or other types)
5. **Check that the column has select options** - if it's empty, the dropdown will be empty
6. **Verify the column name matches exactly**: `Issue Type` (with a space, not `IssueType` or `issue type`)

## 🔧 **How It Actually Works (Technical Reality)**

1. **Customer fills out form** → Data sent to Netlify Functions (serverless backend)
2. **Photos get uploaded** → Stored in Netlify Blobs (secure file storage)
3. **Data gets saved** → Automatically added to your Notion database via API
4. **Status monitoring** → System checks for changes every 2 minutes (cron job)
5. **Email notifications** → Automatic emails sent when status changes
6. **File cleanup** → Temporary files are automatically managed by Netlify

## 📱 **What Your Customers Actually Experience**

A clean, professional form where they can:

- **Product Details**: Enter product name, serial number, and purchase date (must be in the past)
- **Product Symptom**: Select issue type from dropdown (populated from your Notion database) and describe the problem
- **File Upload**: Drag & drop or click to upload images (up to 10 files, 5MB each, supports JPG, PNG, GIF, WebP, SVG)
- **Engineer Schedule**: Choose preferred date for engineer visit (must be in the future)
- **Contact Information**: Provide full name and email address

## 📊 **What You Actually See in Notion**

A well-organized database with these exact columns:

- **Full Name** (Title) - Customer's full name
- **Email** (Email) - Customer's email address
- **Product** (Text) - Product name and model
- **Serial Number** (Text) - Product serial number
- **Purchase Date** (Date) - When the product was purchased
- **Issue Details** (Text) - Description of the problem
- **Issue Type** (Select) - Category of the issue (populates the form dropdown)
- **Status** (Status) - Request status (New, In Progress, Completed, Rejected)
- **Received Date** (Date) - When the request was submitted
- **Schedule Date** (Date) - Preferred engineer visit date
- **Image Upload** (Files) - Uploaded photos and documents
- **Email Sent** (Checkbox) - Tracks if notification was sent
- **Email Sent Date** (Date) - When notification was sent

Plus easy filtering, searching, and multiple view options for workflow management.

## 🎨 **Customization Options (Advanced Users)**

### Change the Visual Design

- Edit `public/index.html` to modify the form design
- Update the logo by replacing `public/stackseekers.jpg`
- Modify colors and styling using the embedded Tailwind CSS

### Modify Form Fields

- Add or remove fields in the HTML form
- **IMPORTANT**: Update your Notion database structure to match
- Modify the JavaScript code that processes the form

### Customize Email Templates

The system includes comprehensive email customization options:

#### **Email Configuration (`config.js`)**

- **SMTP Settings**: Gmail SMTP configuration (host, port, security)
- **Email Subjects**: Customize subject lines for different statuses
- **Header Text**: Modify greeting messages and status update text
- **Section Titles**: Change labels for product details, issue type, etc.
- **Status Messages**: Customize messages for "Completed" and "Rejected" statuses
- **Footer Content**: Update team name, website, and contact information

#### **Email Templates (`email-templates.js`)**

- **Visual Styling**: Colors, fonts, layouts, and responsive design
- **Status-Specific Styling**: Different colors and icons for each status
- **Content Layout**: Grid layouts, cards, and information organization
- **Image Handling**: Product image display in emails
- **Branding Elements**: Headers, gradients, and professional styling

#### **What You Can Customize:**

- **Company branding** and colors
- **Email subjects** and message content
- **Status-specific messages** for different workflows
- **Visual design** and layout
- **SMTP settings** for different email providers
- **Email triggers** and automation rules

## 💡 **Pro Tips for Success**

1. **Test locally first**: Run `npm run dev` to test on your computer before deploying
2. **Use Gmail app passwords**: Never use your regular Gmail password
3. **Backup your database**: Export your Notion database regularly
4. **Monitor your Netlify logs**: Check the function logs if something isn't working
5. **Check the status function**: The system runs every 2 minutes to check for changes
6. **Start small**: Test with 1-2 requests before going live
7. **Keep API keys secure**: Don't share them or commit them to public repositories
8. **Never commit environment variables**: Keep `.env` files out of Git and use Netlify's dashboard

## 🔒 **Security & Privacy Features**

- All data is stored securely in Notion (your data, your control)
- No customer data is stored on Netlify servers
- Photos are securely stored in Netlify Blobs
- CORS is properly configured for cross-origin requests
- File uploads are validated for type and size
- API keys are stored securely in Netlify environment variables

## 💰 **Realistic Cost Breakdown**

- **Netlify**: Free tier includes 100GB bandwidth and 125K function calls per month
- **Notion**: Free tier includes unlimited databases and 5GB file storage
- **Gmail**: Free for sending emails (up to 500 per day)
- **Total**: $0 for most small to medium businesses

## 🎉 **What You Actually Get (After Successful Setup)**

Once deployed and working, you'll have a professional service request system that:

- Saves you hours on data entry and organization
- Keeps customers informed automatically
- Organizes everything in your Notion workspace
- Looks professional and builds customer trust
- Handles file uploads securely
- Scales with your business needs

## 🌟 **Open Source Benefits**

This project is open source, which means:

- **Transparency**: You can see exactly how it works
- **Customization**: Modify it to fit your specific needs
- **Community**: Get help from other developers
- **Security**: Code is reviewed by the community
- **No vendor lock-in**: You own your data and can modify the system

---

**Your customers will love the easy-to-use form, and you'll love having everything organized in one place with automatic notifications - but only after you get through the setup process successfully!**

**Built with ❤️ using Netlify Functions, Notion API, and modern web technologies**
