# 🚀 React PWA (Experiment 3)

This project demonstrates how to convert a React application into a Progressive Web App (PWA) with offline capability using service workers.

---

## 📌 Objective

- Add a manifest.json for installability  
- Register a service worker  
- Enable offline support using caching  
- Verify PWA behavior (install + offline usage)

---

## 🛠️ Tech Stack

- React (Create React App - PWA Template)
- Service Workers (Workbox)
- HTML, CSS, JavaScript

---

## ⚙️ Setup Instructions

### 1. Create Project
npx create-react-app pwa --template cra-template-pwa  
cd pwa  

### 2. Install Dependencies (if needed)
npm install --legacy-peer-deps  
npm install web-vitals --legacy-peer-deps  

### 3. Run Development Server
npm start  

---

## 🔧 Enable PWA

Open: src/index.js  

Change:  
serviceWorkerRegistration.unregister();  

To:  
serviceWorkerRegistration.register();  

---

## 🏗️ Build for Production

npm run build  
npm install -g serve  
serve -s build  

---

## 🧪 Testing PWA Features

### ✅ Service Worker
- Open DevTools → Application → Service Workers  
- Status should be activated  

### ✅ Installable App
- Check install icon in browser  
- OR DevTools → Manifest  

### ✅ Offline Support
1. Open app normally  
2. Wait 5–10 seconds  
3. DevTools → Network → Offline  
4. Refresh page  

App should still load  

---

## 📂 Project Structure

pwa/  
├── public/  
│   ├── manifest.json  
│   └── icons  
├── src/  
│   ├── App.js  
│   ├── index.js  
│   ├── serviceWorkerRegistration.js  
│   └── reportWebVitals.js  
└── package.json  

---

## 🎯 Output

- React app runs normally  
- App is installable as PWA  
- App works without internet (offline mode)

---