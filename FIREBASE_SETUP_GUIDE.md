# 🔧 ALPHASK HOMES - Firebase Cloud Database Setup Guide

## Overview
Your ALPHASK HOMES Property Management System now supports cloud-based data persistence using Firebase Realtime Database. This ensures your data never gets lost and is accessible from anywhere.

## Why Firebase?
- ✅ **Cloud-based**: Data stored on secure Firebase servers
- ✅ **Real-time**: Changes sync instantly across devices
- ✅ **Offline support**: App works offline, syncs when reconnected
- ✅ **Automatic backup**: Google handles data backup
- ✅ **Free tier**: Generous free plan for small businesses
- ✅ **Encryption**: All data encrypted in transit

## Step-by-Step Firebase Setup

### 1. Create a Firebase Project
1. Go to [firebase.google.com](https://firebase.google.com)
2. Click **"Get Started"** or Sign in with Google
3. Click **"Create a project"**
4. Enter project name: `alphask-homes` (or your choice)
5. Uncheck "Enable Google Analytics" (optional)
6. Click **"Create project"**

### 2. Create Realtime Database
1. In Firebase Console, click **"Realtime Database"** (left menu)
2. Click **"Create Database"**
3. Choose location: `United States` (or closest to you)
4. Start in **test mode** (easier setup)
5. Click **"Enable"**
6. Copy the database URL (looks like: `https://alphask-homes-xxxx.firebaseio.com`)

### 3. Get Your Firebase Config
1. Click **Settings icon** (⚙️) → **Project settings**
2. Scroll to **"Your apps"** section
3. Click **"Web"** icon (looks like `</>`)
4. Register your app (name it `alphask-homes-web`)
5. Copy the full Firebase config object - you'll need:
   - apiKey
   - authDomain
   - databaseURL
   - projectId
   - storageBucket
   - messagingSenderId

### 4. Connect Firebase to ALPHASK HOMES
1. Open `house.html` in your browser
2. Log in with default credentials:
   - Email: `admin@alphaskhomes.co.ke`
   - Password: `alphask2024`
3. Click **⚙️ CloudDB** button (top right)
4. Fill in all Firebase configuration fields:
   - **API Key**: From Firebase Console
   - **Auth Domain**: `your-project.firebaseapp.com`
   - **Database URL**: `https://alphask-homes-xxxx.firebaseio.com`
   - **Project ID**: Your project ID
   - **Storage Bucket**: `your-project.appspot.com`
   - **Messaging Sender ID**: Your sender ID
5. Click **"Save Firebase Configuration"**
6. Page will reload automatically

### 5. Verify Connection
After setup, you should see:
- ✅ Green notification: "Connected to Firebase - Data is syncing to cloud"
- All your data automatically synced to Firebase

## Firebase Console Dashboard
Monitor your data at:
```
https://console.firebase.google.com/project/YOUR_PROJECT_ID/database
```

You'll see your data organized by:
- `users/` - Login accounts
- `landlords/` - Landlord information
- `tenants/` - Tenant records
- `payments/` - Rent payments
- `deposits/` - Deposit & commission records
- `zeroPayments/` - Non-payment records
- `vacantHouses/` - Vacant property listings
- `archive/` - Activity logs

## Data Backup & Storage
- **Local Storage**: Data always saved locally first (offline support)
- **Firebase**: Data syncs to cloud when online
- **Auto-Sync**: Changes upload automatically
- **Real-time Updates**: Multiple devices sync instantly

## Security Rules for Production

When ready for production, update your Firebase security rules:

```json
{
  "rules": {
    ".read": "auth != null",
    ".write": "auth != null",
    "users": {
      ".indexOn": ["email"]
    },
    "payments": {
      ".indexOn": ["tenantId", "landlordId", "month"]
    }
  }
}
```

Update in Firebase Console: **Realtime Database** → **Rules**

## Troubleshooting

### Connection Issues
- Verify all Firebase config fields are correct
- Check internet connection
- Clear browser cache and reload
- Ensure Firebase Database is in "test mode"

### Data Not Syncing
- Check browser console (F12) for errors
- Verify API key has database access
- Reset configuration and try again

### Lost Data
- Check Firebase Console at `firebase.google.com`
- Data is NOT deleted locally, reinstall to recover
- Firebase keeps automatic backups

## Migration from LocalStorage
Your existing data automatically:
1. Remains saved in browser localStorage
2. Gets synced to Firebase on first connection
3. Stays protected both locally and in cloud

## Hosting the App Online

### Option 1: Firebase Hosting (Recommended)
```bash
npm install -g firebase-tools
firebase login
firebase init hosting
firebase deploy
```

Your app will be live at: `your-project.web.app`

### Option 2: Other Hosting Providers
- Netlify
- Vercel
- GitHub Pages (static)
- Any web server (Apache, Nginx, etc.)

Just upload `house.html` and Firebase will handle data.

## Free Tier Limits
Firebase Free tier includes:
- ✅ 100 simultaneous connections
- ✅ 1 GB storage
- ✅ Unlimited read/write operations
- ✅ Perfect for small businesses

Upgrade to paid plan only if you exceed limits.

## Contact & Support
For ALPHASK HOMES support:
- 📞 0726 267 437 / 0737 002 969
- ✉️ alphoncewanje9@gmail.com

---

**Your data is now secure and accessible from anywhere! 🎉**
