# ✅ Lab 01: Website Cloning & Offline Browsing with HTTrack

## 🎯 Objective
Learn how to clone and mirror websites for offline analysis using HTTrack. Understand the limitations of static website cloning and explore the structure of downloaded sites.

## 🛠 Tools Used
- HTTrack

## 🔄 Task Summary
- Clone a public website using HTTrack.
- Analyze the local copy for assets, structure, and resources.

## 🧪 Steps

### 🔹 Step 1: Install HTTrack
```bash
sudo apt update
sudo apt install httrack
```

### 🔹 Step 2: Clone a website
```bash
httrack "http://example.com" -O ~/offline-site
```

### 🔹 Step 3: Navigate and open the offline website
```bash
cd ~/offline-site/example.com
firefox index.html
```

## 👀 Observations
- HTTrack downloads HTML, images, JavaScript, CSS, and other static resources.
- It does not clone backend code, databases, or server-side logic.
- Ideal for passive reconnaissance and offline analysis.

## ✅ Expected Output
- A complete offline version of the target website that can be viewed in a browser.
- Folder structure mirroring the original website with all static files.