# ALPHASK HOMES - Quick Start Guide

## 🚀 Quick Setup (5 minutes)

### 1. Free Firebase Account
Go to: https://firebase.google.com → Create New Project

### 2. Get Your Config
Firebase Console → Project Settings → Web App → Copy these 6 values:
```
API Key
Auth Domain
Database URL
Project ID
Storage Bucket
Messaging Sender ID
```

### 3. Connect to Your App
- Open: `house.html` in browser
- Login: admin@alphaskhomes.co.ke / alphask2024
- Click: **⚙️ CloudDB** (top right)
- Paste: All 6 Firebase config values
- Click: **Save**
- Done! ✅

Your data now syncs to Firebase cloud!

---

## 📋 Default Login Credentials

```
Email: admin@alphaskhomes.co.ke
Password: alphask2024
```

---

## 💾 Data Storage Options

### Current Setup (Firebase + Local)
- **Primary**: Firebase Cloud Database
- **Backup**: Browser LocalStorage
- **Sync**: Automatic

### Without Firebase (LocalStorage Only)
If you don't configure Firebase:
- Data stored in browser only
- Lost if cache is cleared
- Different per device/browser

### With Firebase (Recommended)
- Data stored on secure Google servers
- Access from any device
- Automatic backups
- Never lose data

---

## 🔐 Features Included

✅ Landlord Management
✅ Tenant Registration (10 property types)
✅ Rent Payment Tracking
✅ Deposits & Commission
✅ Zero Payment Recording
✅ Monthly Collection Reports
✅ Commission Tracking
✅ Revenue Reports
✅ Vacant Property Listings
✅ Payment History
✅ Cloud Backup with Firebase

---

## ⚙️ Firebase Console

After setup, monitor your data at:
```
https://console.firebase.google.com
```

View:
- All tenant & payment records
- Rent collection statistics
- Commission tracking
- Database size/usage

---

## 📱 Multi-Device Access

### Same Device, Different Browser
- Same data (if using Firebase)
- Auto-synced

### Different Devices
- Login with same account
- All data instantly accessible
- Changes sync in real-time

### Offline Access
- App works offline using local data
- Changes sync when online
- No data loss

---

## 🎯 Common Tasks

### Add New Landlord
1. Dashboard → Landlords tab
2. Click "+ Add Landlord"
3. Fill details → Save
4. ✓ Data saved to Firebase

### Add New Tenant
1. Dashboard → Tenants tab
2. Click "+ Add Tenant"
3. Choose property type
4. Fill details → Save
5. ✓ Auto-synced to Firebase

### Record Rent Payment
1. Click "Pay" button on tenant
2. Enter M-Pesa details
3. Generate receipt
4. Send SMS receipt
5. ✓ Payment recorded & synced

### View Reports
1. Dashboard → Reports tab
2. Choose:
   - Monthly Collections
   - Commission Tracking
   - Monthly Revenue
   - Annual Summary
   - Unpaid Rents
   - Vacancy Report

---

## 🛠️ Troubleshooting

**Data not syncing?**
- Check internet connection
- Verify Firebase credentials correct
- Go to ⚙️ CloudDB to reconfigure

**App says "Not connected to Firebase"?**
- Firebase not configured yet
- Click ⚙️ CloudDB button
- Enter Firebase config
- Save and reload

**Lost data?**
- Check Firebase Console
- LocalStorage acts as backup
- Data persists in browser

---

## 📞 Support

ALPHASK HOMES Support:
- 📞 0726 267 437 / 0737 002 969
- ✉️ alphoncewanje9@gmail.com

See **FIREBASE_SETUP_GUIDE.md** for detailed setup instructions.

---

**Version**: 1.0 with Firebase Cloud Integration
**Last Updated**: April 2026
**Status**: Production Ready ✓
