# Service Request Manager

A simple web application that helps businesses manage customer service requests using Notion as a database. Think of it as a digital form that automatically saves customer requests to your Notion workspace and sends email notifications when things get updated.

## 🎯 What This Does

**For Your Customers:**

- Fill out a simple web form with their service request details
- Upload photos of their broken items or issues
- Get automatic email updates when their request status changes

**For Your Business:**

- All customer requests automatically appear in your Notion database
- No more manual data entry or lost paperwork
- Automatic email notifications keep customers informed
- Everything is organized and searchable in Notion

## 🚀 Quick Start (5 minutes)

### Step 1: Get Your Notion Setup Ready

1. **Create a Notion Integration**: Go to [notion.so/my-integrations](https://notion.so/my-integrations) and create a new integration
2. **Copy your API key** (looks like: `secret_abc123...`)
3. **Create a database** in Notion with these columns:
   - `Product` (Text)
   - `Serial Number` (Text)
   - `Purchase Date` (Date)
   - `Issue Type` (Select)
   - `Description` (Text)
   - `Status` (Select: "Pending", "In Progress", "Completed", "Rejected")
   - `Email Sent` (Checkbox)
   - `Client Email` (Email)
   - `Client Name` (Text)
   - `Phone` (Phone Number)
4. **Copy your database ID** from the URL (the part after the last slash)

### Step 2: Deploy to Netlify

1. **Fork this repository** to your GitHub account
2. **Sign up for Netlify** at [netlify.com](https://netlify.com)
3. **Connect your GitHub repository** to Netlify
4. **Set these environment variables** in Netlify:
   - `NOTION_API_KEY` = your Notion API key
   - `NOTION_DATABASE_ID` = your Notion database ID
   - `SMTP_USER` = your Gmail address
   - `SMTP_PASS` = your Gmail app password
5. **Deploy!** Netlify will automatically build and launch your site

### Step 3: Test It Out

1. Visit your new website (Netlify will give you a URL)
2. Fill out the service request form
3. Check your Notion database - the request should appear automatically!

## 🔧 How It Works (Simple Version)

1. **Customer fills out form** → Data goes to your Notion database
2. **Photos get uploaded** → Stored temporarily, then added to Notion
3. **Status changes** → Automatic emails sent to customers
4. **Everything syncs** → Your Notion database stays up-to-date

## 📱 What Your Customers See

A clean, professional form where they can:

- Enter product details (name, serial number, purchase date)
- Select the type of issue they're having
- Describe the problem in detail
- Upload photos (up to 5MB each)
- Provide contact information

## 📊 What You See in Notion

A organized database with:

- All customer requests in one place
- Status tracking for each request
- Customer contact information
- Attached photos and documents
- Easy filtering and searching

## 🎨 Customization

### Change the Look

- Edit `public/index.html` to modify the form design
- Update the logo by replacing `public/stackseekers.jpg`
- Modify colors and styling in the HTML file

### Modify the Form Fields

- Add or remove fields in the HTML form
- Update the Notion database structure to match
- Modify the JavaScript code that processes the form

### Change Email Templates

- Edit `netlify/functions/email-templates.js` to customize email messages
- Modify `netlify/functions/email-utils.js` to change email behavior

## 🚨 Troubleshooting

### "Notion API key missing" Error

- Make sure you've set `NOTION_API_KEY` in your Netlify environment variables
- Double-check that your Notion integration is active

### "Database ID missing" Error

- Verify `NOTION_DATABASE_ID` is set correctly in Netlify
- Make sure your Notion integration has access to the database

### Photos not uploading

- Check that your Netlify site has Blobs enabled (should happen automatically)
- Verify file sizes are under 5MB

### Emails not sending

- Ensure your Gmail app password is correct
- Check that `SMTP_USER` and `SMTP_PASS` are set properly

## 💡 Pro Tips

1. **Test locally first**: Run `npm run dev` to test on your computer before deploying
2. **Use Gmail app passwords**: Don't use your regular Gmail password - create an app password instead
3. **Backup your database**: Export your Notion database regularly
4. **Monitor your Netlify logs**: Check the function logs if something isn't working

## 🤝 Need Help?

1. **Check the logs**: Look at your Netlify function logs for error messages
2. **Verify setup**: Make sure all environment variables are set correctly
3. **Test step by step**: Try each part individually to isolate issues

## 📚 What's in the Box

- **`public/index.html`** - The customer-facing form
- **`netlify/functions/`** - Backend functions that handle everything
- **`netlify.toml`** - Configuration for Netlify
- **`package.json`** - List of required software packages

## 🔒 Security & Privacy

- All data is stored securely in Notion
- No customer data is stored on Netlify servers
- Photos are automatically cleaned up after 24 hours
- CORS is enabled for cross-origin requests

## 💰 Cost

- **Netlify**: Free tier includes 100GB bandwidth and 125K function calls per month
- **Notion**: Free tier includes unlimited databases and 5GB file storage
- **Gmail**: Free for sending emails (up to 500 per day)

## 🎉 You're All Set!

Once deployed, you'll have a professional service request system that:

- Saves you time on data entry
- Keeps customers informed automatically
- Organizes everything in Notion
- Looks professional and trustworthy

Your customers will love the easy-to-use form, and you'll love having everything organized in one place!
