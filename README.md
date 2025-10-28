# 🌐 Personal Portfolio Deployment Guide

This project is my **personal portfolio website** built using **React+Vite** and deployed on **GitHub Pages**.  
Below are the simple step-by-step instructions we followed to successfully deploy it.

---

## 🚀 Deployment Checklist

### 1️⃣ Install dependencies
npm install

### 2️⃣ Build the project
npm run build
This creates the `dist` folder (contains all production files).

---

### 3️⃣ Set the correct base path
Open **vite.config.js** and add your GitHub repo name:
export default defineConfig({
  base: '/your-repo-name/',
})
➡ Example: `/mypersonal_portfolio/`

---

### 4️⃣ Initialize Git and connect repository
git init  
git add .  
git commit -m "Initial commit"  
git branch -M main  
git remote add origin https://github.com/YourUsername/your-repo-name.git  
git push -u origin main  

If you get **“remote origin already exists”**, run:
git remote remove origin  
git remote add origin https://github.com/YourUsername/your-repo-name.git

---

### 5️⃣ Install GitHub Pages package
npm install gh-pages --save-dev

---

### 6️⃣ Add deploy scripts in package.json
Add these two lines under `"scripts"`:
"predeploy": "npm run build",  
"deploy": "gh-pages -d dist"

---

### 7️⃣ Deploy your project
npm run deploy  
Once you see **Published**, your site is live on the `gh-pages` branch.

---

### 8️⃣ Enable GitHub Pages
1. Go to your repository on GitHub  
2. Click **Settings → Pages**  
3. Under **Source**, select:  
   - **Branch:** `gh-pages`  
   - **Folder:** `/ (root)`  
4. Click **Save**  

After a few minutes, you’ll see a message like:  
Your site is published at https://YourUsername.github.io/your-repo-name/

---

## 🧠 Troubleshooting

| Issue | Fix |
|-------|-----|
| Remote origin already exists | Remove and re-add the origin |
| CSS/JS not loading | Check `base` path in `vite.config.js` |
| Push rejected | Run `git pull origin main --allow-unrelated-histories` before pushing |
| Website not appearing | Wait a few minutes or re-save the Pages settings |

---

## ✅ Final Result
Your website is live and can be shared using your GitHub Pages link! 🎉  

---

### ✨ Example
Live Demo: https://Saili1601.github.io/mypersonal_portfolio/

---

### 🧩 About
Created and deployed by **Saili Thombare**  
Built using **React+Vite + HTML + CSS + JavaScript**  
Hosted on **GitHub Pages**
