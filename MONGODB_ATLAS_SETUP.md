# 🗄️ MongoDB Atlas Setup - Step by Step

## 🎯 **Quick Setup (5 minutes)**

### **Step 1: Create MongoDB Atlas Account**
1. **Go to**: https://www.mongodb.com/atlas
2. **Click**: "Try Free" or "Get Started Free"
3. **Fill in**:
   - Email: Your email address
   - Password: Create a strong password
   - Account name: Your name or company
4. **Click**: "Create Account"
5. **Verify your email** (check inbox)

### **Step 2: Create Database Cluster**
1. **Click**: "Build a Database"
2. **Choose**: "FREE" tier (M0)
3. **Cloud Provider**: Choose any (AWS/Google Cloud/Azure)
4. **Region**: Select closest to you
5. **Click**: "Create Cluster"
6. **Wait**: 2-3 minutes for cluster to be ready

### **Step 3: Set Up Database Access**
1. **Go to**: "Database Access" (left sidebar)
2. **Click**: "Add New Database User"
3. **Fill in**:
   - Username: `imageapp_user`
   - Password: Create a strong password (save this!)
   - Role: "Read and write to any database"
4. **Click**: "Add User"

### **Step 4: Set Up Network Access**
1. **Go to**: "Network Access" (left sidebar)
2. **Click**: "Add IP Address"
3. **Click**: "Allow Access from Anywhere" (0.0.0.0/0)
4. **Click**: "Confirm"

### **Step 5: Get Connection String**
1. **Go to**: "Database" (left sidebar)
2. **Click**: "Connect"
3. **Choose**: "Connect your application"
4. **Copy** the connection string

### **Step 6: Update Your .env File**
1. **Open**: `.env` file in your project
2. **Replace** the MONGODB_URI line with:
   ```env
   MONGODB_URI=mongodb+srv://imageapp_user:YOUR_PASSWORD@cluster0.xxxxx.mongodb.net/image-upload-app?retryWrites=true&w=majority
   ```
3. **Replace**:
   - `YOUR_PASSWORD` with the password you created
   - `cluster0.xxxxx.mongodb.net` with your actual cluster URL

---

## 🚀 **Start Your App**

### **Terminal 1 - Start Backend**
```bash
# In E:\Components directory
npm run server
```

**Expected output:**
```
Server running on port 5000
MongoDB Connected
```

### **Terminal 2 - Start Frontend**
```bash
# In E:\Components\frontend-new directory
cd frontend-new
npm start
```

**Expected output:**
```
Local:            http://localhost:3000
```

---

## 🎉 **You're Done!**

- **Frontend**: http://localhost:3000
- **Backend**: http://localhost:5000
- **Database**: MongoDB Atlas (cloud)

**Test your app:**
1. Upload an image
2. View it in the gallery
3. Click to preview with zoom

---

## ❓ **Need Help?**

**If you see "MongoDB Connected"** → Everything is working! ✅

**If you see connection errors** → Check your .env file and password

**If you need help with any step** → Let me know which step you're stuck on! 